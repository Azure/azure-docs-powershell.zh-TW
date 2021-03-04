---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 0c8773066f39d11e6985bbe4bd1f1e69cd9142f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911805"
---
# Az.Accounts 模組
## 描述
管理所有 Azure 模組的認證和一般組組。

## Az.Accounts Cmdlet
### [Add-AzEnvironment](Add-AzEnvironment.md)
新增 Azure Resource Manager 實例的端點和中繼資料。

### [Clear-AzCoNtext](Clear-AzContext.md)
移除所有 Azure 認證、帳戶和訂閱資訊。

### [Clear-AzDefault](Clear-AzDefault.md)
清除使用者目前內容中設定的預設設定。

### [Connect-AzAccount](Connect-AzAccount.md)
使用經過驗證的帳戶連接至 Azure，以用於 Az PowerShell 模組中的 Cmdlet。

### [Disable-AzCoNtextAutosave](Disable-AzContextAutosave.md)
關閉 Azure 認證自動儲存功能。  下次開啟 PowerShell 視窗時，您的登入資訊將會忘記

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
選擇不收集資料以改善 Azure PowerShell Cmdlet。 除非您明確退出宣告，否則預設會收集資料。

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
停用 Az 模組的 AzureRm 首碼別名。

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
中斷連接 Azure 帳戶的中斷，並移除所有與該帳戶相關聯的認證和上下文。

### [Enable-AzCoNtextAutosave](Enable-AzContextAutosave.md)
Azure 上下文是代表您作用中訂閱以執行命令的 PowerShell 物件，以及連接至 Azure 雲端所需的驗證資訊。 使用 Azure 上下文時，Azure PowerShell 不需要每次切換訂閱時重新驗證您的帳戶。 詳細資訊請參閱 Azure [PowerShell 上下文物件](https://docs.microsoft.com/powershell/azure/context-persistence)。

此 Cmdlet 可讓您在啟動 PowerShell 程式時儲存並自動載入 Azure 上下文資訊。 例如，開啟新視窗時。

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
讓 Azure PowerShell 收集資料以改善 Azure PowerShell Cmdlet 的使用者體驗。 執行此 Cmdlet 會加入宣告目前電腦上目前使用者的資料收集。 除非您明確退出宣告，否則預設會收集資料。

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
啟用 Az 模組的 AzureRm 首碼別名。

### [Get-AzAccessToken](Get-AzAccessToken.md)
取得原始存取權杖。 使用 -ResourceUrl 時，請確定該值與目前的 Azure 環境相符。 您可以參照到 的值 `(Get-AzContext).Environment` 。

### [Get-AzCoNtext](Get-AzContext.md)
獲得用來驗證 Azure Resource Manager 要求之中繼資料。

### [Get-AzCoNtextAutosaveSetting](Get-AzContextAutosaveSetting.md)
顯示內容自動儲存功能相關中繼資料，包括內容是否會自動儲存，以及可在哪裡找到已儲存的上下文和認證資訊。

### [Get-AzDefault](Get-AzDefault.md)
取得使用者目前上下文所設定的預設設定。

### [Get-AzEnvironment](Get-AzEnvironment.md)
取得 Azure 服務實例的端點和中繼資料。

### [Get-AzSubscription](Get-AzSubscription.md)
取得目前帳戶可存取的訂閱。

### [Get-AzTenant](Get-AzTenant.md)
為目前使用者獲得授權租使用者。

### [Import-AzCoNtext](Import-AzContext.md)
載入檔案中的 Azure 驗證資訊。

### [Invoke-Az InvokeMethod](Invoke-AzRestMethod.md)
僅建構和執行 Azure 資源管理端點的 HTTP 要求

### [Register-AzModule](Register-AzModule.md)
僅適用于內部使用 - 針對 AutoLet 產生的 Cmdlet 提供執行時間支援

### [Remove-AzCoNtext](Remove-AzContext.md)
從一組可用的上下文移除內容

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
移除連接特定 Azure 實例的端點和中繼資料。

### [Rename-AzCoNtext](Rename-AzContext.md)
重新命名 Azure 上下文。  根據預設，上下文會以使用者帳戶和訂閱命名。

### [Resolve-AzError](Resolve-AzError.md)
顯示 PowerShell 錯誤的詳細資訊，以及 Azure PowerShell 錯誤的延伸詳細資料。

### [Save-AzCoNtext](Save-AzContext.md)
會保存目前的驗證資訊，以用於其他 PowerShell 會話。

### [Select-AzCoNtext](Select-AzContext.md)
在 Azure PowerShell Cmdlet 中選取要鎖定的訂閱和帳戶

### [傳送意見](Send-Feedback.md)
透過一組引導提示傳送意見回饋給 Azure PowerShell 小組。

### [Set-AzCoNtext](Set-AzContext.md)
設定 Cmdlet 要用於目前會話的租使用者、訂閱及環境。

### [Set-AzDefault](Set-AzDefault.md)
在目前的情境中設定預設值

### [Set-AzEnvironment](Set-AzEnvironment.md)
設定 Azure 環境的屬性。

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
從電腦移除所有 AzureRm 模組。

