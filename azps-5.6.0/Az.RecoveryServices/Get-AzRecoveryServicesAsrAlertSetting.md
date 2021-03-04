---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: cadde5ec773452897aa9c6915a5f3e16f00cfef5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916374"
---
# <span data-ttu-id="513eb-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="513eb-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="513eb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="513eb-102">SYNOPSIS</span></span>
<span data-ttu-id="513eb-103">為保存庫設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="513eb-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="513eb-104">語法</span><span class="sxs-lookup"><span data-stu-id="513eb-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="513eb-105">描述</span><span class="sxs-lookup"><span data-stu-id="513eb-105">DESCRIPTION</span></span>
<span data-ttu-id="513eb-106">**Get-AzRecoveryServicesAsrAlertSetting** Cmdlet 會取得保存庫的已設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="513eb-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="513eb-107">例子</span><span class="sxs-lookup"><span data-stu-id="513eb-107">EXAMPLES</span></span>

### <span data-ttu-id="513eb-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="513eb-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="513eb-109">取得 Azure 網站復原的通知/通知設定。</span><span class="sxs-lookup"><span data-stu-id="513eb-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="513eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="513eb-110">PARAMETERS</span></span>

### <span data-ttu-id="513eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513eb-111">-DefaultProfile</span></span>
<span data-ttu-id="513eb-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="513eb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513eb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513eb-113">CommonParameters</span></span>
<span data-ttu-id="513eb-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="513eb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513eb-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="513eb-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513eb-116">輸入</span><span class="sxs-lookup"><span data-stu-id="513eb-116">INPUTS</span></span>

### <span data-ttu-id="513eb-117">沒有</span><span class="sxs-lookup"><span data-stu-id="513eb-117">None</span></span>

## <span data-ttu-id="513eb-118">輸出</span><span class="sxs-lookup"><span data-stu-id="513eb-118">OUTPUTS</span></span>

### <span data-ttu-id="513eb-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="513eb-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="513eb-120">筆記</span><span class="sxs-lookup"><span data-stu-id="513eb-120">NOTES</span></span>

## <span data-ttu-id="513eb-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="513eb-121">RELATED LINKS</span></span>
