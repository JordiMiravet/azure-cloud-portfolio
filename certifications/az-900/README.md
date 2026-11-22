# AZ-900 Labs

Hands-on labs for **AZ-900: Microsoft Azure Fundamentals**, based on the official [AZ-900 exercises](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/) from Microsoft Learning.

## Labs

| Lab | Official exercise | My documentation | Status |
| --- | --- | --- | --- |
| Create an Azure resource | [Exercise](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/02-exercise-create-azure-resource.html) | [Documentation](01-create-azure-resource/README.md) | Completed |
| Create a virtual machine and configure it as a web host | [Exercise](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/03-exercise-create-azure-virtual-machine.html) | [Documentation](02-create-virtual-machine/README.md) | Completed |
| Create a storage blob | [Exercise](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/05-exercise-create-storage-blob.html) | [Documentation](03-create-storage-blob/README.md) | Completed |
| Estimate workload costs with the Pricing calculator | [Exercise](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/06-exercise-estimate-workload-costs-use-pricing-calculator.html) | [Documentation](04-estimate-workload-costs/README.md) | Completed |
| Configure resource locks | [Exercise](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/Instructions/Labs/08-exercise-configure-resource-lock.html) | [Documentation](05-configure-resource-locks/README.md) | Completed |

## Adding a New Lab

1. Copy the [`lab-template/`](lab-template/) folder and rename it with the next two-digit number followed by a `kebab-case` name, for example `06-lab-name/`.
2. Fill in its `README.md` following the [Documentation Guide](../../docs/documentation-guide.md).
3. Update the lab's row in the table above with a link to its documentation and its new status.