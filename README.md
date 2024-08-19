# Azure-Active-Directory
Comprehensive guide for setting up and managing Microsoft Entra ID (formerly Azure AD), including integration with on-premises AD, user management, and advanced security features. Ideal for IT administrators and cloud architects.

# Microsoft Entra ID Setup Guide

This guide provides a step-by-step process to set up and manage Microsoft Entra ID (formerly Azure Active Directory). By following these instructions, you will establish a secure and scalable identity and access management system for your organization.

## Table of Contents
1. [Step 1: Login to Azure Portal](#step-1-login-to-azure-portal)
2. [Step 2: Create a New Microsoft Entra ID Tenant](#step-2-create-a-new-microsoft-entra-id-tenant)
3. [Step 3: Manage Users and Groups](#step-3-manage-users-and-groups)
4. [Step 4: Integrate On-Premises AD with Microsoft Entra ID (Optional)](#step-4-integrate-on-premises-ad-with-microsoft-entra-id-optional)
5. [Step 5: Configure Security Features](#step-5-configure-security-features)
6. [Step 6: Monitor and Audit Microsoft Entra ID](#step-6-monitor-and-audit-microsoft-entra-id)
7. [Step 7: Assign Roles and Permissions](#step-7-assign-roles-and-permissions)
8. [Step 8: Stay Updated and Maintain Your Environment](#step-8-stay-updated-and-maintain-your-environment)

---

## Step 1: Login to Azure Portal

Log in to the [Azure portal](https://portal.azure.com/) using your credentials.

---

## Step 2: Create a New Microsoft Entra ID Tenant

1. **Navigate to Microsoft Entra ID**:
    - Click the **Menu** (three horizontal lines) or the **Home** icon to find **Microsoft Entra ID** in the sidebar.
  
      ![image](https://github.com/user-attachments/assets/eba1155d-877c-4389-84dc-e51b00cda607)

    - Alternatively, search for "Microsoft Entra ID" in the Azure portal search bar.
  
     ![image](https://github.com/user-attachments/assets/ad1805e1-2f43-498c-8c4b-061b750d2836)
 

2. **Create a New Tenant**:
    - Select **Create a tenant**.
    - Choose **Azure Active Directory** as the type.
    - Click **Next: Configuration**.


![image](https://github.com/user-attachments/assets/e0347b8e-0eca-47b7-97e3-b6c3fc15d10d)

3. **Configure Your Tenant**:
    - **Organization Name**: Enter a name for your directory.
    - **Initial Domain Name**: Specify a domain name (e.g., `mycompany.onmicrosoft.com`).
    - **Country/Region**: Select the appropriate country.
    - Click **Review + Create**, then click **Create**.

![image](https://github.com/user-attachments/assets/f09a8a7b-8ab7-456b-8809-681b6e281931)

---

## Step 3: Manage Users and Groups

### Add Users

1. **In your Microsoft Entra ID tenant, go to Users**:
    - Click **New user** and enter the required details, including username and password.
    - Click **Create**.

![image](https://github.com/user-attachments/assets/e06ecfa5-6068-4c24-88ce-ad78e82e6b85)


2. **Invite External Users (Guests) - Optional**:
    - For B2B collaboration, you can invite external users.
    - Click **New user > Invite external user**.
    - Provide the user’s email, configure their role, and send the invite.

### Create Groups

1. **Go to Groups**:
    - Click **New group**.
  
      ![image](https://github.com/user-attachments/assets/171a1d63-7bfc-4709-a430-a045d464cf68)


    - Choose the type (e.g., Security group), and enter a name and description.
    - Add members, then click **Create**.
      
![image](https://github.com/user-attachments/assets/11eefe2b-544e-4a8f-8de6-56fa23701f3c)


---

## Step 4: Integrate On-Premises AD with Microsoft Entra ID (Optional)

If you have an on-premises Active Directory and want to sync it with Microsoft Entra ID, follow these steps:

### Install Azure AD Connect

1. **Download the Azure AD Connect tool from the Azure portal**.
2. **Install the tool on your on-premises server**.

### Configure Azure AD Connect

1. During setup, choose the **Express Settings** for a simple configuration or **Customize** for more control.
2. Enter your Azure AD and on-premises AD credentials.
3. Configure synchronization options (e.g., Password Sync, Federation).
4. Finish the setup and start the initial sync.

### Verify Sync

1. After syncing, verify that users from on-premises AD are now visible in Microsoft Entra ID under Users.

---

## Step 5: Configure Security Features

### Set Up Multi-Factor Authentication (MFA)

1. In Microsoft Entra ID, go to **Security > Manage > Authentication methods**.
2. Enable and configure MFA settings as required.

   ![image](https://github.com/user-attachments/assets/45cd539a-f2d3-4ef6-aa53-f7c8aa321a1c)


### Configure Conditional Access Policies

1. Under **Security > Protect > Conditional Access**.
2. Create policies based on conditions such as location, device compliance, etc.
3. Define controls like MFA, block access, or allow access with restrictions.

![image](https://github.com/user-attachments/assets/98841611-e07d-448e-841d-6bf7d20d93d7)


---

## Step 6: Monitor and Audit Microsoft Entra ID

### Sign-In Monitoring

1. **View Sign-In Logs**:
    - Go to **Monitoring > Sign-ins**.
    - Review detailed sign-in logs, including successful and failed sign-ins, MFA challenges, and suspicious activities.

![image](https://github.com/user-attachments/assets/e26776e3-8983-4127-906e-14e7abe268ad)



### Audit Logs

1. **Access Audit Logs**:
    - Navigate to **Monitoring > Audit logs** to track changes within the Microsoft Entra ID environment.
    - This includes activities like user creation, group changes, and policy updates.

2. **Export Logs**:
    - Logs can be exported for compliance and further analysis.
    - Use **Azure Monitor** and **Log Analytics** for more advanced monitoring and alerting.


![image](https://github.com/user-attachments/assets/45f6a530-5f65-45fb-9c07-cacbb4425054)



---

## Step 7: Assign Roles and Permissions

1. **Assign Roles**:
    - In the **Users** section, select a user and go to **Roles and administrators**.
  
      ![image](https://github.com/user-attachments/assets/a183501a-dddd-4452-a2fa-2d0c1ae53622)


    - Assign appropriate roles like Global Administrator, User Administrator, etc.
  
      ![image](https://github.com/user-attachments/assets/2cb77cd8-7f9c-455f-b227-3e8617df3b2b)



---

## Step 8: Stay Updated and Maintain Your Environment

### Regular Updates

- Staying informed about updates and new features in Microsoft Entra ID is paramount.
- Regularly review and update security settings and policies.

### Training and Documentation

- Explore **Microsoft Learn** for tutorials and best practices.
- Utilize official documentation for detailed guidance on advanced configurations.

---

By following these steps, you can set up and manage a robust identity and access management system using Microsoft Entra ID, ensuring your organization’s security and compliance needs are met while maintaining flexibility and scalability.

---

## Contributing

Contributions to this repository are welcome. Please submit a pull request with your changes or open an issue to discuss any improvements or suggestions.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
