---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139416"
---
# Az. 支援模組
## 說明
本節主題所述的 Azure PowerShell Cmdlet 可在 Azure 資源管理器 (ARM) 架構中建立和管理 Azure 支援票證。 Cmdlet 存在於 Microsoft. 命令中。支援命名空間

## Az. 支援 Cmdlet
### [AzSupportService](Get-AzSupportService.md)
取得目前提供支援的 Azure 服務清單。 每個 Azure 服務都有自己的一組類別，稱為「問題分類」。 使用 AzSupportProblemClassification，以取得服務的目前問題分類清單。 您可以使用 [服務] 和 [問題分類 GUID]，使用新的 AzSupportTicket 建立新的支援票證。

### [AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
取得 Azure 服務的目前問題分類清單。 您可以使用 [服務] 和 [問題分類 GUID]，使用新的 AzSupportTicket 建立新的支援票證。 

### [新-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
協助程式 Cmdlet 建立支援連絡人設定檔物件。 您可以將此物件用於 New-AzSupportTicket Cmdlet。

### [新-AzSupportTicket](New-AzSupportTicket.md)
建立新的 Azure 支援票證。 這個作業會根據 Azure [新支援要求頁面](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)的行為進行模型。

### [AzSupportTicket](Get-AzSupportTicket.md)
取得支援票證的清單。 您可以依票證名稱取得完整的支援票證詳細資料，或依 *狀態* 或 *CreatedDate* 篩選支援票證。

### [更新-AzSupportTicket](Update-AzSupportTicket.md)
更新支援票證的嚴重性、狀態或客戶連絡人詳細資料。

### [AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
取得支援票證的通訊。 您也可以使用 *CreatedDate* 或 *CommunicationType* 來篩選支援票證通訊。 

### [新-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
將新的客戶通訊新增至 Azure 支援票證。 



