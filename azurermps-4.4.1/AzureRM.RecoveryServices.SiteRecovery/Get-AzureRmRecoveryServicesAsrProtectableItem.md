---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: b209c706a8da88cfc5188b11302166469749c33f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455644"
---
# <span data-ttu-id="4640c-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4640c-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="4640c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4640c-102">SYNOPSIS</span></span>
<span data-ttu-id="4640c-103">在 ASR 保護容器中取得可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="4640c-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4640c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4640c-104">SYNTAX</span></span>

### <span data-ttu-id="4640c-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="4640c-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="4640c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4640c-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="4640c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4640c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="4640c-108">說明</span><span class="sxs-lookup"><span data-stu-id="4640c-108">DESCRIPTION</span></span>
<span data-ttu-id="4640c-109">**AzureRmRecoveryServicesAsrProtectableItem** Cmdlet 會取得 Azure Site Recovery 保護容器中的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="4640c-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="4640c-110">示例</span><span class="sxs-lookup"><span data-stu-id="4640c-110">EXAMPLES</span></span>

### <span data-ttu-id="4640c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4640c-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="4640c-112">在指定的 ASR 保護容器中取得所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="4640c-112">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="4640c-113">參數</span><span class="sxs-lookup"><span data-stu-id="4640c-113">PARAMETERS</span></span>

### <span data-ttu-id="4640c-114">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4640c-114">-FriendlyName</span></span>
<span data-ttu-id="4640c-115">指定 ASR [能保護的專案] 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4640c-115">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="4640c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4640c-116">-Name</span></span>
<span data-ttu-id="4640c-117">指定 ASR [能保護的專案] 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4640c-117">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="4640c-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4640c-118">-ProtectionContainer</span></span>
<span data-ttu-id="4640c-119">指定 Azure Site Recovery 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="4640c-119">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4640c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4640c-120">CommonParameters</span></span>
<span data-ttu-id="4640c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4640c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4640c-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4640c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4640c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4640c-123">INPUTS</span></span>

### <span data-ttu-id="4640c-124">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4640c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="4640c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4640c-125">OUTPUTS</span></span>

### <span data-ttu-id="4640c-126">System.object. IEnumerable "1 [ASRProtectableItem，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="4640c-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4640c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4640c-127">NOTES</span></span>

## <span data-ttu-id="4640c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4640c-128">RELATED LINKS</span></span>

[<span data-ttu-id="4640c-129">AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4640c-129">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="4640c-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="4640c-130">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
