<!-- loioc6dd6a5f141f4df0ae93b98904014e17 -->

# Configure Login Hint Parameter

Tenant administrator can configure the login hint parameter via the administration console for Identity Authentication.



## Context

The configuration of the login hint parameter affects the following scenarios:

-   Identity Authentication acting as proxy to delegate authentication to an external corporate identity provider \(IdP\). The user is authenticated via that corporate identity provider.
-   Identity Authentication acting as a conditional proxy where an external corporate identity provider is configured to be used as an authenticating IdP under certain conditions.

The login hint parameter helps the user when he or she is known to the service provider \(SP\) or relying party. Thus it prevents the user from re-typing the user identifier on the logon. If the corporate IdP supports the login hint parameter, then it requests only the user credentials.

If the corporate IdP does not support the login hint parameter, it requires both the user identifier and password. You can configure the login hint parameter for corporate IdP via the administration console for Identity Authentication.

There are two aspects in the configuration of the login hint parameter: the value of the parameter, and how it is sent to the corporate IdP. The *How it is sent to the corporate IdP* configuration is only relevant for SAML 2.0 corporate identity ptoviders and depends on the *Value* configuration:

<a name="loioc6dd6a5f141f4df0ae93b98904014e17__table_f3z_fst_tqb"/>Configuration Options


<table>
<tr>
<th valign="top">

Value



</th>
<th valign="top">

How it is sent to the corporate IdP



</th>
</tr>
<tr>
<td valign="top">

User Input



</td>
<td valign="top">

-   Login Hint URL parameter - the login hint is sent in the URL as `login_hint parameter`
-   Authentication Request - the login hint is sent in the SAML 2.0 authentication request as <`Subject`\> attribute \(for SAML 2.0 only\)



</td>
</tr>
<tr>
<td valign="top">

None



</td>
<td valign="top">

no login hint parameter is sent



</td>
</tr>
<tr>
<td valign="top">

User Attributes

-   Login Name
-   E-Mail



</td>
<td valign="top">

-   Login Hint URL parameter - the login hint is sent in the URL as `login_hint parameter`
-   Authentication Request - the login hint is sent in the SAML 2.0 authentication request as <`Subject`\> attribute \(for SAML 2.0 only\)



</td>
</tr>
</table>

> ### Note:  
> The *User Input* is the default value option.
> 
> The *User Attributes* option is valid only for users that exist in the Identity Authentication local user store. If the user is missing the specified attribute in the configuration, then login hint parameter will not be sent to the corporate IdP.
> 
> If the user does not exist in Identity Authentication local user store, then the User Input will be sent as login hint to the corporate IdP.



## Procedure

1.  Access the tenant's administration console for Identity Authentication by using the console's URL.

    > ### Note:  
    > The URL has the following pattern:
    > 
    > `https://<tenant ID>.accounts.ondemand.com/admin`
    > 
    > *Tenant ID* is an automatically generated ID by the system. The first administrator created for the tenant receives an activation e-mail with a URL in it. This URL contains the *tenant ID*. For more information about your tenants, see [Viewing Assigned Tenants and Administrators](../viewing-assigned-tenants-and-administrators-f56e6f2.md).
    > 
    > If you have a configured custom domain, the URL has the following pattern: `<your custom domain>/admin`.

2.  Under *Identity Providers*, choose the *Corporate Identity Providers* tile.

3.  Select the corporate identity provider that you want to configure.

    > ### Tip:  
    > If you need to change the protocol, see [Choose Identity Provider Type](choose-identity-provider-type-0838379.md)..

4.  Set a value for the login hint parameter:

    -   User Input
    -   None
    -   User Attribute \(local users only\)

5.  \(For SAML 2.0 providers only\) Set how the login hint parameter should be sent to the corporate IdP:

    -   *Login Hint URL parameter* -
    -   *Authentication Request*

    > ### Remember:  
    > The options are valid only if *User Input* or *User Attribute \(local users only\)* values are set.

6.  Save your configuration.


