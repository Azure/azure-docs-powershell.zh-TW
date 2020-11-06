---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 72f94dca73a1d99adf2d5cced50be9122ff2e7d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451079"
---
# <span data-ttu-id="9df8e-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9df8e-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="9df8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9df8e-102">SYNOPSIS</span></span>
<span data-ttu-id="9df8e-103">在 ASR 保護容器中取得可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9df8e-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9df8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9df8e-104">SYNTAX</span></span>

### <span data-ttu-id="9df8e-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="9df8e-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9df8e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="9df8e-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9df8e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9df8e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9df8e-108">說明</span><span class="sxs-lookup"><span data-stu-id="9df8e-108">DESCRIPTION</span></span>
<span data-ttu-id="9df8e-109">**AzureRmRecoveryServicesAsrProtectableItem** Cmdlet 會取得 Azure Site Recovery 保護容器中的可保護專案。</span><span class="sxs-lookup"><span data-stu-id="9df8e-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="9df8e-110">示例</span><span class="sxs-lookup"><span data-stu-id="9df8e-110">EXAMPLES</span></span>

### <span data-ttu-id="9df8e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9df8e-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="9df8e-112">在指定的 ASR 保護容器中取得所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9df8e-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="9df8e-113">範例2</span><span class="sxs-lookup"><span data-stu-id="9df8e-113">Example 2</span></span>
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

<span data-ttu-id="9df8e-114">在指定的 ASR 保護容器中，以指定的易記名稱取得可以保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9df8e-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="9df8e-115">範例3</span><span class="sxs-lookup"><span data-stu-id="9df8e-115">Example 3</span></span>
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

<span data-ttu-id="9df8e-116">在指定的 ASR 保護容器中取得所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="9df8e-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="9df8e-117">參數</span><span class="sxs-lookup"><span data-stu-id="9df8e-117">PARAMETERS</span></span>

### <span data-ttu-id="9df8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df8e-118">-DefaultProfile</span></span>
<span data-ttu-id="9df8e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9df8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9df8e-120">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9df8e-120">-FriendlyName</span></span>
<span data-ttu-id="9df8e-121">指定 ASR [能保護的專案] 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9df8e-121">Specifies the friendly name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="9df8e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9df8e-122">-Name</span></span>
<span data-ttu-id="9df8e-123">指定 ASR [能保護的專案] 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9df8e-123">Specifies the name of the ASR protectable item.</span></span>

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

### <span data-ttu-id="9df8e-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9df8e-124">-ProtectionContainer</span></span>
<span data-ttu-id="9df8e-125">指定 Azure Site Recovery 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="9df8e-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="9df8e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df8e-126">CommonParameters</span></span>
<span data-ttu-id="9df8e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9df8e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df8e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9df8e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df8e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9df8e-129">INPUTS</span></span>

### <span data-ttu-id="9df8e-130">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9df8e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="9df8e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9df8e-131">OUTPUTS</span></span>

### <span data-ttu-id="9df8e-132">System.object. IEnumerable "1 [ASRProtectableItem，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="9df8e-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9df8e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9df8e-133">NOTES</span></span>

## <span data-ttu-id="9df8e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9df8e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9df8e-135">AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9df8e-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="9df8e-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9df8e-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)
