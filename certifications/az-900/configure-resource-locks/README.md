# Configure Resource Locks

## Overview

This lab applies resource locks to a storage account to see how they protect it from accidental changes and deletion. It tests a read-only lock and a delete lock, and shows that a lock has to be removed before the resource can be deleted. It uses the services Resource groups, Storage accounts, and Resource locks.

Based on the official exercise: [Configure resource locks](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/08-exercise-configure-resource-lock.html).

Region used: TODO region.

## Steps

### 1. Create a resource group and a storage account

1. In the Azure portal, create a resource group named `IntroAzureRG`.
2. Create a storage account in that resource group with a unique name, the same region as the resource group, **Standard** performance, and **Locally redundant storage (LRS)** redundancy. Leave the rest as default.
3. Wait for the deployment to finish and select **Go to resource**.

### 2. Apply a read-only lock

1. In the storage account, open **Settings** > **Locks** and select **+ Add**.
2. Enter a lock name, check that the lock type is **Read-only**, and select **OK**.

![Read-only lock added](assets/screenshots/01-read-only-lock-added.png)
