---
title: Deploy Managed Rulesets for a zone
pcx_content_type: how-to
weight: 5
meta:
  title: Deploy Managed Rulesets for a zone in the dashboard
---

# Deploy Managed Rulesets for a zone in the dashboard

You can enable and configure Managed Rulesets for a zone in **Security** > **WAF** > **Managed rules**.

![Example Managed Rules configuration in the Managed rules tab under Security > WAF. There is a configured rule for executing the Cloudflare Managed Ruleset, and there are two Managed Rulesets available for deployment.](/waf/static/waf-managed-rules-tab.png)

## Deploy a Managed Ruleset

Under **Managed Rulesets**, click **Add** on the right of a Managed Ruleset to deploy the Managed Ruleset for the current zone.

When you deploy a Managed Ruleset, the WAF adds an _Execute_ rule, displayed under **Managed rules**, that deploys the Managed Ruleset.

## Enable or disable a Managed Ruleset

Click the **Enabled** toggle on the right of a Managed Ruleset to enable or disable it.

## Configure a Managed Ruleset

Configure a Managed Ruleset to:

- Define specific field values for one or more rules (for example, configure a rule with an action different from the action configured by Cloudflare)
- Disable one or more rules

To skip one or more rules or WAF Managed Rulesets, [add a WAF exception](/waf/managed-rulesets/waf-exceptions/).

{{<Aside type="note">}}

Some Managed Rulesets may not allow custom configuration, depending on your Cloudflare plan.

{{</Aside>}}

### Configure field values for all the rules

To configure rule field values for all the rules in a Managed Ruleset:

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/), and select your account and website.

2. Go to **Security** > **WAF** > **Managed rules**.

3. On the right of the _Execute_ rule that deploys the Managed Ruleset you want to configure, click **Edit**.

4. Under **Ruleset configuration**, set one or more rule fields from the available values in the drop-down lists.

    For example, select the action to perform for all the rules in the ruleset from the **Ruleset action** drop-down list.

    ![The Configure Managed Ruleset page displaying the available options to override all the rules in the ruleset. In the displayed Managed Ruleset you can override the ruleset action.](/waf/static/waf-configure-ruleset.png)

5. Click **Save**.

### View the rules of a Managed Ruleset

You can browse the available rules in a Managed Ruleset and search for individual rules or tags.

Use the available filters in the Browse Managed Ruleset interface.

To view the rules of a Managed Ruleset:

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/), and select your account and website.

2. Go to **Security** > **WAF** > **Managed rules**.

3. On the right of the _Execute_ rule that deploys the Managed Ruleset you want to browse, click **Edit**.

4. Click **Browse rules**.

    The Browse Managed Ruleset interface displays.

    ![The Browse rules page displaying the list of rules in the Cloudflare Managed Ruleset](/waf/static/waf-browse-rules.png)

### Configure a single rule in a Managed Ruleset

You can configure one or more rules in the Browse Managed Ruleset interface.

Do the following:

1. Search for a rule using the available filters. You can search for tags.

2. Find the rule you want to configure in the results list.

3. In the result line for the rule you want to change, select the desired value for a field in the displayed drop-down lists. For example, select the rule action in the **Action** dropdown.

    In some Managed Rulesets, you can also change the status of a rule using the toggle available on the right.

    ![The Browse rules page displaying the list of rules in the Cloudflare Managed Ruleset. In this interface you can override the behavior of specific rules.](/waf/static/waf-browse-rules.png)

4. Click **Next**.

    The Configure Managed Ruleset interface displays, listing the configuration you just defined.

5. Click **Save**.

### Configure rules in bulk in a Managed Ruleset

You can configure several rules at once in the Browse Managed Ruleset interface.

Do the following:

1. Enter search terms in the available input to find the rules you want to configure. You can search for tags.

    ![Example of filtering rules by the wordpress tag in the Browse rules page](/waf/static/waf-selected-tag.png)

2. In the results list, click the checkbox on the left of all the rules you want to configure.

    Alternatively, click a tag name under the search input to filter the rules with that tag, and then click the checkboxes for the rules you want to configure.

3. Update one or more fields for the selected rules using the drop-down lists displayed in the top right corner of the table.

    ![Selecting all rules in a page displays additional drop-down lists above the table to override the behavior of several rules at once.](/waf/static/waf-modify-selected-rules.png)

4. Click **Next**.

    {{<Aside type="note" header="Note">}}

If you selected a tag, you get a dialog asking you if any new rules with the selected tag should be configured with the field values you selected.

Select **Do not apply to new rules** to apply your configurations to the selected rules only.

Select **Apply to new rules** if you want to apply your configurations to any new rules with the select tag.

    {{</Aside>}}

5. Click **Save**.
