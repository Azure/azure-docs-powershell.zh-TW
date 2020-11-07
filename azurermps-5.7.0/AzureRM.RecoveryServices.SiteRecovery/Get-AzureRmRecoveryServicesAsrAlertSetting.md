---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624693"
---
# <span data-ttu-id="e0ea1-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="e0ea1-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="e0ea1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ea1-103">取得保存庫的已設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="e0ea1-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ea1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0ea1-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0ea1-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ea1-106">**AzureRmRecoveryServicesAsrAlertSetting** Cmdlet 會取得保存庫的已設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="e0ea1-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="e0ea1-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="e0ea1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e0ea1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="e0ea1-109">取得 Azure Site Recovery 的警示/通知設定。</span><span class="sxs-lookup"><span data-stu-id="e0ea1-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="e0ea1-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0ea1-110">PARAMETERS</span></span>

### <span data-ttu-id="e0ea1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ea1-111">-DefaultProfile</span></span>
<span data-ttu-id="e0ea1-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0ea1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ea1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ea1-113">CommonParameters</span></span>
<span data-ttu-id="e0ea1-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0ea1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ea1-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0ea1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ea1-116">輸入</span><span class="sxs-lookup"><span data-stu-id="e0ea1-116">INPUTS</span></span>

### <span data-ttu-id="e0ea1-117">所有</span><span class="sxs-lookup"><span data-stu-id="e0ea1-117">None</span></span>

## <span data-ttu-id="e0ea1-118">輸出</span><span class="sxs-lookup"><span data-stu-id="e0ea1-118">OUTPUTS</span></span>

### <span data-ttu-id="e0ea1-119">System.object. IEnumerable "1 [ASRAlertSetting，RecoveryServices. SiteRecovery，Version = 0.1.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="e0ea1-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e0ea1-120">筆記</span><span class="sxs-lookup"><span data-stu-id="e0ea1-120">NOTES</span></span>

## <span data-ttu-id="e0ea1-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0ea1-121">RELATED LINKS</span></span>
