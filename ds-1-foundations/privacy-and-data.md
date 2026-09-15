---
description: How DS-1 handles your data, keeps it secure, and protects user privacy.
icon: lock
---

# Privacy and data

### What it is

{% hint style="info" %}
An overview of how DS-1 and Dstillery handles data, model architecture, retention, security, and compliance, along with guardrails around sensitive category targeting.
{% endhint %}

***

### Data handling

* Every DS-1 interaction is stored, used both for QA and core app functionality
* Data within a chat session is retained so DS-1 can understand conversation context
* Chat sessions are also saved for product analytics (e.g. did the user get a proper response, did an error occur)
* Client first party data is strictly sequestered and used exclusively for that client's custom models, never shared or repurposed
* For DS-1 activation workflows, no external partner data is stored or persisted beyond the active session; it's read in-memory and discarded after

### Retention

* Platform generated data is stored in its original form for up to 30 days, then deleted
* A de-identified version of that data is retained for up to two years; pseudonymous data may be retained up to one year for research
* Non-PII stored in cookies expires no later than 60 days from last device encounter
* DS-1 conversation data itself is currently retained indefinitely

### Access controls

* Access is governed by Role Based Access Control (RBAC), following least privilege
* Client facing teams (Sales, Account Management) access campaign data and performance metrics only
* Data Science and Engineering access raw data for model building and troubleshooting
* All access requires multi-factor authentication (MFA) through a zero trust network
* Access control configurations are managed as code, peer reviewed, and regularly audited

### Client data isolation

* Client data is logically separated and independently secured, with unique identifiers per client to prevent commingling
* Isolation is maintained through the full data lifecycle, from ingestion through processing and storage
* Reviewed annually as part of Dstillery's SOC 2 audit
* Client specific models operate on a zero trust, logically separated basis within a secure network; all data is encrypted in transit and at rest (AES-256 at rest)

### AI models and architecture

* DS-1 runs a pre-trained Google or Anthropic foundation model, with no fine-tuning or custom weights
* Capabilities come from prompt engineering and tool definition, not model training; the model is used for inference only
* A 0-day retention agreement is in place with the model provider
* No client or partner data is used to train or update Dstillery's global models or parameters; any client specific model training (e.g. joining client data with Dstillery data) is scoped exclusively to that client
* Prompts are version controlled in git and go through PR review; model upgrades are evaluated against internal benchmarks before shipping
* Generative AI is not used in model outputs. It may be used narrowly to help select or refine seed URLs during pre-campaign modeling, based on their position in text embedding space
* Underlying models are predictive (supervised machine learning), not generative, limiting unintended output behavior. Outputs are limited to a score or probability tied to conversion propensity for specific ad inventory

### Human oversight

* Every session is user directed; before any activation action executes, DS-1 presents the proposed action and waits for explicit confirmation
* All interactions are logged for monitoring
* An AI Governance Committee reviews models for fairness, bias, and performance before deployment
* Models are trained exclusively on URL level visit and conversion data. No demographic, behavioral, or sensitive attributes are collected, inferred, or provided to any model

### Security and monitoring

* LangSmith is used for tracing and observability across agent interactions, alongside manual log review
* MCP integrations are scoped to explicit tool schemas; agents cannot execute arbitrary operations
* Internal and external networks are separated by firewalls, with regular internal and external vulnerability scanning
* Dstillery maintains a formal Information Security Program (WISP) with regular employee security training
* Dstillery's Information Security Committee conducts annual formal risk assessments, with findings reported to the CEO and quarterly updates to the Board

***

### Data subject rights

* Individuals can submit Data Subject Access Requests (DSARs) for access, correction, or deletion through Dstillery's privacy page, managed via OneTrust
* Opt-out requests are honored by removing the individual's data from Dstillery systems and excluding them from downstream partner data sharing

### Incident response

* Real-time monitoring detects incidents; any incident involving personal data escalates immediately to the Data Protection Officer and Privacy Team
* Clients are notified of a Reportable Incident within 48 hours
* Clients retain sole authority over whether to notify individuals or regulators; Dstillery will not notify third parties without written client consent, unless legally required

### Sensitive category guardrails

{% hint style="warning" %}
Dstillery maintains a Sensitive Categories Policy governing how sensitive characteristics can and cannot be used in targeting:
{% endhint %}

1. Dstillery does not offer ID-based targeting products for sensitive categories. Custom AI and Custom Built user-based audiences will not be built around sensitive characteristics, and the standard prebuilt taxonomy does not include segments related to sensitive categories. Prebuilt segments may still be applied to any campaign where they're deemed relevant.
2. Dstillery has a review and approval process for targeting sensitive categories using products built with ID-free® Technology and activated via PMP or Custom Bidding Algorithm. This includes ID-free® Custom Built (seeded with domains) and Custom Search Lookalikes (seeded with search terms). Dstillery will not build ID-free Custom AI® targeting models seeded with first party data.
3. Sales or customer success representatives must submit a written request for approval on behalf of clients wishing to target sensitive categories.
4. Dstillery is committed to ongoing review of these policies beyond legal requirements. Approval standards are inherently subjective and will evolve over time, incorporating ethical judgment and Dstillery's comfort level based on the nature of each use case.

***

### Further reading

* Dstillery Trust Page: [https://dstillery.com/client-trust/](https://dstillery.com/client-trust/)
* Dstillery Privacy Policy: [https://dstillery.com/privacy-policy/](https://dstillery.com/privacy-policy/)
