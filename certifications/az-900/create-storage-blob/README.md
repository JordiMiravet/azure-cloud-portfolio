# Create a Storage Blob

## Overview

This lab creates a storage account and a blob container in Azure, uploads an image, and changes the container's anonymous access level to make the file reachable from the internet. It uses the services Resource groups, Storage accounts, and Blob Storage.

Based on the official exercise: [Create a storage blob](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/05-exercise-create-storage-blob.html).

Region used: (Europe) Spain Central.

## Steps

### 1. Create a storage account

1. In the Azure portal, select **Create a resource**, then **Infrastructure services**, and create a **Storage account**.
2. On the **Basics** tab, configure the following settings:

The Basics tab configuration:

| Setting | Value |
|---|---|
| Subscription | XLabs-731 |
| Resource group | `IntroAzureRG` |
| Storage account name | `introazuremiravet` |
| Region | Spain Central |
| Primary service | Azure Blob Storage or Azure Data Lake Storage |
| Primary workload | Not specified |
| Performance | Standard |
| Replication | Locally redundant storage (LRS) |

The Advanced tab configuration:

| Setting | Value |
|---|---|
| Enable hierarchical namespace | Disabled |
| Enable SFTP | Disabled |
| Enable network file system v3 | Disabled |
| Allow cross-tenant replication | Disabled |
| Access tier | Hot |
| Managed Identity for SMB | Disabled |
| Require Encryption in Transit for SMB | Enabled |

The Networking tab configuration:

| Setting | Value |
|---|---|
| Public network access | Enabled |
| Public network access scope | Enabled from all networks |
| Default routing tier | Microsoft network routing |

The Data protection tab configuration:

| Setting | Value |
|---|---|
| Point-in-time restore | Disabled |
| Blob soft delete | Enabled |
| Blob retainment period in days | 7 |
| Container soft delete | Enabled |
| Container retainment period in days | 7 |
| Classic file share soft delete | Enabled |
| Classic file share retainment period in days | 7 |
| Versioning | Disabled |
| Blob change feed | Disabled |
| Version-level immutability support | Disabled |

The Security tab configuration:

| Setting | Value |
|---|---|
| Secure transfer | Enabled |
| Blob anonymous access | Enabled |
| Allow storage account key access | Enabled |
| Default to Microsoft Entra authorization in the Azure portal | Disabled |
| Minimum TLS version | Version 1.2 |
| Permitted scope for copy operations (Preview) | From any storage account |
| Enable Defender for Storage | Disabled |

The Encryption tab configuration:

| Setting | Value |
|---|---|
| Encryption type | Microsoft-managed keys (MMK) |
| Enable support for customer-managed keys | Blobs and files only |
| Enable infrastructure encryption | Disabled |

3. On the **Advanced** tab, check **Allow enabling anonymous access on individual containers**.
4. Select **Review + create** and then **Create**, wait for the deployment to finish, and select **Go to resource**.

### 2. Create a container and upload a file

1. Under **Data storage**, select **Containers** and then **+ Add container**.
2. Enter a name for the container, keep the anonymous access level as **Private (no anonymous access)**, and select **Create**.
3. Open the container, select **Upload**, and upload an image from the computer.

The container created with private access:

![Container created](assets/screenshots/03-container-created.png)

The image uploaded to the container:

![Blob uploaded](assets/screenshots/04-blob-uploaded.png)

### 3. Try to access the blob while the container is private

1. Select the uploaded blob and copy its URL from the **Properties** tab.
2. Open the URL in a new browser tab.
3. The request fails with this error: TODO exact error shown. The container does not allow anonymous access yet.

![Access denied to the blob](assets/screenshots/05-blob-access-denied.png)

### 4. Change the access level

1. Go back to the container and select **Change access level**.
2. Set the anonymous access level to **Blob (anonymous read access for blobs only)** and select **OK**.
3. Refresh the tab with the blob URL.

The access level change:

![Change access level](assets/screenshots/06-change-access-level.png)

The blob is now accessible from the internet:

![Blob accessible](assets/screenshots/07-blob-access-allowed.png)

### 5. Clean up

1. In the Azure portal, open **Resource groups** and select `IntroAzureRG`.
2. Select **Delete resource group**.
3. Type `IntroAzureRG` to confirm and select **Delete**, then confirm in the pop-up window.

Deleting the resource group removes the storage account and everything stored in it.

![Resource group deleted](assets/screenshots/08-resource-group-deleted.png)

## Result

Before changing the access level, the blob URL returned an error. After setting the container's anonymous access level to **Blob**, the same URL displayed the uploaded image.

## Lessons Learned

- A storage account is the top-level resource for Azure Storage. Blobs live inside containers, and containers live inside the account.
- Containers are private by default: a blob cannot be reached through its URL until anonymous access is allowed.
- Anonymous access has to be enabled on the storage account before it can be configured on a container.
- The access level is set per container. The **Blob** level allows reading individual blobs by their URL, but not listing the container's contents.
- Anonymous access exposes files to the whole internet, so it should only be used for content meant to be public.
- Deleting the resource group removes the storage account and avoids leaving resources behind.

## References

- [Official AZ-900 lab instructions - Create a storage blob](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/05-exercise-create-storage-blob.html)
- [Introduction to Azure Blob Storage](https://learn.microsoft.com/azure/storage/blobs/storage-blobs-introduction)
- [Configure anonymous read access for containers and blobs](https://learn.microsoft.com/azure/storage/blobs/anonymous-read-access-configure)
