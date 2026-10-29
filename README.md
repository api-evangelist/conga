# Conga

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Conga (formerly Apttus + Conga) is an enterprise Revenue Lifecycle Management vendor whose Conga Advantage Platform unifies Configure-Price-Quote (CPQ), Contract Lifecycle Management (CLM), document generation and e-signature, X-Author authoring, approvals, billing and incentives, and AI-assisted contract intelligence. It is one of the largest documented API surfaces in the catalog: Conga publishes a complete OpenAPI 3.0.1 definition for every operation on its ReadMe-hosted developer portal at developer.conga.com - 2,136 operations across 31 services, captured here in openapi/. The platform is regionally partitioned (NA/EU/AU), secured with OAuth 2.0 bearer tokens minted from region-specific Conga login services that publish OIDC discovery and a real per-service scope set (api.cart, api.catalog, api.quote, api.order, api.user-management, api.revenue-admin, sign, doc-gen.composer and more), and uses JSON bodies, page/limit pagination with Content-Range headers, URI filter functions and a JSON:API-style error envelope. Conga also runs two machine surfaces it documents nowhere: a hosted, OAuth-gated MCP server at /mcp on every regional gateway, and a multi-tenant GraphQL API evidenced only by its own first-party npm client @conga-cloud/graphql. Conga is backed by ICONIQ Capital and Insight Partners.

**Areas:** Company · Enterprise Software · Contract Lifecycle Management · CPQ · Revenue Lifecycle Management · Document Automation · E-Signature · Contract Intelligence · CRM · OpenAPI · MCP · GraphQL

## Conga on APIs.io

Everything profiled for Conga is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/conga/](https://apis.io/providers/conga/)** — or go straight to one of the APIs or properties below.

### APIs (345)

- [Conga Advantage Platform MCP Server](https://apis.io/apis/conga/conga-advantage-platform-mcp-server/) — A hosted, remote Model Context Protocol server on every regional Conga Advantage Platform gateway. It answers MCP JSON-RPC over Streamable HTTP, rejects…
- [Conga GraphQL API](https://apis.io/apis/conga/conga-graphql-api/) — A multi-tenant GraphQL API over the Conga Advantage Platform data core, with Relay-style connections, cursor pagination, SOQL-like where predicates and…
- [Conga 2. Order Actions API](https://apis.io/apis/conga/conga-2-order-actions-api/) — Manages the complete lifecycle of your orders from initial confirmation through activation, modification, and cancellation.
- [Conga 3. Order Line Items API](https://apis.io/apis/conga/conga-3-order-line-items-api/) — Manages order line items represent each product, service, or subscription that a customer has purchased as part of an order.
- [Conga Account API](https://apis.io/apis/conga/conga-account-api/) — The Account API from Conga — 8 operation(s) for account.
- [Conga Account Attachments Blacklist API](https://apis.io/apis/conga/conga-accountattachmentsblacklist-api/) — The AccountAttachmentsBlacklist API from Conga — 1 operation(s) for accountattachmentsblacklist.
- [Conga Account Attachments Whitelist API](https://apis.io/apis/conga/conga-accountattachmentswhitelist-api/) — The AccountAttachmentsWhitelist API from Conga — 1 operation(s) for accountattachmentswhitelist.
- [Conga Account Designer Settings API](https://apis.io/apis/conga/conga-accountdesignersettings-api/) — The AccountDesignerSettings API from Conga — 1 operation(s) for accountdesignersettings.
- [Conga Account Email Reminder Settings API](https://apis.io/apis/conga/conga-accountemailremindersettings-api/) — The AccountEmailReminderSettings API from Conga — 1 operation(s) for accountemailremindersettings.
- [Conga Account Feature Settings API](https://apis.io/apis/conga/conga-accountfeaturesettings-api/) — The AccountFeatureSettings API from Conga — 1 operation(s) for accountfeaturesettings.
- [Conga Account Package Settings API](https://apis.io/apis/conga/conga-accountpackagesettings-api/) — The AccountPackageSettings API from Conga — 1 operation(s) for accountpackagesettings.
- [Conga Accounts API](https://apis.io/apis/conga/conga-accounts-api/) — The Accounts API from Conga — 4 operation(s) for accounts.
- [Conga Account Signing Logos API](https://apis.io/apis/conga/conga-accountsigninglogos-api/) — The AccountSigningLogos API from Conga — 1 operation(s) for accountsigninglogos.
- [Conga Account Signing Theme API](https://apis.io/apis/conga/conga-accountsigningtheme-api/) — The AccountSigningTheme API from Conga — 1 operation(s) for accountsigningtheme.
- [Conga Account Signing UI Options API](https://apis.io/apis/conga/conga-accountsigninguioptions-api/) — The AccountSigningUIOptions API from Conga — 1 operation(s) for accountsigninguioptions.
- [Conga Account Supported Languages API](https://apis.io/apis/conga/conga-accountsupportedlanguages-api/) — The AccountSupportedLanguages API from Conga — 1 operation(s) for accountsupportedlanguages.
- [Conga Account System Settings API](https://apis.io/apis/conga/conga-accountsystemsettings-api/) — The AccountSystemSettings API from Conga — 1 operation(s) for accountsystemsettings.
- [Conga Action Permissions API](https://apis.io/apis/conga/conga-action-permissions-api/) — The Action Permissions API from Conga — 1 operation(s) for action permissions.
- [Conga Activities API](https://apis.io/apis/conga/conga-activities-api/) — The Activities API from Conga — 1 operation(s) for activities.
- [Conga Activity History API](https://apis.io/apis/conga/conga-activityhistory-api/) — The ActivityHistory API from Conga — 1 operation(s) for activityhistory.
- [Conga Ad Hoc Groups API](https://apis.io/apis/conga/conga-adhocgroups-api/) — The AdHoc Groups Controller
- [Conga Adhoc Process API](https://apis.io/apis/conga/conga-adhocprocess-api/) — The AdhocProcess API from Conga — 5 operation(s) for adhocprocess.
- [Conga Adjustments API](https://apis.io/apis/conga/conga-adjustments-api/) — Adjustments controller
- [Conga Admin Permissions API](https://apis.io/apis/conga/conga-admin-permissions-api/) — The Admin Permissions API from Conga — 1 operation(s) for admin permissions.
- [Conga Adobe Sign API](https://apis.io/apis/conga/conga-adobesign-api/) — Adobe sign
- [Conga Agreement API](https://apis.io/apis/conga/conga-agreement-api/) — This class contains API endpoints for Agreements
- [Conga Agreement Clause API](https://apis.io/apis/conga/conga-agreementclause-api/) — This class holds APIs related to agreement clauses
- [Conga Agreement Document API](https://apis.io/apis/conga/conga-agreementdocument-api/) — This class contains APIs related to agreement documents.
- [Conga Agreement Document Checkin API](https://apis.io/apis/conga/conga-agreementdocumentcheckin-api/) — This class contains APIs related to agreement document checkins
- [Conga Agreement Lock API](https://apis.io/apis/conga/conga-agreementlock-api/) — This class contains API endpoints for Agreement Document's Lock.
- [Conga Agreement Metadata API](https://apis.io/apis/conga/conga-agreementmetadata-api/) — This class contains APIs for agreement metadata.
- [Conga Agreement Offline API](https://apis.io/apis/conga/conga-agreementoffline-api/) — This class contains APIs related to offline agreements.
- [Conga Agreement Review API](https://apis.io/apis/conga/conga-agreementreview-api/) — This class contains APIs for Agreement Review Controller.
- [Conga Agreement Signing Cycle API](https://apis.io/apis/conga/conga-agreementsigningcycle-api/) — Provides endpoints for managing and retrieving agreement signing cycles.
- [Conga Agreement Template API](https://apis.io/apis/conga/conga-agreementtemplate-api/) — This class contains APIs related to agreement and template related operations.
- [Conga AI Redline API](https://apis.io/apis/conga/conga-airedline-api/) — This class contains API endpoints for documents AI operation
- [Conga Alternate Clause API](https://apis.io/apis/conga/conga-alternateclause-api/) — This class contains API endpoints for alternate clauses related operations.
- [Conga Analytics API](https://apis.io/apis/conga/conga-analytics-api/) — This class holds APIs related to application usage
- [Conga API Connections API](https://apis.io/apis/conga/conga-api-connections-api/) — The API Connections API from Conga — 3 operation(s) for api connections.
- [Conga API Resource API](https://apis.io/apis/conga/conga-api-resource-api/) — The API Resource API from Conga — 7 operation(s) for api resource.
- [Conga Approval API](https://apis.io/apis/conga/conga-approval-api/) — The Approval API from Conga — 6 operation(s) for approval.
- [Conga Asset Actions API](https://apis.io/apis/conga/conga-assetactions-api/) — Controller to manage the asset action(s)
- [Conga Assets API](https://apis.io/apis/conga/conga-assets-api/) — Controller to manage assets
- [Conga Async Operation Status API](https://apis.io/apis/conga/conga-asyncoperationstatus-api/) — The AsyncOperationStatus API from Conga — 1 operation(s) for asyncoperationstatus.
- [Conga Attribute Constraint Rule Entries API](https://apis.io/apis/conga/conga-attribute-constraint-rule-entries-api/) — The Attribute Constraint Rule Entries API from Conga — 4 operation(s) for attribute constraint rule entries.
- [Conga Attribute Constraint Rules API](https://apis.io/apis/conga/conga-attribute-constraint-rules-api/) — The Attribute Constraint Rules API from Conga — 2 operation(s) for attribute constraint rules.
- [Conga Attribute Group Members API](https://apis.io/apis/conga/conga-attribute-group-members-api/) — The Attribute Group Members API from Conga — 2 operation(s) for attribute group members.
- [Conga Attribute Groups API](https://apis.io/apis/conga/conga-attribute-groups-api/) — The Attribute Groups API from Conga — 2 operation(s) for attribute groups.
- [Conga Attribute Matrices API](https://apis.io/apis/conga/conga-attribute-matrices-api/) — The Attribute Matrices API from Conga — 2 operation(s) for attribute matrices.
- [Conga Attribute Matrix Entries API](https://apis.io/apis/conga/conga-attribute-matrix-entries-api/) — The Attribute Matrix Entries API from Conga — 4 operation(s) for attribute matrix entries.
- [Conga Attributes API](https://apis.io/apis/conga/conga-attributes-api/) — Controller for managing attributes.
- [Conga Authentication Tokens API](https://apis.io/apis/conga/conga-authenticationtokens-api/) — The AuthenticationTokens API from Conga — 4 operation(s) for authenticationtokens.
- [Conga Authorization API](https://apis.io/apis/conga/conga-authorization-api/) — This class contains endpoints for authorizing sign providers like Conga Sign, Adobe Sign, or DocuSign, or wet signature.
- [Conga Backup Admin API](https://apis.io/apis/conga/conga-backupadmin-api/) — The BackupAdmin API from Conga — 1 operation(s) for backupadmin.
- [Conga Backup Delegates API](https://apis.io/apis/conga/conga-backupdelegates-api/) — The BackupDelegates API from Conga — 5 operation(s) for backupdelegates.
- [Conga Bulk Import API](https://apis.io/apis/conga/conga-bulk-import-api/) — The Bulk Import API from Conga — 5 operation(s) for bulk import.
- [Conga Bundle Line Item Structure API](https://apis.io/apis/conga/conga-bundlelineitemstructure-api/) — The BundleLineItemStructure API from Conga — 1 operation(s) for bundlelineitemstructure.
- [Conga Business Objects API](https://apis.io/apis/conga/conga-businessobjects-api/) — The BusinessObjects API from Conga — 15 operation(s) for businessobjects.
- [Conga Callback API](https://apis.io/apis/conga/conga-callback-api/) — The Callback API from Conga — 7 operation(s) for callback.
- [Conga Cart Analyzers API](https://apis.io/apis/conga/conga-cart-analyzers-api/) — Config Debug Rule Controller
- [Conga Carts API](https://apis.io/apis/conga/conga-carts-api/) — The Cart Controller
- [Conga Categories API](https://apis.io/apis/conga/conga-categories-api/) — The Categories API from Conga — 11 operation(s) for categories.
- [Conga CDN Store API](https://apis.io/apis/conga/conga-cdn-store-api/) — The CDN Store API from Conga — 3 operation(s) for cdn store.
- [Conga Clause API](https://apis.io/apis/conga/conga-clause-api/) — This class contains API endpoints for clauses.
- [Conga Clause Obligations API](https://apis.io/apis/conga/conga-clause-obligations-api/) — The Clause Obligations API from Conga — 3 operation(s) for clause obligations.
- [Conga Clause Comparison API](https://apis.io/apis/conga/conga-clausecomparison-api/) — This class contains API endpoints for clause semantic comparison
- [Conga Clause Content API](https://apis.io/apis/conga/conga-clausecontent-api/) — This class contains API endpoints for clause's content.
- [Conga Clause Library API](https://apis.io/apis/conga/conga-clauselibrary-api/) — This class contains API endpoints for clauses.
- [Conga Clause Metadata API](https://apis.io/apis/conga/conga-clausemetadata-api/) — This class contains API endpoints for template clause metadata
- [Conga Clause Version API](https://apis.io/apis/conga/conga-clauseversion-api/) — This class contains API endpoints for clause's version-related operations.
- [Conga Clone API](https://apis.io/apis/conga/conga-clone-api/) — The Clone API from Conga — 3 operation(s) for clone.
- [Conga Collaboration Request API](https://apis.io/apis/conga/conga-collaborationrequest-api/) — The Collaboration Request Controller
- [Conga Complex Field Definition API](https://apis.io/apis/conga/conga-complex-field-definition-api/) — The Complex Field Definition API from Conga — 3 operation(s) for complex field definition.
- [Conga Composer Parameter API](https://apis.io/apis/conga/conga-composerparameter-api/) — The ComposerParameter API from Conga — 2 operation(s) for composerparameter.
- [Conga Comprehensive Health Check API](https://apis.io/apis/conga/conga-comprehensivehealthcheck-api/) — The ComprehensiveHealthCheck API from Conga — 1 operation(s) for comprehensivehealthcheck.
- [Conga Configuration API](https://apis.io/apis/conga/conga-configuration-api/) — The Configuration API from Conga — 10 operation(s) for configuration.
- [Conga Configurations API](https://apis.io/apis/conga/conga-configurations-api/) — The Configurations API from Conga — 1 operation(s) for configurations.
- [Conga Hooks API](https://apis.io/apis/conga/conga-conga-hooks-api/) — The Conga Hooks API from Conga — 4 operation(s) for conga hooks.
- [Conga Hooks Rules API](https://apis.io/apis/conga/conga-conga-hooks-rules-api/) — The Conga Hooks Rules API from Conga — 4 operation(s) for conga hooks rules.
- [Conga Sign API](https://apis.io/apis/conga/conga-congasign-api/) — Send transaction using Conga Sign
- [Conga Constraint Rule Actions API](https://apis.io/apis/conga/conga-constraint-rule-actions-api/) — The Constraint Rule Actions API from Conga — 5 operation(s) for constraint rule actions.
- [Conga Constraint Rule Conditions API](https://apis.io/apis/conga/conga-constraint-rule-conditions-api/) — The Constraint Rule Conditions API from Conga — 2 operation(s) for constraint rule conditions.
- [Conga Constraint Rules API](https://apis.io/apis/conga/conga-constraint-rules-api/) — The Constraint Rules API from Conga — 2 operation(s) for constraint rules.
- [Conga Consumption Billing API](https://apis.io/apis/conga/conga-consumption-billing-api/) — Controller for CRUD operations on usage inputs, supporting rating, unrating, and draft rating in synchronous and asynchronous modes.
- [Conga Contact API](https://apis.io/apis/conga/conga-contact-api/) — The Contact API from Conga — 8 operation(s) for contact.
- [Conga Contact Users API](https://apis.io/apis/conga/conga-contact-users-api/) — The Contact Users API from Conga — 3 operation(s) for contact users.
- [Conga Contract API](https://apis.io/apis/conga/conga-contract-api/) — The Contract API from Conga — 4 operation(s) for contract.
- [Conga Contract Clause API](https://apis.io/apis/conga/conga-contract-clause-api/) — The Contract Clause API from Conga — 6 operation(s) for contract clause.
- [Conga Contract Cycle Time API](https://apis.io/apis/conga/conga-contract-cycle-time-api/) — The Contract Cycle Time API from Conga — 4 operation(s) for contract cycle time.
- [Conga Contract Documents API](https://apis.io/apis/conga/conga-contract-documents-api/) — The Contract Documents API from Conga — 15 operation(s) for contract documents.
- [Conga Contract Lifecycle API](https://apis.io/apis/conga/conga-contract-lifecycle-api/) — The Contract Lifecycle API from Conga — 9 operation(s) for contract lifecycle.
- [Conga Contract Obligations API](https://apis.io/apis/conga/conga-contract-obligations-api/) — The Contract Obligations API from Conga — 6 operation(s) for contract obligations.
- [Conga Contract Obligations Fulfillment API](https://apis.io/apis/conga/conga-contract-obligations-fulfillment-api/) — The Contract Obligations Fulfillment API from Conga — 6 operation(s) for contract obligations fulfillment.
- [Conga Contract Related List API](https://apis.io/apis/conga/conga-contract-related-list-api/) — The Contract Related List API from Conga — 3 operation(s) for contract related list.
- [Conga Contract Relationship API](https://apis.io/apis/conga/conga-contract-relationship-api/) — The Contract Relationship API from Conga — 5 operation(s) for contract relationship.
- [Conga Contract Request API](https://apis.io/apis/conga/conga-contract-request-api/) — The Contract Request API from Conga — 7 operation(s) for contract request.
- [Conga Contract Request Team Members API](https://apis.io/apis/conga/conga-contract-request-team-members-api/) — The Contract Request Team Members API from Conga — 4 operation(s) for contract request team members.
- [Conga Contract Team Members API](https://apis.io/apis/conga/conga-contract-team-members-api/) — The Contract Team Members API from Conga — 4 operation(s) for contract team members.
- [Conga Contract Type Document Requirement Settings API](https://apis.io/apis/conga/conga-contract-type-document-requirement-settings-api/) — Controller for managing Contract Type Document Requirement Settings
- [Conga Contract Checkin API](https://apis.io/apis/conga/conga-contractcheckin-api/) — This class contains APIs related to agreement document checkins
- [Conga Conversation Thread API](https://apis.io/apis/conga/conga-conversation-thread-api/) — Provides endpoints for managing conversation threads.
- [Conga Credit Memos API](https://apis.io/apis/conga/conga-credit-memos-api/) — API controller for managing credit memo operations.
- [Conga Currency Admin API](https://apis.io/apis/conga/conga-currency-admin-api/) — The Currency Admin API from Conga — 3 operation(s) for currency admin.
- [Conga Currency API](https://apis.io/apis/conga/conga-currency-api/) — The Currency API from Conga — 1 operation(s) for currency.
- [Conga Currency Format API](https://apis.io/apis/conga/conga-currency-format-api/) — The Currency Format API from Conga — 1 operation(s) for currency format.
- [Conga Currency Runtime API](https://apis.io/apis/conga/conga-currency-runtime-api/) — The Currency Runtime API from Conga — 3 operation(s) for currency runtime.
- [Conga Custom Code API](https://apis.io/apis/conga/conga-custom-code-api/) — The Custom Code API from Conga — 14 operation(s) for custom code.
- [Conga Custom Object API](https://apis.io/apis/conga/conga-custom-object-api/) — The Custom Object API from Conga — 9 operation(s) for custom object.
- [Conga Custom Plan Template API](https://apis.io/apis/conga/conga-custom-plan-template-api/) — The CustomPlanTemplate (also called BillingPlanTemplate) Controller
- [Conga Custom Plans API](https://apis.io/apis/conga/conga-custom-plans-api/) — Controller for managing generic custom billing plans. Provides endpoints to create, retrieve, and delete custom plans.
- [Conga Customer Onboarded API](https://apis.io/apis/conga/conga-customeronboarded-api/) — The CustomerOnboarded API from Conga — 1 operation(s) for customeronboarded.
- [Conga Custom Settings API](https://apis.io/apis/conga/conga-customsettings-api/) — The CustomSettings API from Conga — 9 operation(s) for customsettings.
- [Conga DAI API](https://apis.io/apis/conga/conga-dai-api/) — To do the operation reated to Discovery extraction and checking the status and marking
- [Conga Data Correction API](https://apis.io/apis/conga/conga-datacorrection-api/) — This class contains API endpoints for data correction-related operations.
- [Conga Deal Color Bands API](https://apis.io/apis/conga/conga-deal-color-bands-api/) — The Deal Color Bands API from Conga — 2 operation(s) for deal color bands.
- [Conga Deal Guidance Dimension Set Members API](https://apis.io/apis/conga/conga-deal-guidance-dimension-set-members-api/) — The Deal Guidance Dimension Set Members API from Conga — 2 operation(s) for deal guidance dimension set members.
- [Conga Deal Guidance Dimension Sets API](https://apis.io/apis/conga/conga-deal-guidance-dimension-sets-api/) — The Deal Guidance Dimension Sets API from Conga — 2 operation(s) for deal guidance dimension sets.
- [Conga Deal Guidance Dimensions API](https://apis.io/apis/conga/conga-deal-guidance-dimensions-api/) — The Deal Guidance Dimensions API from Conga — 2 operation(s) for deal guidance dimensions.
- [Conga Deal Guidance Rule Entries API](https://apis.io/apis/conga/conga-deal-guidance-rule-entries-api/) — The Deal Guidance Rule Entries API from Conga — 2 operation(s) for deal guidance rule entries.
- [Conga Deal Guidance Rules API](https://apis.io/apis/conga/conga-deal-guidance-rules-api/) — The Deal Guidance Rules API from Conga — 2 operation(s) for deal guidance rules.
- [Conga Dependent Picklist Definition API](https://apis.io/apis/conga/conga-dependent-picklist-definition-api/) — The Dependent Picklist Definition API from Conga — 1 operation(s) for dependent picklist definition.
- [Conga Document API](https://apis.io/apis/conga/conga-document-api/) — This class contains API endpoints for Document.
- [Conga Document Generation API](https://apis.io/apis/conga/conga-document-generation-api/) — The Document Generation API from Conga — 5 operation(s) for document generation.
- [Conga Document Settings API](https://apis.io/apis/conga/conga-document-settings-api/) — The Document Settings API from Conga — 7 operation(s) for document settings.
- [Conga Document Metadata API](https://apis.io/apis/conga/conga-documentmetadata-api/) — This class contains API endpoints for document metadata.
- [Conga Document Protection API](https://apis.io/apis/conga/conga-documentprotection-api/) — This class contains API endpoints for Document protection.
- [Conga Documents API](https://apis.io/apis/conga/conga-documents-api/) — The Documents API from Conga — 38 operation(s) for documents.
- [Conga Document Sync API](https://apis.io/apis/conga/conga-documentsync-api/) — This class contains API endpoints for Document Transfer Metadata Sync.
- [Conga Draft API](https://apis.io/apis/conga/conga-draft-api/) — The Draft API from Conga — 2 operation(s) for draft.
- [Conga Email API](https://apis.io/apis/conga/conga-email-api/) — This controller provides access to email operations like sending email in post delivery.
- [Conga Email Delivery Status API](https://apis.io/apis/conga/conga-email-delivery-status-api/) — The Email Delivery Status API from Conga — 2 operation(s) for email delivery status.
- [Conga Email Profile API](https://apis.io/apis/conga/conga-email-profile-api/) — The Email Profile API from Conga — 2 operation(s) for email profile.
- [Conga Email Sender API](https://apis.io/apis/conga/conga-email-sender-api/) — The Email Sender API from Conga — 4 operation(s) for email sender.
- [Conga Email Template API](https://apis.io/apis/conga/conga-email-template-api/) — The Email Template API from Conga — 8 operation(s) for email template.
- [Conga Email Template Category API](https://apis.io/apis/conga/conga-email-template-category-api/) — The Email Template Category API from Conga — 2 operation(s) for email template category.
- [Conga Encryption API](https://apis.io/apis/conga/conga-encryption-api/) — Encryption controller which will be used to create all the methods for encrypt/decrypt.
- [Conga Export API](https://apis.io/apis/conga/conga-export-api/) — Export cart data (line items) as CSV.
- [Conga External Endpoint Auth Credentials API](https://apis.io/apis/conga/conga-external-endpoint-auth-credentials-api/) — The External Endpoint Auth Credentials API from Conga — 2 operation(s) for external endpoint auth credentials.
- [Conga External Endpoint Configuration API](https://apis.io/apis/conga/conga-external-endpoint-configuration-api/) — The External Endpoint Configuration API from Conga — 3 operation(s) for external endpoint configuration.
- [Conga External Authentication API](https://apis.io/apis/conga/conga-externalauthentication-api/) — The ExternalAuthentication API from Conga — 1 operation(s) for externalauthentication.
- [Conga Favorites API](https://apis.io/apis/conga/conga-favorites-api/) — The Favorites API from Conga — 7 operation(s) for favorites.
- [Conga Feature API](https://apis.io/apis/conga/conga-feature-api/) — The Feature API from Conga — 2 operation(s) for feature.
- [Conga Feature Sets API](https://apis.io/apis/conga/conga-feature-sets-api/) — The Feature Sets API from Conga — 4 operation(s) for feature sets.
- [Conga Features API](https://apis.io/apis/conga/conga-features-api/) — The Features API from Conga — 2 operation(s) for features.
- [Conga Feature Settings API](https://apis.io/apis/conga/conga-featuresettings-api/) — Controller to fetch the feature settings
- [Conga Field Definition API](https://apis.io/apis/conga/conga-field-definition-api/) — The Field Definition API from Conga — 5 operation(s) for field definition.
- [Conga Field Expressions API](https://apis.io/apis/conga/conga-field-expressions-api/) — The Field Expressions API from Conga — 5 operation(s) for field expressions.
- [Conga Field History Tracking API](https://apis.io/apis/conga/conga-field-history-tracking-api/) — The Field History Tracking API from Conga — 1 operation(s) for field history tracking.
- [Conga Field History Tracking Config API](https://apis.io/apis/conga/conga-field-history-tracking-config-api/) — The Field History Tracking Config API from Conga — 2 operation(s) for field history tracking config.
- [Conga Field Permission API](https://apis.io/apis/conga/conga-field-permission-api/) — The Field Permission API from Conga — 3 operation(s) for field permission.
- [Conga Field Data API](https://apis.io/apis/conga/conga-fielddata-api/) — This class contains API endpoints for field's marking-related operations.
- [Conga Field Data Retrieval API](https://apis.io/apis/conga/conga-fielddataretrieval-api/) — This class contains API endpoints for retrieving document field data related operations.
- [Conga Field Mark API](https://apis.io/apis/conga/conga-fieldmark-api/) — This class contains API endpoints for field's marking-related operations.
- [Conga Fields API](https://apis.io/apis/conga/conga-fields-api/) — This class contains API endpoints for the document field's related operations.
- [Conga Field Set Settings API](https://apis.io/apis/conga/conga-fieldsetsettings-api/) — The FieldSetSettings API from Conga — 2 operation(s) for fieldsetsettings.
- [Conga Fields Validate API](https://apis.io/apis/conga/conga-fieldsvalidate-api/) — This class contains API endpoints for document field validation operations.
- [Conga File Store API](https://apis.io/apis/conga/conga-file-store-api/) — The File Store API from Conga — 17 operation(s) for file store.
- [Conga File Attachment API](https://apis.io/apis/conga/conga-fileattachment-api/) — The FileAttachment API from Conga — 7 operation(s) for fileattachment.
- [Conga Forecast Billing API](https://apis.io/apis/conga/conga-forecast-billing-api/) — The Forecast Billing API from Conga — 3 operation(s) for forecast billing.
- [Conga Frequency Conversion Admin API](https://apis.io/apis/conga/conga-frequency-conversion-admin-api/) — The Frequency Conversion Admin API from Conga — 3 operation(s) for frequency conversion admin.
- [Conga Frequency Conversion Runtime API](https://apis.io/apis/conga/conga-frequency-conversion-runtime-api/) — The Frequency Conversion Runtime API from Conga — 3 operation(s) for frequency conversion runtime.
- [Conga GlobalSearch Runtime API](https://apis.io/apis/conga/conga-globalsearch-runtime-api/) — The GlobalSearch Runtime API from Conga — 1 operation(s) for globalsearch runtime.
- [Conga Google Config API](https://apis.io/apis/conga/conga-googleconfig-api/) — This class contains API endpoints for google configurations such as google drive enabled and service configuration info
- [Conga Grant Login API](https://apis.io/apis/conga/conga-grant-login-api/) — The Grant Login API from Conga — 3 operation(s) for grant login.
- [Conga Guest User API](https://apis.io/apis/conga/conga-guest-user-api/) — The Guest User API from Conga — 4 operation(s) for guest user.
- [Conga Health Check API](https://apis.io/apis/conga/conga-health-check-api/) — The Health Check API from Conga — 2 operation(s) for health check.
- [Conga Hierarchies API](https://apis.io/apis/conga/conga-hierarchies-api/) — The Hierarchies API from Conga — 4 operation(s) for hierarchies.
- [Conga Idv Evidence Summary API](https://apis.io/apis/conga/conga-idvevidencesummary-api/) — The IdvEvidenceSummary API from Conga — 3 operation(s) for idvevidencesummary.
- [Conga Idv Workflow API](https://apis.io/apis/conga/conga-idvworkflow-api/) — The IdvWorkflow API from Conga — 1 operation(s) for idvworkflow.
- [Conga IF Workflow Configuration API](https://apis.io/apis/conga/conga-ifworkflowconfiguration-api/) — The IFWorkflowConfiguration API from Conga — 1 operation(s) for ifworkflowconfiguration.
- [Conga Imprint Fields API](https://apis.io/apis/conga/conga-imprintfields-api/) — The ImprintFields API from Conga — 3 operation(s) for imprintfields.
- [Conga In-Effect View API](https://apis.io/apis/conga/conga-in-effect-view-api/) — The In-Effect View API from Conga — 3 operation(s) for in-effect view.
- [Conga In App Reports API](https://apis.io/apis/conga/conga-inappreports-api/) — The InAppReports API from Conga — 4 operation(s) for inappreports.
- [Conga Incentive Conditions API](https://apis.io/apis/conga/conga-incentive-conditions-api/) — The Incentive Conditions API from Conga — 2 operation(s) for incentive conditions.
- [Conga Incentive Coupons API](https://apis.io/apis/conga/conga-incentive-coupons-api/) — The Incentive Coupons API from Conga — 3 operation(s) for incentive coupons.
- [Conga Incentive Limits API](https://apis.io/apis/conga/conga-incentive-limits-api/) — The Incentive Limits API from Conga — 2 operation(s) for incentive limits.
- [Conga Incentive Programs API](https://apis.io/apis/conga/conga-incentive-programs-api/) — The Incentive Programs API from Conga — 2 operation(s) for incentive programs.
- [Conga Incentive Rule Entries API](https://apis.io/apis/conga/conga-incentive-rule-entries-api/) — The Incentive Rule Entries API from Conga — 2 operation(s) for incentive rule entries.
- [Conga Incentive Rules API](https://apis.io/apis/conga/conga-incentive-rules-api/) — The Incentive Rules API from Conga — 2 operation(s) for incentive rules.
- [Conga Incentives API](https://apis.io/apis/conga/conga-incentives-api/) — The Incentives API from Conga — 3 operation(s) for incentives.
- [Conga Index Definition API](https://apis.io/apis/conga/conga-index-definition-api/) — The Index Definition API from Conga — 2 operation(s) for index definition.
- [Conga Initiate Billing API](https://apis.io/apis/conga/conga-initiate-billing-api/) — Controller to handle Billing Schedule related operations
- [Conga Intelligent Import API](https://apis.io/apis/conga/conga-intelligentimport-api/) — The IntelligentImport API from Conga — 5 operation(s) for intelligentimport.
- [Conga Intelligent Import Risk API](https://apis.io/apis/conga/conga-intelligentimportrisk-api/) — The IntelligentImportRisk API from Conga — 4 operation(s) for intelligentimportrisk.
- [Conga Invoice Configurations API](https://apis.io/apis/conga/conga-invoice-configurations-api/) — Provides endpoints for configuring and managing invoice run requests.
- [Conga Invoice Request Results API](https://apis.io/apis/conga/conga-invoice-request-results-api/) — Controller for managing invoice request results. Provides endpoints to retrieve invoice request result information.
- [Conga Invoices API](https://apis.io/apis/conga/conga-invoices-api/) — API controller for managing invoice operations.
- [Conga Jobs API](https://apis.io/apis/conga/conga-jobs-api/) — Handles actions related to workflow jobs
- [Conga JSON API](https://apis.io/apis/conga/conga-json-api/) — The Json API from Conga — 2 operation(s) for json.
- [Conga Layout API](https://apis.io/apis/conga/conga-layout-api/) — The Layout API from Conga — 2 operation(s) for layout.
- [Conga Locations API](https://apis.io/apis/conga/conga-locations-api/) — Catalog APIs for Locations
- [Conga Lock API](https://apis.io/apis/conga/conga-lock-api/) — LockController
- [Conga Log API](https://apis.io/apis/conga/conga-log-api/) — This class contains APIs for application logs.
- [Conga Lookup Field Settings API](https://apis.io/apis/conga/conga-lookup-field-settings-api/) — The Lookup Field Settings API from Conga — 2 operation(s) for lookup field settings.
- [Conga Lookup Field Data API](https://apis.io/apis/conga/conga-lookupfielddata-api/) — Lookup Field Data Controller
- [Conga Merge API](https://apis.io/apis/conga/conga-merge-api/) — This controller initiates Composer API Merge
- [Conga Migration API](https://apis.io/apis/conga/conga-migration-api/) — The Migration API from Conga — 1 operation(s) for migration.
- [Conga Milestone Schedule API](https://apis.io/apis/conga/conga-milestone-schedule-api/) — The Milestone Schedule API from Conga — 7 operation(s) for milestone schedule.
- [Conga Notification API](https://apis.io/apis/conga/conga-notification-api/) — The Notification API from Conga — 5 operation(s) for notification.
- [Conga Object Definition API](https://apis.io/apis/conga/conga-object-definition-api/) — The Object Definition API from Conga — 6 operation(s) for object definition.
- [Conga Object Definition Translation API](https://apis.io/apis/conga/conga-object-definition-translation-api/) — The Object Definition Translation API from Conga — 1 operation(s) for object definition translation.
- [Conga Object Metadata API](https://apis.io/apis/conga/conga-object-metadata-api/) — The Object Metadata API from Conga — 8 operation(s) for object metadata.
- [Conga Object Permission API](https://apis.io/apis/conga/conga-object-permission-api/) — The Object Permission API from Conga — 6 operation(s) for object permission.
- [Conga Obligations API](https://apis.io/apis/conga/conga-obligations-api/) — Controller for managing obligations.
- [Conga One Span Package API](https://apis.io/apis/conga/conga-onespanpackage-api/) — The OneSpanPackage API from Conga — 1 operation(s) for onespanpackage.
- [Conga One Span URL API](https://apis.io/apis/conga/conga-onespanurl-api/) — The OneSpanUrl API from Conga — 1 operation(s) for onespanurl.
- [Conga Open Search Sync Audit API](https://apis.io/apis/conga/conga-opensearchsyncaudit-api/) — The OpenSearchSyncAudit API from Conga — 1 operation(s) for opensearchsyncaudit.
- [Conga Opportunity API](https://apis.io/apis/conga/conga-opportunity-api/) — The Opportunity API from Conga — 7 operation(s) for opportunity.
- [Conga Option Group Members API](https://apis.io/apis/conga/conga-option-group-members-api/) — The Option Group Members API from Conga — 2 operation(s) for option group members.
- [Conga Option Groups API](https://apis.io/apis/conga/conga-option-groups-api/) — The Option Groups API from Conga — 8 operation(s) for option groups.
- [Conga Orchestrate API](https://apis.io/apis/conga/conga-orchestrate-api/) — The Orchestrate API from Conga — 1 operation(s) for orchestrate.
- [Conga Organization API](https://apis.io/apis/conga/conga-organization-api/) — The Organization API from Conga — 4 operation(s) for organization.
- [Conga Organization External Integration API](https://apis.io/apis/conga/conga-organization-external-integration-api/) — The Organization External Integration API from Conga — 4 operation(s) for organization external integration.
- [Conga Package API](https://apis.io/apis/conga/conga-package-api/) — The Package API from Conga — 12 operation(s) for package.
- [Conga Package Deployment API](https://apis.io/apis/conga/conga-package-deployment-api/) — The Package Deployment API from Conga — 8 operation(s) for package deployment.
- [Conga Package Migration API](https://apis.io/apis/conga/conga-packagemigration-api/) — This class contains API endpoints for package migration.
- [Conga Payment Terms API](https://apis.io/apis/conga/conga-payment-terms-api/) — Controller for managing payment terms.
- [Conga Permission Groups API](https://apis.io/apis/conga/conga-permission-groups-api/) — The Permission Groups API from Conga — 2 operation(s) for permission groups.
- [Conga Picklist Definition API](https://apis.io/apis/conga/conga-picklist-definition-api/) — The Picklist Definition API from Conga — 6 operation(s) for picklist definition.
- [Conga Platform Composer Feature Flag API](https://apis.io/apis/conga/conga-platformcomposerfeatureflag-api/) — The PlatformComposerFeatureFlag API from Conga — 1 operation(s) for platformcomposerfeatureflag.
- [Conga Playbook API](https://apis.io/apis/conga/conga-playbook-api/) — Provides API endpoints for managing playbooks associated with a contract. Supports retrieving available playbooks, playbook rules, and matched playbooks…
- [Conga Playbook Execution API](https://apis.io/apis/conga/conga-playbookexecution-api/) — Provides API endpoints for executing playbooks against contract documents and retrieving playbook execution results including clause and document rule outcomes.
- [Conga Preferences API](https://apis.io/apis/conga/conga-preferences-api/) — The Billing Preference Controller
- [Conga Preview API](https://apis.io/apis/conga/conga-preview-api/) — The Preview API from Conga — 1 operation(s) for preview.
- [Conga Price Dimensions API](https://apis.io/apis/conga/conga-price-dimensions-api/) — The Price Dimensions API from Conga — 3 operation(s) for price dimensions.
- [Conga Price Lists API](https://apis.io/apis/conga/conga-price-lists-api/) — The Price Lists API from Conga — 9 operation(s) for price lists.
- [Conga Price Matrices API](https://apis.io/apis/conga/conga-price-matrices-api/) — The Price Matrices API from Conga — 2 operation(s) for price matrices.
- [Conga Price Matrix Entries API](https://apis.io/apis/conga/conga-price-matrix-entries-api/) — The Price Matrix Entries API from Conga — 2 operation(s) for price matrix entries.
- [Conga Price Program Associations API](https://apis.io/apis/conga/conga-price-program-associations-api/) — The Price Program Associations API from Conga — 5 operation(s) for price program associations.
- [Conga Price Program Rule Entries API](https://apis.io/apis/conga/conga-price-program-rule-entries-api/) — The Price Program Rule Entries API from Conga — 2 operation(s) for price program rule entries.
- [Conga Price Program Rules API](https://apis.io/apis/conga/conga-price-program-rules-api/) — The Price Program Rules API from Conga — 2 operation(s) for price program rules.
- [Conga Price Programs API](https://apis.io/apis/conga/conga-price-programs-api/) — The Price Programs API from Conga — 2 operation(s) for price programs.
- [Conga Price Rule Entries API](https://apis.io/apis/conga/conga-price-rule-entries-api/) — The Price Rule Entries API from Conga — 2 operation(s) for price rule entries.
- [Conga Price Rule Sets API](https://apis.io/apis/conga/conga-price-rule-sets-api/) — The Price Rule Sets API from Conga — 2 operation(s) for price rule sets.
- [Conga Price Rules API](https://apis.io/apis/conga/conga-price-rules-api/) — The Price Rules API from Conga — 2 operation(s) for price rules.
- [Conga Price Escalator API](https://apis.io/apis/conga/conga-priceescalator-api/) — The PriceEscalator API from Conga — 2 operation(s) for priceescalator.
- [Conga Price Waterfall API](https://apis.io/apis/conga/conga-pricewaterfall-api/) — PriceWaterfall controller
- [Conga Process API](https://apis.io/apis/conga/conga-process-api/) — The Process API from Conga — 15 operation(s) for process.
- [Conga Process Steps API](https://apis.io/apis/conga/conga-processsteps-api/) — The ProcessSteps API from Conga — 3 operation(s) for processsteps.
- [Conga Product Attribute Groups API](https://apis.io/apis/conga/conga-product-attribute-groups-api/) — The Product Attribute Groups API from Conga — 2 operation(s) for product attribute groups.
- [Conga Product Attribute Rule Actions API](https://apis.io/apis/conga/conga-product-attribute-rule-actions-api/) — The Product Attribute Rule Actions API from Conga — 2 operation(s) for product attribute rule actions.
- [Conga Product Attribute Rules API](https://apis.io/apis/conga/conga-product-attribute-rules-api/) — The Product Attribute Rules API from Conga — 2 operation(s) for product attribute rules.
- [Conga Product Configurations API](https://apis.io/apis/conga/conga-product-configurations-api/) — The Product Billing Configuration Controller
- [Conga Product Groups API](https://apis.io/apis/conga/conga-product-groups-api/) — The Product Groups API from Conga — 8 operation(s) for product groups.
- [Conga Product Information API](https://apis.io/apis/conga/conga-product-information-api/) — The Product Information API from Conga — 2 operation(s) for product information.
- [Conga Product Option Components API](https://apis.io/apis/conga/conga-product-option-components-api/) — The Product Option Components API from Conga — 2 operation(s) for product option components.
- [Conga Product Option Prices API](https://apis.io/apis/conga/conga-product-option-prices-api/) — The Product Option Prices API from Conga — 2 operation(s) for product option prices.
- [Conga Product Option Groups API](https://apis.io/apis/conga/conga-productoptiongroups-api/) — The ProductOptionGroups API from Conga — 4 operation(s) for productoptiongroups.
- [Conga Products API](https://apis.io/apis/conga/conga-products-api/) — The Products API from Conga — 26 operation(s) for products.
- [Conga Property Permission API](https://apis.io/apis/conga/conga-property-permission-api/) — The Property Permission API from Conga — 2 operation(s) for property permission.
- [Conga Proposal Locations API](https://apis.io/apis/conga/conga-proposal-locations-api/) — The Proposal Locations API from Conga — 2 operation(s) for proposal locations.
- [Conga Query API](https://apis.io/apis/conga/conga-query-api/) — This class contains APIs for querying objects
- [Conga Quote API](https://apis.io/apis/conga/conga-quote-api/) — The quote controller
- [Conga Ramp Line Items API](https://apis.io/apis/conga/conga-ramplineitems-api/) — The Ramp Line Items Controller
- [Conga Ramps API](https://apis.io/apis/conga/conga-ramps-api/) — The Ramps Controller
- [Conga Rebate Programs API](https://apis.io/apis/conga/conga-rebate-programs-api/) — <p> <H3> <strong>⚠️ Deprecated:</strong> Rebate Program APIs have been deprecated from the Rebates-Admin Service.</H3> </p> <p> <H3>Please find these APIs…
- [Conga Rebate Rule Entries API](https://apis.io/apis/conga/conga-rebate-rule-entries-api/) — The Rebate Rule Entries API from Conga — 2 operation(s) for rebate rule entries.
- [Conga Rebate Rules API](https://apis.io/apis/conga/conga-rebate-rules-api/) — The Rebate Rules API from Conga — 2 operation(s) for rebate rules.
- [Conga Rebates API](https://apis.io/apis/conga/conga-rebates-api/) — Controller for handling rebate-related actions in the cart API.
- [Conga Reconciliation API](https://apis.io/apis/conga/conga-reconciliation-api/) — This class contains API endpoints related to document reconciliation
- [Conga Record Share API](https://apis.io/apis/conga/conga-record-share-api/) — The Record Share API from Conga — 6 operation(s) for record share.
- [Conga Record Type Permission API](https://apis.io/apis/conga/conga-record-type-permission-api/) — The Record Type Permission API from Conga — 5 operation(s) for record type permission.
- [Conga Record Type API](https://apis.io/apis/conga/conga-recordtype-api/) — This class contains APIs for the record type object
- [Conga RecordType Definition API](https://apis.io/apis/conga/conga-recordtype-definition-api/) — The RecordType Definition API from Conga — 2 operation(s) for recordtype definition.
- [Conga Redline Execution Status API](https://apis.io/apis/conga/conga-redlineexecutionstatus-api/) — Provides API endpoints for polling the status of a redline execution. Tracks extraction and redlining progress for rules applied against a contract document.
- [Conga Related Incentives API](https://apis.io/apis/conga/conga-related-incentives-api/) — The Related Incentives API from Conga — 2 operation(s) for related incentives.
- [Conga Related Price List Items API](https://apis.io/apis/conga/conga-related-price-list-items-api/) — The Related Price List Items API from Conga — 2 operation(s) for related price list items.
- [Conga Reminder API](https://apis.io/apis/conga/conga-reminder-api/) — The Reminder API from Conga — 1 operation(s) for reminder.
- [Conga Reports API](https://apis.io/apis/conga/conga-reports-api/) — The Reports API from Conga — 6 operation(s) for reports.
- [Conga Requests API](https://apis.io/apis/conga/conga-requests-api/) — The Requests API from Conga — 27 operation(s) for requests.
- [Conga Response Field Configuration API](https://apis.io/apis/conga/conga-responsefieldconfiguration-api/) — ResponseFieldConfigurationController
- [Conga Review API](https://apis.io/apis/conga/conga-review-api/) — The Review API from Conga — 12 operation(s) for review.
- [Conga Reviewer API](https://apis.io/apis/conga/conga-reviewer-api/) — Conga Reviewer APIs
- [Conga Role Admin API](https://apis.io/apis/conga/conga-role-admin-api/) — The Role Admin API from Conga — 7 operation(s) for role admin.
- [Conga Role API](https://apis.io/apis/conga/conga-role-api/) — The Role API from Conga — 6 operation(s) for role.
- [Conga Roles Verification API](https://apis.io/apis/conga/conga-rolesverification-api/) — The RolesVerification API from Conga — 2 operation(s) for rolesverification.
- [Conga Rule Dimensions API](https://apis.io/apis/conga/conga-ruledimensions-api/) — The RuleDimensions API from Conga — 2 operation(s) for ruledimensions.
- [Conga Rule Entries API](https://apis.io/apis/conga/conga-ruleentries-api/) — The RuleEntries API from Conga — 4 operation(s) for ruleentries.
- [Conga Rule Execution API](https://apis.io/apis/conga/conga-ruleexecution-api/) — Provides API endpoints for executing individual playbook rules against contract documents and retrieving clause-level and document-level rule execution results.
- [Conga Rules API](https://apis.io/apis/conga/conga-rules-api/) — The Rules API from Conga — 10 operation(s) for rules.
- [Conga Salesforce API](https://apis.io/apis/conga/conga-salesforce-api/) — This controller provides access to information inside a customer's salesforce account.
- [Conga Scheduler API](https://apis.io/apis/conga/conga-scheduler-api/) — The Scheduler API from Conga — 11 operation(s) for scheduler.
- [Conga Search Admin API](https://apis.io/apis/conga/conga-search-admin-api/) — The Search Admin API from Conga — 10 operation(s) for search admin.
- [Conga Search Runtime API](https://apis.io/apis/conga/conga-search-runtime-api/) — The Search Runtime API from Conga — 6 operation(s) for search runtime.
- [Conga Sender API](https://apis.io/apis/conga/conga-sender-api/) — The Sender API from Conga — 6 operation(s) for sender.
- [Conga Services API](https://apis.io/apis/conga/conga-services-api/) — Catalog APIs to search service products
- [Conga Session API](https://apis.io/apis/conga/conga-session-api/) — The Session API from Conga — 1 operation(s) for session.
- [Conga Settings API](https://apis.io/apis/conga/conga-settings-api/) — The Settings API from Conga — 2 operation(s) for settings.
- [Conga Sign API](https://apis.io/apis/conga/conga-sign-api/) — sign APIs
- [Conga Signature Image API](https://apis.io/apis/conga/conga-signatureimage-api/) — The SignatureImage API from Conga — 1 operation(s) for signatureimage.
- [Conga Signature Layout API](https://apis.io/apis/conga/conga-signaturelayout-api/) — The SignatureLayout API from Conga — 1 operation(s) for signaturelayout.
- [Conga Solution API](https://apis.io/apis/conga/conga-solution-api/) — The Solution API from Conga — 5 operation(s) for solution.
- [Conga Split Criteria API](https://apis.io/apis/conga/conga-split-criteria-api/) — Provides endpoints for managing invoice split criteria setups, including creation, activation, and deactivation.
- [Conga Status API](https://apis.io/apis/conga/conga-status-api/) — Get merge process status
- [Conga Storefronts API](https://apis.io/apis/conga/conga-storefronts-api/) — The Storefronts API from Conga — 3 operation(s) for storefronts.
- [Conga Sub Accounts API](https://apis.io/apis/conga/conga-subaccounts-api/) — The SubAccounts API from Conga — 4 operation(s) for subaccounts.
- [Conga Summary Groups API](https://apis.io/apis/conga/conga-summarygroups-api/) — The Summary Groups Controller
- [Conga Tax Codes API](https://apis.io/apis/conga/conga-tax-codes-api/) — TaxCodes Controller
- [Conga Team Role API](https://apis.io/apis/conga/conga-team-role-api/) — The Team Role API from Conga — 3 operation(s) for team role.
- [Conga Template API](https://apis.io/apis/conga/conga-template-api/) — Controller for Templates APIs
- [Conga Template Migrate API](https://apis.io/apis/conga/conga-templatemigrate-api/) — This class contains API endpoints for template migration.
- [Conga Timezone and Locale API](https://apis.io/apis/conga/conga-timezone-and-locale-api/) — The Timezone and Locale API from Conga — 9 operation(s) for timezone and locale.
- [Conga Token API](https://apis.io/apis/conga/conga-token-api/) — The Token API from Conga — 3 operation(s) for token.
- [Conga Translation Audit History Tracking API](https://apis.io/apis/conga/conga-translation-audit-history-tracking-api/) — The Translation Audit History Tracking API from Conga — 1 operation(s) for translation audit history tracking.
- [Conga Translation Management Runtime API](https://apis.io/apis/conga/conga-translation-management-runtime-api/) — The Translation Management Runtime API from Conga — 1 operation(s) for translation management runtime.
- [Conga Translation Runtime API](https://apis.io/apis/conga/conga-translation-runtime-api/) — The Translation Runtime API from Conga — 5 operation(s) for translation runtime.
- [Conga Translations Management Admin API](https://apis.io/apis/conga/conga-translations-management-admin-api/) — The Translations Management Admin API from Conga — 11 operation(s) for translations management admin.
- [Conga Type Ahead API](https://apis.io/apis/conga/conga-typeahead-api/) — The TypeAhead API from Conga — 1 operation(s) for typeahead.
- [Conga UFC API](https://apis.io/apis/conga/conga-ufc-api/) — The UFC API from Conga — 2 operation(s) for ufc.
- [Conga UOM Conversion Admin API](https://apis.io/apis/conga/conga-uom-conversion-admin-api/) — The UOM Conversion Admin API from Conga — 3 operation(s) for uom conversion admin.
- [Conga UOM Conversion Runtime API](https://apis.io/apis/conga/conga-uom-conversion-runtime-api/) — The UOM Conversion Runtime API from Conga — 3 operation(s) for uom conversion runtime.
- [Conga Usage Tiers API](https://apis.io/apis/conga/conga-usagetiers-api/) — Usage Tiers Controller
- [Conga User Admin API](https://apis.io/apis/conga/conga-user-admin-api/) — The User Admin API from Conga — 15 operation(s) for user admin.
- [Conga User API](https://apis.io/apis/conga/conga-user-api/) — User Search APIs
- [Conga User Group API](https://apis.io/apis/conga/conga-user-group-api/) — The User Group API from Conga — 3 operation(s) for user group.
- [Conga User Group Member API](https://apis.io/apis/conga/conga-user-group-member-api/) — The User Group Member API from Conga — 5 operation(s) for user group member.
- [Conga User Dashboard API](https://apis.io/apis/conga/conga-userdashboard-api/) — The UserDashboard API from Conga — 4 operation(s) for userdashboard.
- [Conga Validation API](https://apis.io/apis/conga/conga-validation-api/) — The Validation API from Conga — 2 operation(s) for validation.
- [Conga Virtual Room API](https://apis.io/apis/conga/conga-virtualroom-api/) — The VirtualRoom API from Conga — 5 operation(s) for virtualroom.
- [Conga Visibility Rules API](https://apis.io/apis/conga/conga-visibility-rules-api/) — The Visibility Rules API from Conga — 2 operation(s) for visibility rules.
- [Conga Waterfall Charts API](https://apis.io/apis/conga/conga-waterfall-charts-api/) — The Waterfall Charts API from Conga — 2 operation(s) for waterfall charts.
- [Conga Waterfall Rules API](https://apis.io/apis/conga/conga-waterfall-rules-api/) — The Waterfall Rules API from Conga — 2 operation(s) for waterfall rules.
- [Conga Waterfall Rule Entry API](https://apis.io/apis/conga/conga-waterfallruleentry-api/) — The WaterfallRuleEntry API from Conga — 2 operation(s) for waterfallruleentry.
- [Conga Waterfall Ruleset API](https://apis.io/apis/conga/conga-waterfallruleset-api/) — The WaterfallRuleset API from Conga — 2 operation(s) for waterfallruleset.
- [Conga Waterfalls API](https://apis.io/apis/conga/conga-waterfalls-api/) — The Waterfalls API from Conga — 2 operation(s) for waterfalls.
- [Conga O Auth2 API](https://apis.io/apis/conga/conga-oauth2-api/) — The OAuth2 API from Conga — 4 operation(s) for oauth2.
- [Conga Account Roles API](https://apis.io/apis/conga/conga-account-roles-api/) — The Account Roles API from Conga — 4 operation(s) for account roles.
- [Conga Account Settings API](https://apis.io/apis/conga/conga-account-settings-api/) — The Account Settings API from Conga — 1 operation(s) for account settings.
- [Conga Admin Settings API](https://apis.io/apis/conga/conga-admin-settings-api/) — This class contains API endpoints for admin setting
- [Conga Business Object API](https://apis.io/apis/conga/conga-business-object-api/) — The business object controller
- [Conga Cart Actions API](https://apis.io/apis/conga/conga-cart-actions-api/) — The cart actions controller
- [Conga Cart Items API](https://apis.io/apis/conga/conga-cart-items-api/) — The Cart Item Controller
- [Conga Configuration Management API](https://apis.io/apis/conga/conga-configuration-management-api/) — This class contains APIs related to configuration management
- [Conga Custom Branding API](https://apis.io/apis/conga/conga-custom-branding-api/) — The Custom Branding API from Conga — 3 operation(s) for custom branding.
- [Conga Custom Fields API](https://apis.io/apis/conga/conga-custom-fields-api/) — The Custom Fields API from Conga — 2 operation(s) for custom fields.
- [Conga Customer Registration API](https://apis.io/apis/conga/conga-customer-registration-api/) — The Customer Registration API from Conga — 1 operation(s) for customer registration.
- [Conga Data Management API](https://apis.io/apis/conga/conga-data-management-api/) — The Data Management API from Conga — 2 operation(s) for data management.
- [Conga Document Review API](https://apis.io/apis/conga/conga-document-review-api/) — This class contains API endpoints for Document Review.
- [Conga Job Status API](https://apis.io/apis/conga/conga-job-status-api/) — API to return job status details
- [Conga Password Policy API](https://apis.io/apis/conga/conga-password-policy-api/) — The Password Policy API from Conga — 1 operation(s) for password policy.
- [Conga Review Sites API](https://apis.io/apis/conga/conga-review-sites-api/) — Review Site APIs
- [Conga Schema Metadata API](https://apis.io/apis/conga/conga-schema-metadata-api/) — This class contains APIs for Schema metadata.
- [Conga Search Filters API](https://apis.io/apis/conga/conga-search-filters-api/) — The Search Filters API from Conga — 5 operation(s) for search filters.
- [Conga Smart Search API](https://apis.io/apis/conga/conga-smart-search-api/) — Search APIs to search product details
- [Conga System Properties API](https://apis.io/apis/conga/conga-system-properties-api/) — The System Properties API from Conga — 5 operation(s) for system properties.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Conga Webhooks](https://apis.io/asyncapis/conga/conga-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Conga Advantage Platform MCP Server](https://apis.io/servers/conga/conga-advantage-platform-mcp-server/)

#### Collections (1)

Postman and Open Collection request collections.

- [Open Conga Openapi Index](https://apis.io/collections/conga/open-conga-openapi-index/)

#### Overlays (344)

OpenAPI overlays, including conversational phrasing for each operation.

- [Conga 2 Order Actions Api Phrasing Overlay](https://apis.io/overlays/conga/conga-2-order-actions-api-phrasing-overlay/)
- [Conga 3 Order Line Items Api Phrasing Overlay](https://apis.io/overlays/conga/conga-3-order-line-items-api-phrasing-overlay/)
- [Conga Account Api Phrasing Overlay](https://apis.io/overlays/conga/conga-account-api-phrasing-overlay/)
- [Conga Account Roles Api Phrasing Overlay](https://apis.io/overlays/conga/conga-account-roles-api-phrasing-overlay/)
- [Conga Account Settings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-account-settings-api-phrasing-overlay/)
- [Conga Accountattachmentsblacklist Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountattachmentsblacklist-api-phrasing-overlay/)
- [Conga Accountattachmentswhitelist Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountattachmentswhitelist-api-phrasing-overlay/)
- [Conga Accountdesignersettings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountdesignersettings-api-phrasing-overlay/)
- [Conga Accountemailremindersettings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountemailremindersettings-api-phrasing-overlay/)
- [Conga Accountfeaturesettings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountfeaturesettings-api-phrasing-overlay/)
- [Conga Accountpackagesettings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountpackagesettings-api-phrasing-overlay/)
- [Conga Accounts Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accounts-api-phrasing-overlay/)
- [Conga Accountsigninglogos Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountsigninglogos-api-phrasing-overlay/)
- [Conga Accountsigningtheme Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountsigningtheme-api-phrasing-overlay/)
- [Conga Accountsigninguioptions Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountsigninguioptions-api-phrasing-overlay/)
- [Conga Accountsupportedlanguages Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountsupportedlanguages-api-phrasing-overlay/)
- [Conga Accountsystemsettings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-accountsystemsettings-api-phrasing-overlay/)
- [Conga Action Permissions Api Phrasing Overlay](https://apis.io/overlays/conga/conga-action-permissions-api-phrasing-overlay/)
- [Conga Activities Api Phrasing Overlay](https://apis.io/overlays/conga/conga-activities-api-phrasing-overlay/)
- [Conga Activityhistory Api Phrasing Overlay](https://apis.io/overlays/conga/conga-activityhistory-api-phrasing-overlay/)
- [Conga Adhocgroups Api Phrasing Overlay](https://apis.io/overlays/conga/conga-adhocgroups-api-phrasing-overlay/)
- [Conga Adhocprocess Api Phrasing Overlay](https://apis.io/overlays/conga/conga-adhocprocess-api-phrasing-overlay/)
- [Conga Adjustments Api Phrasing Overlay](https://apis.io/overlays/conga/conga-adjustments-api-phrasing-overlay/)
- [Conga Admin Permissions Api Phrasing Overlay](https://apis.io/overlays/conga/conga-admin-permissions-api-phrasing-overlay/)
- [Conga Admin Settings Api Phrasing Overlay](https://apis.io/overlays/conga/conga-admin-settings-api-phrasing-overlay/)
- …and 319 more published on APIs.io

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Conga Authentication](https://apis.io/security/conga/conga-authentication/)
- [Conga Domain Security](https://apis.io/security/conga/conga-domain-security/)
- [Conga Trust Center](https://apis.io/security/conga/conga-trust-center/)
- [Conga Vulnerability Disclosure](https://apis.io/security/conga/conga-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Conga Scopes](https://apis.io/scopes/conga/conga-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Conga Plans Pricing](https://apis.io/plans/conga/conga-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Conga Rate Limits](https://apis.io/rate-limits/conga/conga-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.conga.com/)
- [Documentation](https://documentation.conga.com/)
- [Getting started](https://developer.conga.com/revenue/docs/user-authentication-to-conga-platform)
- [API reference](https://developer.conga.com/platform/reference)
- [Pricing](https://conga.com/pricing)
- [Support](https://conga.com/support)
- [Blog](https://conga.com/resources/blog)
- [Security](https://conga.com/vulnerability-disclosure)
- [Compliance](https://conga.com/trust-compliance-center)
- [Terms of service](https://conga.com/legal/terms-and-conditions)
- [Privacy policy](https://conga.com/privacy)
- [Status](https://status.conga.com/)

## API Evangelist rating

**Kin Score 68.6** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 60.9 |
| Contract governance | 18.2 |
| Operational transparency | 71.1 |
| Developer ergonomics | 66.1 |
| Access clarity | 53.9 |

**Agent readiness 48.7** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 45.1** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/conga/](https://apis.io/providers/conga/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Conga: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/conga/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
