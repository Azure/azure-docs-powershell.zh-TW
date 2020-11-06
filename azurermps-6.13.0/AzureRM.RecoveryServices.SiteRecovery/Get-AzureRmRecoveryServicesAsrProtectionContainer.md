---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 6572fb6f98e06d03d698f75948ac4a7a38f2e785
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447285"
---
# <span data-ttu-id="b16c8-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b16c8-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="b16c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b16c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b16c8-103">取得恢復服務電子倉庫中的 ASR 保護容器。</span><span class="sxs-lookup"><span data-stu-id="b16c8-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b16c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="b16c8-104">SYNTAX</span></span>

### <span data-ttu-id="b16c8-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="b16c8-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b16c8-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b16c8-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b16c8-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b16c8-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b16c8-108">說明</span><span class="sxs-lookup"><span data-stu-id="b16c8-108">DESCRIPTION</span></span>
<span data-ttu-id="b16c8-109">**AzureRmRecoveryServicesAsrProtectionContainer** Cmdlet 會在復原服務電子倉庫中取得 Azure Site Recovery 保護容器。</span><span class="sxs-lookup"><span data-stu-id="b16c8-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="b16c8-110">保護容器是一個邏輯容器，可讓您) 和受保護的物件（例如虛擬電腦）來 (探索。</span><span class="sxs-lookup"><span data-stu-id="b16c8-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="b16c8-111">複製原則定義受保護專案的複製設定，而且可以與保護容器相關聯，並套用至可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="b16c8-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="b16c8-112">示例</span><span class="sxs-lookup"><span data-stu-id="b16c8-112">EXAMPLES</span></span>

### <span data-ttu-id="b16c8-113">範例1</span><span class="sxs-lookup"><span data-stu-id="b16c8-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="b16c8-114">[結構] $fabric 中的保護容器清單。</span><span class="sxs-lookup"><span data-stu-id="b16c8-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="b16c8-115">範例2</span><span class="sxs-lookup"><span data-stu-id="b16c8-115">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="b16c8-116">結構 $fabric 中的保護容器，名稱。</span><span class="sxs-lookup"><span data-stu-id="b16c8-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="b16c8-117">範例3</span><span class="sxs-lookup"><span data-stu-id="b16c8-117">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
FriendlyName                : xxxxxxxx
Name                        : xxxxx
ID                          : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxxxxxxxxxx/replicationProtectionContainers/xxxxxxxxxxxxxxxxxxxxxxxxx
Type                        : Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
FabricFriendlyName          : xxxxxxxxxxxxxxxxxxxxxxxxx
FabricType                  : VMware
Role                        : Primary
AvailablePolicies           : {V2aTestPolicy, v2ahydra, v2aswag-failback, v2aswag}
ProtectionContainerMappings : {pcmmapping, v2aPowerold, 636569dc-79bc-4f50-b83d-89f58717f0b2, df7aa204-b0ef-4d62-943e-324551030e5b}
```

<span data-ttu-id="b16c8-118">具有易記名稱的 fabric $fabric 中的保護容器。</span><span class="sxs-lookup"><span data-stu-id="b16c8-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="b16c8-119">參數</span><span class="sxs-lookup"><span data-stu-id="b16c8-119">PARAMETERS</span></span>

### <span data-ttu-id="b16c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16c8-120">-DefaultProfile</span></span>
<span data-ttu-id="b16c8-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b16c8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16c8-122">-結構</span><span class="sxs-lookup"><span data-stu-id="b16c8-122">-Fabric</span></span>
<span data-ttu-id="b16c8-123">尋找指定的 ASR 結構中的保護容器。</span><span class="sxs-lookup"><span data-stu-id="b16c8-123">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b16c8-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b16c8-124">-FriendlyName</span></span>
<span data-ttu-id="b16c8-125">指定要尋找之 ASR 保護容器的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="b16c8-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16c8-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b16c8-126">-Name</span></span>
<span data-ttu-id="b16c8-127">指定要尋找之 ASR 保護容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b16c8-127">Specifies the name of the ASR protection container to look for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16c8-128">CommonParameters</span></span>
<span data-ttu-id="b16c8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b16c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16c8-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b16c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16c8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b16c8-131">INPUTS</span></span>

### <span data-ttu-id="b16c8-132">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b16c8-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b16c8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b16c8-133">OUTPUTS</span></span>

### <span data-ttu-id="b16c8-134">System.object. IEnumerable "1 [ASRProtectionContainer，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="b16c8-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b16c8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b16c8-135">NOTES</span></span>

## <span data-ttu-id="b16c8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b16c8-136">RELATED LINKS</span></span>
