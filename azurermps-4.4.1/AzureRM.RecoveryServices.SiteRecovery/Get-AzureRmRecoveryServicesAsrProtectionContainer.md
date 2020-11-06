---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456444"
---
# <span data-ttu-id="8530f-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8530f-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="8530f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8530f-102">SYNOPSIS</span></span>
<span data-ttu-id="8530f-103">取得恢復服務電子倉庫中的 ASR 保護容器。</span><span class="sxs-lookup"><span data-stu-id="8530f-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8530f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8530f-104">SYNTAX</span></span>

### <span data-ttu-id="8530f-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="8530f-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="8530f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="8530f-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="8530f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="8530f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="8530f-108">說明</span><span class="sxs-lookup"><span data-stu-id="8530f-108">DESCRIPTION</span></span>
<span data-ttu-id="8530f-109">**AzureRmRecoveryServicesAsrProtectionContainer** Cmdlet 會在復原服務電子倉庫中取得 Azure Site Recovery 保護容器。</span><span class="sxs-lookup"><span data-stu-id="8530f-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="8530f-110">保護容器是一個邏輯容器，可讓您) 和受保護的物件（例如虛擬電腦）來 (探索。</span><span class="sxs-lookup"><span data-stu-id="8530f-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="8530f-111">複製原則定義受保護專案的複製設定，而且可以與保護容器相關聯，並套用至可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="8530f-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="8530f-112">示例</span><span class="sxs-lookup"><span data-stu-id="8530f-112">EXAMPLES</span></span>

### <span data-ttu-id="8530f-113">範例1</span><span class="sxs-lookup"><span data-stu-id="8530f-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="8530f-114">在上述範例中，取得指定 ASR 結構中的所有 ASR 保護容器， (管線輸入。 ) </span><span class="sxs-lookup"><span data-stu-id="8530f-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="8530f-115">參數</span><span class="sxs-lookup"><span data-stu-id="8530f-115">PARAMETERS</span></span>

### <span data-ttu-id="8530f-116">-結構</span><span class="sxs-lookup"><span data-stu-id="8530f-116">-Fabric</span></span>
<span data-ttu-id="8530f-117">尋找指定的 ASR 結構中的保護容器。</span><span class="sxs-lookup"><span data-stu-id="8530f-117">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8530f-118">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8530f-118">-FriendlyName</span></span>
<span data-ttu-id="8530f-119">指定要尋找之 ASR 保護容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="8530f-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8530f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8530f-120">-Name</span></span>
<span data-ttu-id="8530f-121">指定要尋找之 ASR 保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8530f-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="8530f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8530f-122">CommonParameters</span></span>
<span data-ttu-id="8530f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8530f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8530f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8530f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8530f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8530f-125">INPUTS</span></span>

### <span data-ttu-id="8530f-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="8530f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="8530f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8530f-127">OUTPUTS</span></span>

### <span data-ttu-id="8530f-128">System.object. IEnumerable "1 [ASRProtectionContainer，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="8530f-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8530f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8530f-129">NOTES</span></span>

## <span data-ttu-id="8530f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8530f-130">RELATED LINKS</span></span>

