---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455639"
---
# <span data-ttu-id="fd134-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fd134-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="fd134-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd134-102">SYNOPSIS</span></span>
<span data-ttu-id="fd134-103">取得 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="fd134-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd134-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd134-104">SYNTAX</span></span>

### <span data-ttu-id="fd134-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="fd134-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="fd134-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="fd134-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="fd134-107">說明</span><span class="sxs-lookup"><span data-stu-id="fd134-107">DESCRIPTION</span></span>
<span data-ttu-id="fd134-108">**AzureRmRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會針對指定的 ASR 保護容器，取得保存庫中針對複製原則對應 (關聯性) 的保護容器資訊。</span><span class="sxs-lookup"><span data-stu-id="fd134-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="fd134-109">示例</span><span class="sxs-lookup"><span data-stu-id="fd134-109">EXAMPLES</span></span>

### <span data-ttu-id="fd134-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fd134-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="fd134-111">取得指定保護容器的所有保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="fd134-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="fd134-112">參數</span><span class="sxs-lookup"><span data-stu-id="fd134-112">PARAMETERS</span></span>

### <span data-ttu-id="fd134-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd134-113">-Name</span></span>
<span data-ttu-id="fd134-114">指定要取得之保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd134-114">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="fd134-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fd134-115">-ProtectionContainer</span></span>
<span data-ttu-id="fd134-116">取得與指定的 ASR 保護容器物件相對應的保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="fd134-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="fd134-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd134-117">CommonParameters</span></span>
<span data-ttu-id="fd134-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd134-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd134-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd134-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd134-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fd134-120">INPUTS</span></span>

### <span data-ttu-id="fd134-121">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fd134-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="fd134-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fd134-122">OUTPUTS</span></span>

### <span data-ttu-id="fd134-123">System.object. IEnumerable "1 [ASRProtectionContainerMapping，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="fd134-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fd134-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fd134-124">NOTES</span></span>

## <span data-ttu-id="fd134-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd134-125">RELATED LINKS</span></span>

[<span data-ttu-id="fd134-126">新-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fd134-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="fd134-127">移除-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fd134-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
