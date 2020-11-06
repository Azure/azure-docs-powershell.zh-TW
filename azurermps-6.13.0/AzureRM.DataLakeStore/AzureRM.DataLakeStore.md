---
Module Name: AzureRM.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/AzureRM.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/AzureRM.DataLakeStore.md
ms.openlocfilehash: 26a97d9f41ed7d0acb4e80a3302b22c8b2fab1c1
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/14/2020
ms.locfileid: "93443612"
---
# AzureRM DataLakeStore Module
## 說明
本節中的主題會將 azure Data Lake Store 的 Azure PowerShell Cmdlet 儲存至 Azure 資源管理員 (ARM) 架構中。 DataLakeStore 命名空間中存在 Cmdlet。 這些 Cmdlet 只適用于 Azure Data Lake Storage Gen1 帳戶。

## AzureRM DataLakeStore Cmdlet
### [附加 AzureRmDataLakeStoreFirewallRule](Add-AzureRmDataLakeStoreFirewallRule.md)
在指定的資料 Lake Store 帳戶中新增防火牆規則。

### [附加 AzureRmDataLakeStoreItemContent](Add-AzureRmDataLakeStoreItemContent.md)
將內容新增至 Data Lake Store 中的專案。

### [附加 AzureRmDataLakeStoreTrustedIdProvider](Add-AzureRmDataLakeStoreTrustedIdProvider.md)
將信任的身分識別提供者新增至指定的 Data Lake Store 帳戶。

### [附加 AzureRmDataLakeStoreVirtualNetworkRule](Add-AzureRmDataLakeStoreVirtualNetworkRule.md)
將虛擬網路規則新增至指定的 Data Lake Store 帳戶。

### [Enable-AzureRmDataLakeStoreKeyVault](Enable-AzureRmDataLakeStoreKeyVault.md)
嘗試啟用使用者管理的金鑰保存庫以加密指定的資料 Lake Store 帳戶。

### [Export-AzureRmDataLakeStoreChildItemProperties](Export-AzureRmDataLakeStoreChildItemProperties.md)
從指定路徑將整個樹狀結構的 [磁片使用量] 與 [Acl)  (的內容匯出至輸出路徑

### [Export-AzureRmDataLakeStoreItem](Export-AzureRmDataLakeStoreItem.md)
從 Data Lake Store 下載檔案。

### [AzureRmDataLakeStoreAccount](Get-AzureRmDataLakeStoreAccount.md)
取得 Data Lake Store 帳戶的詳細資料。

### [AzureRmDataLakeStoreChildItem](Get-AzureRmDataLakeStoreChildItem.md)
取得 Data Lake Store 中資料夾中的專案清單。

### [AzureRmDataLakeStoreChildItemSummary](Get-AzureRmDataLakeStoreChildItemSummary.md)
取得指定路徑中所含之總大小、檔案和目錄的摘要

### [AzureRmDataLakeStoreFirewallRule](Get-AzureRmDataLakeStoreFirewallRule.md)
取得指定資料 Lake Store 中的指定防火牆規則。
如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。

### [AzureRmDataLakeStoreItem](Get-AzureRmDataLakeStoreItem.md)
取得 Data Lake Store 中檔案或資料夾的詳細資料。

### [AzureRmDataLakeStoreItemAclEntry](Get-AzureRmDataLakeStoreItemAclEntry.md)
在 Data Lake Store 中取得檔案或資料夾的 ACL 中的專案。

### [AzureRmDataLakeStoreItemContent](Get-AzureRmDataLakeStoreItemContent.md)
取得 Data Lake Store 中檔案的內容。

### [AzureRmDataLakeStoreItemOwner](Get-AzureRmDataLakeStoreItemOwner.md)
取得 Data Lake Store 中的檔案或資料夾擁有者。

### [AzureRmDataLakeStoreItemPermission](Get-AzureRmDataLakeStoreItemPermission.md)
取得 Data Lake Store 中檔案或資料夾的許可權八進位數。

### [AzureRmDataLakeStoreTrustedIdProvider](Get-AzureRmDataLakeStoreTrustedIdProvider.md)
在指定的 Data Lake Store 中取得指定的信任身分識別提供者。
如果沒有指定提供者，則會列出該帳戶的所有提供者。

### [AzureRmDataLakeStoreVirtualNetworkRule](Get-AzureRmDataLakeStoreVirtualNetworkRule.md)
取得指定資料 Lake Store 中指定的虛擬網路規則。
如果未指定虛擬網路規則，則會列出該帳戶的所有虛擬網路規則。

### [匯入-AzureRmDataLakeStoreItem](Import-AzureRmDataLakeStoreItem.md)
將本機檔案或目錄上傳到 Data Lake Store。

### [Join-AzureRmDataLakeStoreItem](Join-AzureRmDataLakeStoreItem.md)
加入一或多個檔案，在 Data Lake Store 中建立一個檔案。

### [移動流覽 AzureRmDataLakeStoreItem](Move-AzureRmDataLakeStoreItem.md)
移動或重新命名 Data Lake Store 中的檔案或資料夾。

### [新-AzureRmDataLakeStoreAccount](New-AzureRmDataLakeStoreAccount.md)
建立新的 Data Lake Store 帳戶。

### [新-AzureRmDataLakeStoreItem](New-AzureRmDataLakeStoreItem.md)
在 Data Lake Store 中建立新的檔案或資料夾。

### [移除-AzureRmDataLakeStoreAccount](Remove-AzureRmDataLakeStoreAccount.md)
永久刪除 Data Lake Store 帳戶。

### [移除-AzureRmDataLakeStoreFirewallRule](Remove-AzureRmDataLakeStoreFirewallRule.md)
移除指定資料 Lake Store 中的指定防火牆規則。

### [移除-AzureRmDataLakeStoreItem](Remove-AzureRmDataLakeStoreItem.md)
刪除 Data Lake Store 中的檔案或資料夾。

### [移除-AzureRmDataLakeStoreItemAcl](Remove-AzureRmDataLakeStoreItemAcl.md)
清除 Data Lake Store 中的檔案或資料夾的 ACL。

### [移除-AzureRmDataLakeStoreItemAclEntry](Remove-AzureRmDataLakeStoreItemAclEntry.md)
從 Data Lake Store 中的檔案或資料夾 ACL 中移除專案。

### [移除-AzureRmDataLakeStoreTrustedIdProvider](Remove-AzureRmDataLakeStoreTrustedIdProvider.md)
移除指定資料 Lake Store 中指定的信任身分識別提供者。

### [移除-AzureRmDataLakeStoreVirtualNetworkRule](Remove-AzureRmDataLakeStoreVirtualNetworkRule.md)
移除指定資料 Lake Store 中指定的虛擬網路規則。

### [Set-AzureRmDataLakeStoreAccount](Set-AzureRmDataLakeStoreAccount.md)
修改 Data Lake Store 帳戶。

### [Set-AzureRmDataLakeStoreFirewallRule](Set-AzureRmDataLakeStoreFirewallRule.md)
修改指定資料 Lake Store 中的指定防火牆規則。

### [Set-AzureRmDataLakeStoreItemAcl](Set-AzureRmDataLakeStoreItemAcl.md)
修改 Data Lake Store 中檔案或資料夾的 ACL。

### [Set-AzureRmDataLakeStoreItemAclEntry](Set-AzureRmDataLakeStoreItemAclEntry.md)
修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。

### [Set-AzureRmDataLakeStoreItemExpiry](Set-AzureRmDataLakeStoreItemExpiry.md)
針對 Azure Data Lake Store 帳戶中的檔案設定或移除到期時間。

### [Set-AzureRmDataLakeStoreItemOwner](Set-AzureRmDataLakeStoreItemOwner.md)
修改 Data Lake Store 中的檔案或資料夾擁有者。

### [Set-AzureRmDataLakeStoreItemPermission](Set-AzureRmDataLakeStoreItemPermission.md)
修改 Data Lake Store 中檔案或資料夾的許可權八進位。

### [Set-AzureRmDataLakeStoreTrustedIdProvider](Set-AzureRmDataLakeStoreTrustedIdProvider.md)
在指定的 Data Lake Store 中修改指定的信任身分識別提供者。

### [Set-AzureRmDataLakeStoreVirtualNetworkRule](Set-AzureRmDataLakeStoreVirtualNetworkRule.md)
在指定的 Data Lake Store 中修改指定的虛擬網路規則。

### [Test-AzureRmDataLakeStoreAccount](Test-AzureRmDataLakeStoreAccount.md)
測試資料 Lake Store 帳戶是否存在。

### [Test-AzureRmDataLakeStoreItem](Test-AzureRmDataLakeStoreItem.md)
測試 Data Lake Store 中的檔案或資料夾是否存在。

