---
description: >-
  Explore the consented, scaled, and specialized signals behind Dstillery
  audiences.
icon: satellite-dish
---

# Our data sources

{% hint style="success" %}
Dstillery combines consented journeys, website activity, and specialized partner signals.
{% endhint %}

### The core data layer

{% columns %}
{% column %}
#### Learn from consented journeys

**Opted-in panel data**

About **2 million fully consented users** reveal the journeys behind decisions. This data trains the model. It never targets people directly.
{% endcolumn %}

{% column %}
#### Recognize patterns at scale

**Website visitation data**

Web and mobile activity across about **400 million devices** makes learned patterns actionable. It comes from bidstream partners and web publishing tools.
{% endcolumn %}
{% endcolumns %}

See [dstillery-data-and-ds-1-how-they-fit-together.md](dstillery-data-and-ds-1-how-they-fit-together.md "mention") for the complete flow.

### Data sources

#### Opted-in panel data

Panel partners provide fully consented data from participants. Their browsing journeys show the research and comparison patterns that lead to an outcome.

The model learns sequences, not isolated clicks. It recognizes the difference between casual interest and meaningful consideration.

#### Website visitation data

Website visitation data provides the reach layer. It is sourced through SSPs, exchanges, and web publishing tools, including ad, commenting, and sharing widgets.

This dataset captures billions of daily events. It shows where comparable intent appears across the open web.

#### Specialized partner data

Specialized partners add depth for distinct campaign needs:

* **NielsenIQ/GfK** supports CPG and auto use cases.
* **PurpleLab** supports healthcare use cases.
* **ScreenEngine** supports media and entertainment use cases.
* **Resonate** supports consumer insights.
* **Emporia** supports B2B use cases.

These signals add context to the core datasets. See [how-our-multimodal-ai-works.md](how-our-multimodal-ai-works.md "mention") for the full model.

### Audience inputs

DS-1 can begin with the signal you already have:

* First-party data
* A domain
* Search terms or keywords
* Behavioral signals
* Retail purchase intent

These inputs seed custom audiences. The model identifies related patterns for activation.

### How audiences refresh

{% stepper %}
{% step %}
The model identifies behavior patterns associated with an outcome.
{% endstep %}

{% step %}
Website visitation data identifies devices showing similar behavior.
{% endstep %}

{% step %}
Each device is rescored against the model every 24 hours.
{% endstep %}
{% endstepper %}

### Data principles

{% hint style="success" %}
**Built for your brand.** Each campaign uses a custom model, not a generic shared model.

**Current by design.** Custom audiences refresh every 24 hours.

**Tuned for performance and scale.** Audiences are ranked against Dstillery’s device universe for campaign goals.
{% endhint %}

### Responsible data use

Dstillery uses data to model intent, not to target a known individual.

Learn more in [privacy-and-data.md](../../ds-1-foundations/privacy-and-data.md "mention").

Read [privacy-and-data.md](../../ds-1-foundations/privacy-and-data.md "mention") for data handling and privacy practices.
