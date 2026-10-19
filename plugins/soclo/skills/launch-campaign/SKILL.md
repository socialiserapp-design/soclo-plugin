---
name: launch-campaign
description: Use Soclo when the user wants a connected campaign launch reviewed with exact current targeting, budget and separate spending approval.
---

# Soclo launch-campaign

Read the current /launch-campaign playbook and references/soclo-workflow.md first. Discover owned ad accounts, campaign and saved approved media. For creation, use soclo_ads_create_ad_campaign with a stable requestId and read back the actual provider state. Confirmed creation requests active after exact spend approval; report the returned state and never claim live without confirmed read-back. Reconcile that original operation without another create.

For a supported platform, use soclo_campaign_chat_preview to show the freshly read budget amount/type/currency, provider targeting and approvalHash. Proposed map countries are not proof of live targeting. Read soclo_ads_watch_read. If the owner chooses optional Ads Watch, first show its actual monthlyCredits quote, charged now and every 30 days, and obtain separate explicit owner approval before setting it. Preserve stable original request IDs and the current state hash.

Refresh the launch preview after a settings change. Wait for the owner to approve that exact launch candidate, budget ceiling, currency and confirmed targeting. Only then use the supported confirm contract with unchanged expected fields and approvalHash. Read the provider's final result; unconfirmed is not active. For platforms without this adapter or activation support, explain the tool's actual limitation and hand off to the provider/app rather than substituting an unsupported route. Pause and other changes require a separate owner request; this recipe never grants standing spending authority.
