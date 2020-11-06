---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: aa2cd93d21ba22405fff0f3c5fcf336d00f2f6b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448045"
---
# <span data-ttu-id="ed445-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ed445-101">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="ed445-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed445-102">SYNOPSIS</span></span>
<span data-ttu-id="ed445-103">將指定的複製原則與指定的 ASR 保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="ed445-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed445-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed445-104">SYNTAX</span></span>

### <span data-ttu-id="ed445-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="ed445-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed445-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ed445-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed445-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed445-107">DESCRIPTION</span></span>
<span data-ttu-id="ed445-108">**新的-AzureRmRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會將指定的複製原則與指定的保護容器建立關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="ed445-108">The **New-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="ed445-109">示例</span><span class="sxs-lookup"><span data-stu-id="ed445-109">EXAMPLES</span></span>

### <span data-ttu-id="ed445-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ed445-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="ed445-111">使用指定的參數開始建立保護容器對應，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ed445-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ed445-112">參數</span><span class="sxs-lookup"><span data-stu-id="ed445-112">PARAMETERS</span></span>

### <span data-ttu-id="ed445-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed445-113">-Name</span></span>
<span data-ttu-id="ed445-114">指定保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed445-114">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed445-115">-原則</span><span class="sxs-lookup"><span data-stu-id="ed445-115">-Policy</span></span>
<span data-ttu-id="ed445-116">指定要在對應中使用之複製原則的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="ed445-116">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed445-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ed445-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="ed445-118">針對要在對應中使用的主要保護容器，指定 ASR 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="ed445-118">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed445-119">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ed445-119">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="ed445-120">針對將在複製到非 Azure 的復原位置所使用的對應 (，指定要在所使用之對應中使用之 [恢復保護] 容器的 [ASR 保護] 容器物件。 ) </span><span class="sxs-lookup"><span data-stu-id="ed445-120">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed445-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ed445-121">-Confirm</span></span>
<span data-ttu-id="ed445-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed445-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed445-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed445-123">-WhatIf</span></span>
<span data-ttu-id="ed445-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed445-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed445-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed445-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed445-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed445-126">CommonParameters</span></span>
<span data-ttu-id="ed445-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed445-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed445-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed445-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed445-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ed445-129">INPUTS</span></span>

### <span data-ttu-id="ed445-130">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ed445-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="ed445-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ed445-131">OUTPUTS</span></span>

### <span data-ttu-id="ed445-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed445-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed445-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ed445-133">NOTES</span></span>

## <span data-ttu-id="ed445-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed445-134">RELATED LINKS</span></span>

[<span data-ttu-id="ed445-135">AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ed445-135">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="ed445-136">移除-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ed445-136">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
