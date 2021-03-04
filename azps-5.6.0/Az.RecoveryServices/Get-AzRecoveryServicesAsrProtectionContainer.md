---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 1d7f8adfa0db67d66c65c5ac7f3df7c64b665fda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912338"
---
# <span data-ttu-id="2f432-101">Get-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2f432-101">Get-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="2f432-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f432-102">SYNOPSIS</span></span>
<span data-ttu-id="2f432-103">在修復服務儲存庫中獲得 ASR 保護容器。</span><span class="sxs-lookup"><span data-stu-id="2f432-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

## <span data-ttu-id="2f432-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f432-104">SYNTAX</span></span>

### <span data-ttu-id="2f432-105">ByFabricObject (預設) </span><span class="sxs-lookup"><span data-stu-id="2f432-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f432-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2f432-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f432-107">ByObjectWithWithWithLyName</span><span class="sxs-lookup"><span data-stu-id="2f432-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f432-108">描述</span><span class="sxs-lookup"><span data-stu-id="2f432-108">DESCRIPTION</span></span>
<span data-ttu-id="2f432-109">**Get-AzRecoveryServicesrProtectionContainer** Cmdlet 會取得修復服務庫中的 Azure 網站復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="2f432-109">The **Get-AzRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="2f432-110">保護容器是可保護之 (容器) 及受保護物件 ，例如虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f432-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="2f432-111">複製原則會定義受保護專案的複製設定，而且可以與保護容器相關聯，並適用于受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="2f432-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="2f432-112">例子</span><span class="sxs-lookup"><span data-stu-id="2f432-112">EXAMPLES</span></span>

### <span data-ttu-id="2f432-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f432-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzRecoveryServicesAsrProtectionContainer -Fabric $fabric
```

<span data-ttu-id="2f432-114">布料中保護容器的清單$fabric。</span><span class="sxs-lookup"><span data-stu-id="2f432-114">List of protection container in fabric $fabric.</span></span>

### <span data-ttu-id="2f432-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="2f432-115">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
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

<span data-ttu-id="2f432-116">布料中的保護容器$fabric名稱。</span><span class="sxs-lookup"><span data-stu-id="2f432-116">Protection container in fabric $fabric with name.</span></span>

### <span data-ttu-id="2f432-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="2f432-117">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -FriendlyName xxxxxxxx  -Fabric $fabric
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

<span data-ttu-id="2f432-118">布料中的保護容器$fabric好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f432-118">Protection container in fabric $fabric with friendly Name.</span></span>

## <span data-ttu-id="2f432-119">參數</span><span class="sxs-lookup"><span data-stu-id="2f432-119">PARAMETERS</span></span>

### <span data-ttu-id="2f432-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f432-120">-DefaultProfile</span></span>
<span data-ttu-id="2f432-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f432-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2f432-122">-布料</span><span class="sxs-lookup"><span data-stu-id="2f432-122">-Fabric</span></span>
<span data-ttu-id="2f432-123">尋找指定 ASR 布料中的保護容器。</span><span class="sxs-lookup"><span data-stu-id="2f432-123">Look for the protection container in the specified ASR fabric.</span></span>

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

### <span data-ttu-id="2f432-124">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2f432-124">-FriendlyName</span></span>
<span data-ttu-id="2f432-125">指定要尋找的 ASR 保護容器的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="2f432-125">Specifies the friendly name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="2f432-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f432-126">-Name</span></span>
<span data-ttu-id="2f432-127">指定要尋找的 ASR 保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="2f432-127">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="2f432-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f432-128">CommonParameters</span></span>
<span data-ttu-id="2f432-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f432-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f432-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f432-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f432-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2f432-131">INPUTS</span></span>

### <span data-ttu-id="2f432-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2f432-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2f432-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2f432-133">OUTPUTS</span></span>

### <span data-ttu-id="2f432-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2f432-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="2f432-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2f432-135">NOTES</span></span>

## <span data-ttu-id="2f432-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f432-136">RELATED LINKS</span></span>
