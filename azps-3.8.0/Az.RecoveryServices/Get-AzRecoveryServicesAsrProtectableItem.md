---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: da9dd3d7b1ed0a54a34fdf5c8a0c9d65b507a07b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400598"
---
# <span data-ttu-id="651ae-101">Get-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="651ae-101">Get-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="651ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="651ae-102">SYNOPSIS</span></span>
<span data-ttu-id="651ae-103">在 ASR 保護容器中取得受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="651ae-103">Get the protectable items in an ASR protection container.</span></span>

## <span data-ttu-id="651ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="651ae-104">SYNTAX</span></span>

### <span data-ttu-id="651ae-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="651ae-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="651ae-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="651ae-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="651ae-107">ByObjectWithWithWithLyName</span><span class="sxs-lookup"><span data-stu-id="651ae-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="651ae-108">描述</span><span class="sxs-lookup"><span data-stu-id="651ae-108">DESCRIPTION</span></span>
<span data-ttu-id="651ae-109">**Get-AzRecoveryServicesrProtectableItem** Cmdlet 會取得 Azure 網站修復保護容器中的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="651ae-109">The **Get-AzRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="651ae-110">例子</span><span class="sxs-lookup"><span data-stu-id="651ae-110">EXAMPLES</span></span>

### <span data-ttu-id="651ae-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="651ae-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="651ae-112">在指定的 ASR 保護容器內，獲得所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="651ae-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="651ae-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="651ae-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="651ae-114">取得指定 ASR 保護容器和具有指定好用名稱的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="651ae-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="651ae-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="651ae-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="651ae-116">在指定的 ASR 保護容器內，獲得所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="651ae-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="651ae-117">參數</span><span class="sxs-lookup"><span data-stu-id="651ae-117">PARAMETERS</span></span>

### <span data-ttu-id="651ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651ae-118">-DefaultProfile</span></span>
<span data-ttu-id="651ae-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="651ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="651ae-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="651ae-120">-FriendlyName</span></span>
<span data-ttu-id="651ae-121">指定 ASR 可保護專案的好用名稱。</span><span class="sxs-lookup"><span data-stu-id="651ae-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="651ae-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="651ae-122">-Name</span></span>
<span data-ttu-id="651ae-123">指定 ASR 可保護專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="651ae-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="651ae-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="651ae-124">-ProtectionContainer</span></span>
<span data-ttu-id="651ae-125">指定 Azure 網站復原保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="651ae-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651ae-126">CommonParameters</span></span>
<span data-ttu-id="651ae-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="651ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651ae-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="651ae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651ae-129">輸入</span><span class="sxs-lookup"><span data-stu-id="651ae-129">INPUTS</span></span>

### <span data-ttu-id="651ae-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="651ae-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="651ae-131">輸出</span><span class="sxs-lookup"><span data-stu-id="651ae-131">OUTPUTS</span></span>

### <span data-ttu-id="651ae-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="651ae-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="651ae-133">筆記</span><span class="sxs-lookup"><span data-stu-id="651ae-133">NOTES</span></span>

## <span data-ttu-id="651ae-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="651ae-134">RELATED LINKS</span></span>


