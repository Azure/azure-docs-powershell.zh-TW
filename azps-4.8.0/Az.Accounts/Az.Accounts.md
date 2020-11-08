---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: d15e053e8801c292add5a80e04726f1eeb1181fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126642"
---
# Az. [帳戶] 模組
## 說明
管理所有 Azure 模組的認證與一般設定。

## Az. 帳戶 Cmdlet
### [附加 AzEnvironment](Add-AzEnvironment.md)
新增 Azure 資源管理員實例的端點和中繼資料。

### [Clear-AzCoNtext](Clear-AzContext.md)
移除所有 Azure 認證、帳戶及訂閱資訊。

### [Clear-AzDefault](Clear-AzDefault.md)
清除目前內容中由使用者設定的預設值。

### [連接-AzAccount](Connect-AzAccount.md)
使用已驗證的帳戶連線至 Azure，以便與 Az PowerShell 模組中的 Cmdlet 搭配使用。

### [Disable-AzCoNtextAutosave](Disable-AzContextAutosave.md)
關閉 autosaving Azure 認證。  下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
在收集資料時，無法改善 Azure PowerShell Cmdlet。 預設會收集資料，除非您明確退出宣告。

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
針對 Az 模組停用 AzureRm 首碼別名。

### [中斷連線-AzAccount](Disconnect-AzAccount.md)
中斷連線的 Azure 帳戶，並移除與該帳戶相關聯的所有認證與內容。

### [Enable-AzCoNtextAutosave](Enable-AzContextAutosave.md)
允許在您開啟 PowerShell 視窗時，儲存 azure 認證、帳戶和訂閱資訊，並自動載入。 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
啟用 Azure PowerShell 以收集資料，以使用 Azure PowerShell Cmdlet 來改善使用者體驗。 執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。 預設會收集資料，除非您明確退出宣告。

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
啟用 Az 模組的 AzureRm 首碼別名。

### [AzCoNtext](Get-AzContext.md)
取得用來驗證 Azure 資源管理器要求的中繼資料。

### [AzCoNtextAutosaveSetting](Get-AzContextAutosaveSetting.md)
顯示有關內容自動儲存功能的中繼資料，包括是否自動儲存內容，以及可以在何處找到已儲存的內容和認證資訊。

### [AzDefault](Get-AzDefault.md)
取得使用者在目前內容中設定的預設值。

### [AzEnvironment](Get-AzEnvironment.md)
取得 Azure 服務實例的端點和中繼資料。

### [AzProfile](Get-AzProfile.md)
取得已安裝的模組支援的服務設定檔。

### [AzSubscription](Get-AzSubscription.md)
取得目前帳戶可以存取的訂閱。

### [AzTenant](Get-AzTenant.md)
取得目前使用者的授權承租人。

### [匯入-AzCoNtext](Import-AzContext.md)
從檔案載入 Azure 驗證資訊。

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
僅針對 Azure 資源管理端點構造及執行 HTTP 要求

### [Register-AzModule](Register-AzModule.md)
僅供內部使用-提供 AutoRest 產生的 Cmdlet 的執行時間支援

### [移除-AzCoNtext](Remove-AzContext.md)
從可用的上下文集合中移除內容

### [移除-AzEnvironment](Remove-AzEnvironment.md)
移除端點和中繼資料以連接至指定的 Azure 實例。

### [重新命名 AzCoNtext](Rename-AzContext.md)
重新命名 Azure 內容。  根據預設，上下文是依使用者帳戶和訂閱來命名。

### [解決-AzError](Resolve-AzError.md)
顯示有關 PowerShell 錯誤的詳細資訊，以及有關 Azure PowerShell 錯誤的詳細資訊。

### [儲存-AzCoNtext](Save-AzContext.md)
儲存目前的驗證資訊以供在其他 PowerShell 會話中使用。

### [選取-AzCoNtext](Select-AzContext.md)
選取 Azure PowerShell Cmdlet 中的目標訂閱與帳戶

### [選取-AzProfile](Select-AzProfile.md)
針對支援多個服務設定檔的模組，請載入與指定的服務設定檔相對應的 Cmdlet。

### [傳送-意見反應](Send-Feedback.md)
透過一組引導提示，將意見反應傳送給 Azure PowerShell 小組。

### [Set-AzCoNtext](Set-AzContext.md)
設定要在目前會話中使用之 Cmdlet 的租使用者、訂閱及環境。

### [Set-AzDefault](Set-AzDefault.md)
在目前的內容中設定預設值

### [Set-AzEnvironment](Set-AzEnvironment.md)
設定 Azure 環境的屬性。

### [卸載-AzureRm](Uninstall-AzureRm.md)
從電腦中移除所有 AzureRm 模組。

