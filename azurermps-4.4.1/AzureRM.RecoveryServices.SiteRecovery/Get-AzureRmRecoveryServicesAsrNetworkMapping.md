---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626243"
---
# <span data-ttu-id="00e8a-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00e8a-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="00e8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="00e8a-103">取得目前電子倉庫之網站復原網路對應的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="00e8a-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00e8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="00e8a-104">SYNTAX</span></span>

### <span data-ttu-id="00e8a-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="00e8a-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="00e8a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="00e8a-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="00e8a-107">說明</span><span class="sxs-lookup"><span data-stu-id="00e8a-107">DESCRIPTION</span></span>
<span data-ttu-id="00e8a-108">**AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet 會取得有關恢復服務電子倉庫之 Azure Site Recovery 網路對應的資訊。</span><span class="sxs-lookup"><span data-stu-id="00e8a-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="00e8a-109">示例</span><span class="sxs-lookup"><span data-stu-id="00e8a-109">EXAMPLES</span></span>

### <span data-ttu-id="00e8a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="00e8a-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="00e8a-111">取得已傳送網路的所有網路對應。</span><span class="sxs-lookup"><span data-stu-id="00e8a-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="00e8a-112">參數</span><span class="sxs-lookup"><span data-stu-id="00e8a-112">PARAMETERS</span></span>

### <span data-ttu-id="00e8a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="00e8a-113">-Name</span></span>
<span data-ttu-id="00e8a-114">要取得之 ASR 網路對應物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="00e8a-114">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00e8a-115">-網路</span><span class="sxs-lookup"><span data-stu-id="00e8a-115">-Network</span></span>
<span data-ttu-id="00e8a-116">取得與指定的網路 ASR 物件相對應的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="00e8a-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00e8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e8a-117">CommonParameters</span></span>
<span data-ttu-id="00e8a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00e8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e8a-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00e8a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e8a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="00e8a-120">INPUTS</span></span>

### <span data-ttu-id="00e8a-121">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="00e8a-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="00e8a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="00e8a-122">OUTPUTS</span></span>

### <span data-ttu-id="00e8a-123">System.object. IEnumerable "1 [ASRNetworkMapping，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="00e8a-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="00e8a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="00e8a-124">NOTES</span></span>

## <span data-ttu-id="00e8a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="00e8a-125">RELATED LINKS</span></span>

[<span data-ttu-id="00e8a-126">新-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00e8a-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="00e8a-127">移除-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="00e8a-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
