---
Module Name: Az.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/powershell/module/az.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
ms.openlocfilehash: 4b5000995270d4544b571e825313a2b2203d2247
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902093"
---
# Az.DataLakeStore 模組
## 描述
本節主題將說明 Azure Resource Manager 中 Azure Data Lake Store 的 Azure PowerShell Cmdlet (ARM) 架構。 Cmdlet 存在於 Microsoft.Azure.Commands.DataLakeStore 命名空間中。 這些 Cmdlet 僅適用于 Azure Data Lake Storage Gen1 帳戶。

## Az.DataLakeStore Cmdlets
### [Add-AzDataLakeStoreFirewallRule](Add-AzDataLakeStoreFirewallRule.md)
新增防火牆規則至指定的 Data Lake Store 帳戶。

### [Add-AzDataLakeStoreItemContent](Add-AzDataLakeStoreItemContent.md)
新增內容至 Data Lake Store 中的專案。

### [Add-AzDataLakeStoreTrustedIdProvider](Add-AzDataLakeStoreTrustedIdProvider.md)
將信任的身分識別提供者新增到指定的 Data Lake Store 帳戶。

### [Add-AzDataLakeStoreVirtualNetworkRule](Add-AzDataLakeStoreVirtualNetworkRule.md)
新增虛擬網路規則至指定的 Data Lake Store 帳戶。

### [Enable-AzDataLakeStoreKeyVault](Enable-AzDataLakeStoreKeyVault.md)
嘗試啟用使用者管理的金鑰保存庫，以加密指定的 Data Lake Store 帳戶。

### [Export-AzDataLakeStoreChildItemProperty](Export-AzDataLakeStoreChildItemProperty.md)
匯出 (磁片使用量和 Acl) 從指定路徑匯出至輸出路徑的整個樹狀結構

### [Export-AzDataLakeStoreItem](Export-AzDataLakeStoreItem.md)
從 Data Lake Store 下載檔案。

### [Get-AzDataLakeStoreAccount](Get-AzDataLakeStoreAccount.md)
獲得 Data Lake Store 帳戶的詳細資訊。

### [Get-AzDataLakeStoreChildItem](Get-AzDataLakeStoreChildItem.md)
在 Data Lake Store 中，在資料夾中獲得專案清單。

### [Get-AzDataLakeStoreChildItemSummary](Get-AzDataLakeStoreChildItemSummary.md)
獲得指定路徑中包含的總大小、檔案和目錄摘要

### [Get-AzDataLakeStoreFirewallRule](Get-AzDataLakeStoreFirewallRule.md)
在指定的 Data Lake Store 中，獲得指定的防火牆規則。
如果沒有指定防火牆規則，請列出帳戶的所有防火牆規則。

### [Get-AzDataLakeStoreItem](Get-AzDataLakeStoreItem.md)
在 Data Lake Store 中，獲得檔案或資料夾的詳細資訊。

### [Get-AzDataLakeStoreItemAclEntry](Get-AzDataLakeStoreItemAclEntry.md)
在 Data Lake Store 中，在檔案或資料夾的 ACL 中輸入專案。

### [Get-AzDataLakeStoreItemContent](Get-AzDataLakeStoreItemContent.md)
在 Data Lake Store 中獲取檔案的內容。

### [Get-AzDataLakeStoreItemOwner](Get-AzDataLakeStoreItemOwner.md)
在 Data Lake Store 中，獲得檔案或資料夾的擁有者。

### [Get-AzDataLakeStoreItemPermission](Get-AzDataLakeStoreItemPermission.md)
在 Data Lake Store 中獲得檔案或資料夾的許可權八進位。

### [Get-AzDataLakeStoreTrustedIdProvider](Get-AzDataLakeStoreTrustedIdProvider.md)
在指定的 Data Lake Store 中，獲得指定的信任身分識別提供者。
如果沒有指定提供者，請列出帳戶的所有提供者。

### [Get-AzDataLakeStoreVirtualNetworkRule](Get-AzDataLakeStoreVirtualNetworkRule.md)
在指定的 Data Lake Store 中，獲得指定的虛擬網路規則。
如果沒有指定虛擬網路規則，請列出帳戶的所有虛擬網路規則。

### [Import-AzDataLakeStoreItem](Import-AzDataLakeStoreItem.md)
將本地檔案或目錄上傳到 Data Lake Store。

### [Join-AzDataLakeStoreItem](Join-AzDataLakeStoreItem.md)
加入一或多個檔案，在 Data Lake Store 中建立一個檔案。

### [Move-AzDataLakeStoreItem](Move-AzDataLakeStoreItem.md)
在 Data Lake Store 中移動或重新命名檔案或資料夾。

### [New-AzDataLakeStoreAccount](New-AzDataLakeStoreAccount.md)
建立新 Data Lake Store 帳戶。

### [New-AzDataLakeStoreItem](New-AzDataLakeStoreItem.md)
在 Data Lake Store 中建立新檔案或資料夾。

### [Remove-AzDataLakeStoreAccount](Remove-AzDataLakeStoreAccount.md)
永久刪除 Data Lake Store 帳戶。

### [Remove-AzDataLakeStoreFirewallRule](Remove-AzDataLakeStoreFirewallRule.md)
移除指定 Data Lake Store 中指定的防火牆規則。

### [Remove-AzDataLakeStoreItem](Remove-AzDataLakeStoreItem.md)
刪除 Data Lake Store 中的檔案或資料夾。

### [Remove-AzDataLakeStoreItemAcl](Remove-AzDataLakeStoreItemAcl.md)
清除 Data Lake Store 中檔案或資料夾的 ACL。

### [Remove-AzDataLakeStoreItemAclEntry](Remove-AzDataLakeStoreItemAclEntry.md)
從 Data Lake Store 中檔案或資料夾的 ACL 移除專案。

### [Remove-AzDataLakeStoreTrustedIdProvider](Remove-AzDataLakeStoreTrustedIdProvider.md)
移除指定 Data Lake Store 中指定的信任身分識別提供者。

### [Remove-AzDataLakeStoreVirtualNetworkRule](Remove-AzDataLakeStoreVirtualNetworkRule.md)
移除指定 Data Lake Store 中指定的虛擬網路規則。

### [Set-AzDataLakeStoreAccount](Set-AzDataLakeStoreAccount.md)
修改 Data Lake Store 帳戶。

### [Set-AzDataLakeStoreFirewallRule](Set-AzDataLakeStoreFirewallRule.md)
修改指定 Data Lake Store 中指定的防火牆規則。

### [Set-AzDataLakeStoreItemAcl](Set-AzDataLakeStoreItemAcl.md)
修改 Data Lake Store 中檔案或資料夾的 ACL。

### [Set-AzDataLakeStoreItemAclEntry](Set-AzDataLakeStoreItemAclEntry.md)
修改 Data Lake Store 中檔案或資料夾 ACL 中的專案。

### [Set-AzDataLakeStoreItemExpiry](Set-AzDataLakeStoreItemExpiry.md)
設定或移除 Azure Data Lake Store 帳戶中檔案的到期時間。

### [Set-AzDataLakeStoreItemOwner](Set-AzDataLakeStoreItemOwner.md)
修改 Data Lake Store 中檔案或資料夾的擁有者。

### [Set-AzDataLakeStoreItemPermission](Set-AzDataLakeStoreItemPermission.md)
修改 Data Lake Store 中檔案或資料夾的許可權八進位。

### [Set-AzDataLakeStoreTrustedIdProvider](Set-AzDataLakeStoreTrustedIdProvider.md)
修改指定 Data Lake Store 中指定的信任身分識別提供者。

### [Set-AzDataLakeStoreVirtualNetworkRule](Set-AzDataLakeStoreVirtualNetworkRule.md)
修改指定 Data Lake Store 中指定的虛擬網路規則。

### [Test-AzDataLakeStoreAccount](Test-AzDataLakeStoreAccount.md)
測試 Data Lake Store 帳戶是否存在。

### [Test-AzDataLakeStoreItem](Test-AzDataLakeStoreItem.md)
測試 Data Lake Store 中檔案或資料夾是否存在。

