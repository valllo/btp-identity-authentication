<!-- loio626b17331b4d4014b8790d3aea70b240 -->

# Integrating the Service with Microsoft Azure AD

Identity Authentication is part of the application gallery of Microsoft Azure Active Directory \(Azure AD\) under the name Identity Authentication.

This integration aims to provide single sign-on \(SSO\) between applications using Azure AD as authenticating identity provider and applications using Identity Authentication as proxy identity provider.



## Prerequisites

-   You have a valid Azure AD subscription.
-   You have a subscription for Identity Authentication. For more information how to get Identity Authentication, see [Initial Setup](../initial-setup-31af7da.md).



## Overview

In this scenario Identity Authentication acts as a proxy identity provider and Azure AD as the main authentication authority for the applications. The authentication requests sent to Identity Authentication are redirected to Azure AD. User management and authentication is done on Azure AD side.

> ### Note:  
> Users who are in the Azure AD user store can use the single sign-on \(SSO\) functionality.
> 
> Users who are provisioned to Identity Authentication, but not to Azure AD, are not able to log on.

> ### Tip:  
> Identity Authentication supports the *Identity Federation* option. This option allows the application to check if the users authenticated by the corporate identity provider exist in the user store of Identity Authentication. In the default setting, the *Identity Federation* option is disabled. If *Identity Federation* is enabled, only the users that are imported in Identity Authentication are able to access the application. For more information about how to enable or disable *Identity Federation* with Identity Authentication, see **Enable Identity Federation with Identity Authentication** in [Configure Identity Federation](../Operation-Guide/configure-identity-federation-c029bbb.md).

For this scenario, the configurations are made in Azure classic portal and in the administration console for Identity Authentication.

**Related Information**  


[Integrating the Service with SAP Business Technology Platform, Neo Environment](integrating-the-service-with-sap-business-technology-platform-neo-environment-fe84459.md#loiofe84459e688c43698591d3b9e1aac828 "SAP BTP acts as a service provider, and Identity Authentication acts as an identity provider in this setup.")

[Integrating the Service with the Identity Service of SAP BTP](integrating-the-service-with-the-identity-service-of-sap-btp-d5cd80c.md "The Identity service of SAP BTP enables you to delegate authentication to the Identity Authentication service. The Identity service automates the creation of OpenID Connect (OIDC) applications for the Identity Authentication service for each application the Identity service registers.")

[Integrating the Service with SAP Web IDE Full-Stack](integrating-the-service-with-sap-web-ide-full-stack-313f545.md#loio313f5456f3ab41ca925d555cda748f39 "You can use Identity Authentication as identity provider for SAP Web IDE Full-Stack.")

[Integrating the Service with SAP Document Center](integrating-the-service-with-sap-document-center-397683c.md#loio397683cff69d44c5bb2b38c76714c6ca "You can use Identity Authentication as identity provider for SAP Document Center.")

[Integrating the Service with SAP Identity Management 8.0](integrating-the-service-with-sap-identity-management-8-0-f44f931.md "")

[Integrating the Service with an ABAP Product and SAP Analytics Cloud](integrating-the-service-with-an-abap-product-and-sap-analytics-cloud-dd61aea.md "This integration document aims to provide information about single sign-on (SSO) options for an ABAP product and SAP Analytics Cloud, that use Identity Authentication as an authenticating or proxy identity provider.")

[Integrating the Service with SAP Task Center](integrating-the-service-with-sap-task-center-ab5e90e.md)

[Blogs](blogs-a89ca3e.md "Links to blogs and documents about integration scenarios with Identity Authentication.")
