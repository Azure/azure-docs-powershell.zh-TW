---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969149"
---
# <span data-ttu-id="b80b4-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b80b4-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="b80b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b80b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b80b4-103">取得保存庫的已設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="b80b4-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b80b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="b80b4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b80b4-105">說明</span><span class="sxs-lookup"><span data-stu-id="b80b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b80b4-106">**AzRecoveryServicesAsrAlertSetting** Cmdlet 會取得保存庫的已設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="b80b4-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b80b4-107">示例</span><span class="sxs-lookup"><span data-stu-id="b80b4-107">EXAMPLES</span></span>

### <span data-ttu-id="b80b4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b80b4-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="b80b4-109">取得 Azure Site Recovery 的警示/通知設定。</span><span class="sxs-lookup"><span data-stu-id="b80b4-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="b80b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="b80b4-110">PARAMETERS</span></span>

### <span data-ttu-id="b80b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80b4-111">-DefaultProfile</span></span>
<span data-ttu-id="b80b4-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b80b4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b80b4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80b4-113">CommonParameters</span></span>
<span data-ttu-id="b80b4-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b80b4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80b4-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b80b4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80b4-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b80b4-116">INPUTS</span></span>

### <span data-ttu-id="b80b4-117">所有</span><span class="sxs-lookup"><span data-stu-id="b80b4-117">None</span></span>

## <span data-ttu-id="b80b4-118">輸出</span><span class="sxs-lookup"><span data-stu-id="b80b4-118">OUTPUTS</span></span>

### <span data-ttu-id="b80b4-119">RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b80b4-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="b80b4-120">筆記</span><span class="sxs-lookup"><span data-stu-id="b80b4-120">NOTES</span></span>

## <span data-ttu-id="b80b4-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="b80b4-121">RELATED LINKS</span></span>
