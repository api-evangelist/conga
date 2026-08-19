---
name: conga-send-for-signature
description: Send a document for e-signature with Conga Sign - create a package, add documents and signer roles, send it, then retrieve the signed documents and audit trail.
api: Conga Advantage Platform REST API
generated: '2026-08-13'
method: generated
source: openapi/conga-conga-sign.json, openapi/conga-esignature.json
operations:
  - Package_CreatePackage
  - Package_GetPackageById
  - Package_UpdatePackage
  - Package_ListPackages
  - Documents_CreateDocument
  - Documents_UpdateDocuments
  - Documents_GetDocumentVisibility
  - Documents_UpdateDocumentsVisibility
  - Approval_CreateApproval
  - Documents_CreateSignatureConfirmation
  - Documents_SignAllDocuments
  - Documents_GetZip
  - Documents_GetAllDocumentsZip
  - Package_GetPackageAudit
  - FileAttachment_AddAttachment
  - FileAttachment_GetZipAttachment
  - Package_CreatePackagesUsingBulkSend
  - Package_CreatePackageClone
---

# Send a document for signature with Conga Sign

Base: `https://rls.congacloud.com/api/sign` · scope: `sign`

Conga Sign is the one service in the platform whose OpenAPI carries real
`operationId`s, so bind to those rather than to paths.

## 1. Create the package

```
Package_CreatePackage        POST /v1/cs-packages
```

A *package* is the signing transaction: documents + roles + settings. Read it
back with `Package_GetPackageById` and mutate with `Package_UpdatePackage`.

To re-run a previous transaction or instantiate a template, use
`Package_CreatePackageClone` (`POST /v1/cs-packages/{packageId}/clone`) rather
than rebuilding the package.

## 2. Add documents

```
Documents_CreateDocument     POST /v1/cs-packages/{packageId}/documents
Documents_UpdateDocuments    PUT  /v1/cs-packages/{packageId}/documents
```

Control who sees what with `Documents_GetDocumentVisibility` /
`Documents_UpdateDocumentsVisibility` — visibility is per-role, and it is the
mechanism for multi-party deals where one signer must not see another's terms.

Supporting files the signer must upload are modelled as attachments:
`FileAttachment_AddAttachment`, and
`FileAttachment_CheckAttachmentExists` to confirm the signer actually uploaded.

## 3. Roles and notifications

Signer roles hang off the package (`/v1/cs-packages/{packageId}/roles`).
Notifications are explicit, per-package and per-role:

```
/v1/cs-packages/{packageId}/notifications
/v1/cs-packages/{packageId}/roles/{roleId}/notifications
/v1/cs-packages/{packageId}/roles/{roleId}/sms_notification
```

## 4. Approvals and signing

```
Approval_CreateApproval              POST /v1/cs-packages/{packageId}/documents/{documentId}/approvals
Documents_CreateSignatureConfirmation POST /v1/cs-packages/{packageId}/documents/signConfirm
Documents_SignAllDocuments           POST /v1/cs-packages/{packageId}/documents/signed_documents
```

## 5. Collect the result

```
Documents_GetZip             GET /v1/cs-packages/{packageId}/documents/zip
Documents_GetAllDocumentsZip GET /v1/cs-packages/{packageId}/documents/all-documents/zip
Package_GetPackageAudit      GET /v1/cs-packages/{packageId}/audit
```

`all-documents/zip` includes supporting documents; plain `zip` does not. The
audit trail is the evidence record. Where identity verification was used,
`IdvEvidenceSummary_GetIdvEvidenceSummary` and its image endpoints return the IDV
evidence.

## Completion signals

There is no published webhook payload catalog. Two options:

- Conga Sign callbacks: `/v1/cs-callback` and
  `/v1/cs-callback/connectors/{origin}` (see `asyncapi/conga-webhooks.yml`).
- Pull the eSignature event log:
  `GET /api/esign/v1/esignatures/eventlogs/{packageId}`.

Do not poll `Package_GetPackageById` in a tight loop — 100 req/s is a tenant-wide
budget shared with CPQ and CLM.

## Bulk

`Package_CreatePackagesUsingBulkSend`
(`POST /v1/cs-packages/{packageId}/bulk_send`) fans one package out to many
recipients.
