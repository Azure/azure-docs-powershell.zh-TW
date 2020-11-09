---
Module Name: Az.DataLakeStore
Module Guid: 90dfd814-abce-4e1f-99b6-fe16760c079a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Az.DataLakeStore.md
ms.openlocfilehash: 5796a3692274db9b49ed16c00935ed1cd2d4e8f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285048"
---
# Az DataLakeStore 模組
## 說明
本節中的主題會將 azure Data Lake Store 的 Azure PowerShell Cmdlet 儲存至 Azure 資源管理員 (ARM) 架構中。 DataLakeStore 命名空間中存在 Cmdlet。 這些 Cmdlet 只適用于 Azure Data Lake Storage Gen1 帳戶。

## Az DataLakeStore Cmdlet
### [附加 AzDataLakeStoreFirewallRule](Add-AzDataLakeStoreFirewallRule.md)
在指定的資料 Lake Store 帳戶中新增防火牆規則。

### [附加 AzDataLakeStoreItemContent](Add-AzDataLakeStoreItemContent.md)
將內容新增至 Data Lake Store 中的專案。

### [附加 AzDataLakeStoreTrustedIdProvider](Add-AzDataLakeStoreTrustedIdProvider.md)
將信任的身分識別提供者新增至指定的 Data Lake Store 帳戶。

### [附加 AzDataLakeStoreVirtualNetworkRule](Add-AzDataLakeStoreVirtualNetworkRule.md)
將虛擬網路規則新增至指定的 Data Lake Store 帳戶。

### [Enable-AzDataLakeStoreKeyVault](Enable-AzDataLakeStoreKeyVault.md)
嘗試啟用使用者管理的金鑰保存庫以加密指定的資料 Lake Store 帳戶。

### [Export-AzDataLakeStoreChildItemProperty](Export-AzDataLakeStoreChildItemProperty.md)
從指定路徑將整個樹狀結構的 [磁片使用量] 與 [Acl)  (的內容匯出至輸出路徑

### [Export-AzDataLakeStoreItem](Export-AzDataLakeStoreItem.md)
從 Data Lake Store 下載檔案。

### [AzDataLakeStoreAccount](Get-AzDataLakeStoreAccount.md)
取得 Data Lake Store 帳戶的詳細資料。

### [AzDataLakeStoreChildItem](Get-AzDataLakeStoreChildItem.md)
取得 Data Lake Store 中資料夾中的專案清單。

### [AzDataLakeStoreChildItemSummary](Get-AzDataLakeStoreChildItemSummary.md)
取得指定路徑中所含之總大小、檔案和目錄的摘要

### [AzDataLakeStoreFirewallRule](Get-AzDataLakeStoreFirewallRule.md)
取得指定資料 Lake Store 中的指定防火牆規則。
如果未指定任何防火牆規則，則會列出該帳戶的所有防火牆規則。

### [AzDataLakeStoreItem](Get-AzDataLakeStoreItem.md)
取得 Data Lake Store 中檔案或資料夾的詳細資料。

### [AzDataLakeStoreItemAclEntry](Get-AzDataLakeStoreItemAclEntry.md)
在 Data Lake Store 中取得檔案或資料夾的 ACL 中的專案。

### [AzDataLakeStoreItemContent](Get-AzDataLakeStoreItemContent.md)
取得 Data Lake Store 中檔案的內容。

### [AzDataLakeStoreItemOwner](Get-AzDataLakeStoreItemOwner.md)
取得 Data Lake Store 中的檔案或資料夾擁有者。

### [AzDataLakeStoreItemPermission](Get-AzDataLakeStoreItemPermission.md)
取得 Data Lake Store 中檔案或資料夾的許可權八進位數。

### [AzDataLakeStoreTrustedIdProvider](Get-AzDataLakeStoreTrustedIdProvider.md)
在指定的 Data Lake Store 中取得指定的信任身分識別提供者。
如果沒有指定提供者，則會列出該帳戶的所有提供者。

### [AzDataLakeStoreVirtualNetworkRule](Get-AzDataLakeStoreVirtualNetworkRule.md)
取得指定資料 Lake Store 中指定的虛擬網路規則。
如果未指定虛擬網路規則，則會列出該帳戶的所有虛擬網路規則。

### [匯入-AzDataLakeStoreItem](Import-AzDataLakeStoreItem.md)
將本機檔案或目錄上傳到 Data Lake Store。

### [Join-AzDataLakeStoreItem](Join-AzDataLakeStoreItem.md)
加入一或多個檔案，在 Data Lake Store 中建立一個檔案。

### [移動流覽 AzDataLakeStoreItem](Move-AzDataLakeStoreItem.md)
移動或重新命名 Data Lake Store 中的檔案或資料夾。

### [新-AzDataLakeStoreAccount](New-AzDataLakeStoreAccount.md)
建立新的 Data Lake Store 帳戶。

### [新-AzDataLakeStoreItem](New-AzDataLakeStoreItem.md)
在 Data Lake Store 中建立新的檔案或資料夾。

### [移除-AzDataLakeStoreAccount](Remove-AzDataLakeStoreAccount.md)
永久刪除 Data Lake Store 帳戶。

### [移除-AzDataLakeStoreFirewallRule](Remove-AzDataLakeStoreFirewallRule.md)
移除指定資料 Lake Store 中的指定防火牆規則。

### [移除-AzDataLakeStoreItem](Remove-AzDataLakeStoreItem.md)
刪除 Data Lake Store 中的檔案或資料夾。

### [移除-AzDataLakeStoreItemAcl](Remove-AzDataLakeStoreItemAcl.md)
清除 Data Lake Store 中的檔案或資料夾的 ACL。

### [移除-AzDataLakeStoreItemAclEntry](Remove-AzDataLakeStoreItemAclEntry.md)
從 Data Lake Store 中的檔案或資料夾 ACL 中移除專案。

### [移除-AzDataLakeStoreTrustedIdProvider](Remove-AzDataLakeStoreTrustedIdProvider.md)
移除指定資料 Lake Store 中指定的信任身分識別提供者。

### [移除-AzDataLakeStoreVirtualNetworkRule](Remove-AzDataLakeStoreVirtualNetworkRule.md)
移除指定資料 Lake Store 中指定的虛擬網路規則。

### [Set-AzDataLakeStoreAccount](Set-AzDataLakeStoreAccount.md)
修改 Data Lake Store 帳戶。

### [Set-AzDataLakeStoreFirewallRule](Set-AzDataLakeStoreFirewallRule.md)
修改指定資料 Lake Store 中的指定防火牆規則。

### [Set-AzDataLakeStoreItemAcl](Set-AzDataLakeStoreItemAcl.md)
修改 Data Lake Store 中檔案或資料夾的 ACL。

### [Set-AzDataLakeStoreItemAclEntry](Set-AzDataLakeStoreItemAclEntry.md)
修改 Data Lake Store 中檔案或資料夾的 ACL 中的專案。

### [Set-AzDataLakeStoreItemExpiry](Set-AzDataLakeStoreItemExpiry.md)
針對 Azure Data Lake Store 帳戶中的檔案設定或移除到期時間。

### [Set-AzDataLakeStoreItemOwner](Set-AzDataLakeStoreItemOwner.md)
修改 Data Lake Store 中的檔案或資料夾擁有者。

### [Set-AzDataLakeStoreItemPermission](Set-AzDataLakeStoreItemPermission.md)
修改 Data Lake Store 中檔案或資料夾的許可權八進位。

### [Set-AzDataLakeStoreTrustedIdProvider](Set-AzDataLakeStoreTrustedIdProvider.md)
在指定的 Data Lake Store 中修改指定的信任身分識別提供者。

### [Set-AzDataLakeStoreVirtualNetworkRule](Set-AzDataLakeStoreVirtualNetworkRule.md)
在指定的 Data Lake Store 中修改指定的虛擬網路規則。

### [Test-AzDataLakeStoreAccount](Test-AzDataLakeStoreAccount.md)
測試資料 Lake Store 帳戶是否存在。

### [Test-AzDataLakeStoreItem](Test-AzDataLakeStoreItem.md)
測試 Data Lake Store 中的檔案或資料夾是否存在。

