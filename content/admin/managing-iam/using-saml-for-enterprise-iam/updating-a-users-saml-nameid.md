---
title: Updating a user's SAML NameID
shortTitle: Update SAML NameID
intro: 'When an account''s `NameID` changes on your identity provider (IdP) and the person can no longer sign into {% data variables.location.product_location %}, you must update the `NameID` mapping on {% data variables.location.product_location %}.'
versions:
  ghes: '*'
type: how_to
topics:
  - Accounts
  - Authentication
  - Enterprise
  - Identity
  - SSO
redirect_from:
  - /admin/identity-and-access-management/using-saml-for-enterprise-iam/updating-a-users-saml-nameid
---

## About updates to users' SAML `NameID`

In some situations, you may need to update values associated with a person's account on your SAML IdP. If that identifier is also the `NameID` that you use for authentication on {% data variables.product.github %}, you must update the `NameID` mapping on your instance so the person can continue to authenticate successfully. For more information, see [AUTOTITLE](/admin/identity-and-access-management/managing-iam-for-your-enterprise/username-considerations-for-external-authentication).

To update user SAML `NameID` mappings in bulk, you can use the `ghe-saml-mapping-csv` command. For more information, see [AUTOTITLE](/admin/administering-your-instance/administering-your-instance-from-the-command-line/command-line-utilities#ghe-saml-mapping-csv).

{% ifversion scim-for-ghes-ga %}
When SCIM is enabled on your {% data variables.product.prodname_ghe_server %} instance, you cannot update user SAML `NameID` mappings.
{% endif %}

## Updating a user's SAML `NameID`

Enterprise owners can update a user's SAML `NameID` on a {% data variables.product.github %} instance.

{% data reusables.enterprise_site_admin_settings.access-settings %}
1. In the left sidebar, click **All users**.
1. In the list of users, click the username you'd like to update the `NameID` mapping for.
{% data reusables.enterprise_site_admin_settings.security-tab %}
1. To the right of "Update SAML NameID", click **Edit** .
1. In the "NameID" field, type the new `NameID` for the user.
1. Click **Update NameID**.
