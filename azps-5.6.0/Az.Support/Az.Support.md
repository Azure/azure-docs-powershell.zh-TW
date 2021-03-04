---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: b02401044f3b01a73954ac199cc15457cddb795a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908701"
---
# Az.Support 模組
## 描述
本節主題將說明在 Azure Resource Manager (ARM) 中建立及管理 Azure 支援票證的 Azure PowerShell Cmdlet。 Cmdlet 存在於 Microsoft.Azure.Commands.support 命名空間中

## Az.Support Cmdlet
### [Get-AzSupportService](Get-AzSupportService.md)
獲得目前支援可用的 Azure 服務清單。 每個 Azure 服務都有自己的一組類別，稱為問題分類。 使用 Get-AzSupportProblemClassification 取得服務目前的問題分類清單。 您可以使用服務和問題分類 GUID，使用 New-AzSupportTicket 建立新的支援票證。

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
獲得 Azure 服務目前的問題分類清單。 您可以使用服務和問題分類 GUID，使用 New-AzSupportTicket 建立新的支援票證。 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
建立支援連絡人設定檔物件的協助程式 Cmdlet。 您可以在 Cmdlet 中使用此New-AzSupportTicket物件。

### [New-AzSupportTicket](New-AzSupportTicket.md)
建立新的 Azure 支援票證。 此作業以 Azure 新增支援要求頁面 [的行為為模型](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)。

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
獲得支援票證清單。 您可以根據票證名稱取得完整支援票證詳細資料，或根據狀態或 *CreatedDate 篩選支援票證*。

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
更新支援票證的嚴重性、狀態或客戶連絡人詳細資料。

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
獲得支援票證的通訊。 您也可以使用 *CreatedDate* 或 *CommunicationType 篩選支援票證通訊*。 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
新增客戶通訊至 Azure 支援票證。 



