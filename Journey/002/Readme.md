# Creating a User in Azure AD using PowerShell

## Introduction
\
Learn how to create a user in Azure AD.  

## Cloud Research 

#### **What is Azure AD**

Azure Active Directory is Microsoft's cloud based identity and access management service. Its used for employees to sign in and access resources. 

External resources - MS 365, Azure and other SaaS applications. 

Internal resources - Apps on a network or intranet 

#### **Types of license** 
\
There are 4 types of license 
* Azure Active Directory Free  - Provides user and group management , on premise directory sync , basic reports, self servie password change for cloud users , and single sing on across Azure, Microsoft 365 , and mnay other SaaS apps.
* Azure Active Directory Premium P1 - Allows hybrid users to access both on prem and cloud resources. Supports advanced admin , such as dynamic groups , self service group management , Microsoft Identity Manager and cloud write back capabilities , which allow self service password reset for on prem users. 
* Azure Active Directory Premium P2 - Offers AAD Identity Protection to help provide risk based Conditional Access to apps and company data and Privaleged Identity Management to help discover, restrict ,and monitor admin and their access to resources. 
* "Pay as you go" feature licenses - Additional features such as Azure AAD B2C.
  
#### **Identity**
\
Something that gets authenticated. Could be a user with a username and password. Could also be an application or other servers that might need auth through secret keys or certs. 

#### **Azure AD Global Administrator**  
\
This role is auto assigned to whoever created the Azure AD tenant. Global admins can do all of the admin functions for Azure AD and any serices that federate to Azure AD, such as Exchange Online and SPO. You can have multiple Global admins but only Global admins can assign admin roles. 


#### **Azure tenant**
\
A dedicated and trusted instance of Azure AD that is created automatically when an org signs up for a MS cloud service subscription, such as Azure, Intune or 365. An Azure tenant represents a single org.

#### **Differences between Classic subscription administrator roles, Azure roles, and Azure AD roles**
\
![Admin roles image](rbac-admin-roles.png)


## Try yourself

I wanted to create the user using Azure Cloud Shell - PowerShell. Rather than doing it in the portal. 

### Step 1 

Naviate to portal.azure.com

### Step 2
\
Open up Cloud Shell , select PowerShell and run Connect-AzureAd.

### Step 3 
\
Set the Password Profile 

``` 
$PasswordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
```
Set the password 
```
$PasswordProfile.Password = 'Example123!'
```

### Step 4
\
Create the account
```
New-AzureADUser -DisplayName "New User" -PasswordProfile $PasswordProfile -UserPrincipalName "NewUser@yourorg.onmicrosoft.com" -AccountEnabled$True -MailNickName "NewUser"
```

## ☁️ Cloud Outcome

A new Azure AD account is created .

