---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: be76705ab9b5a07b4d5bf654c897b6e396cf85c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903114"
---
# <span data-ttu-id="2bf26-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf26-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="2bf26-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2bf26-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf26-103">獲得 Azure 網站復原保護容器的映射。</span><span class="sxs-lookup"><span data-stu-id="2bf26-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="2bf26-104">語法</span><span class="sxs-lookup"><span data-stu-id="2bf26-104">SYNTAX</span></span>

### <span data-ttu-id="2bf26-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="2bf26-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bf26-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2bf26-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bf26-107">描述</span><span class="sxs-lookup"><span data-stu-id="2bf26-107">DESCRIPTION</span></span>
<span data-ttu-id="2bf26-108">**Get-AzRecoveryServicesAsrProtectionContainerMadlet** 會取得保護容器與指定 ASR 保護容器之 (關聯) 之複寫原則映射的資訊。</span><span class="sxs-lookup"><span data-stu-id="2bf26-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="2bf26-109">例子</span><span class="sxs-lookup"><span data-stu-id="2bf26-109">EXAMPLES</span></span>

### <span data-ttu-id="2bf26-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2bf26-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="2bf26-111">容器的保護容器映射清單。</span><span class="sxs-lookup"><span data-stu-id="2bf26-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="2bf26-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="2bf26-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="2bf26-113">為指定的保護容器獲取所有保護容器的映射。</span><span class="sxs-lookup"><span data-stu-id="2bf26-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="2bf26-114">參數</span><span class="sxs-lookup"><span data-stu-id="2bf26-114">PARAMETERS</span></span>

### <span data-ttu-id="2bf26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf26-115">-DefaultProfile</span></span>
<span data-ttu-id="2bf26-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bf26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2bf26-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bf26-117">-Name</span></span>
<span data-ttu-id="2bf26-118">指定要取得之保護容器的映射名稱。</span><span class="sxs-lookup"><span data-stu-id="2bf26-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="2bf26-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2bf26-119">-ProtectionContainer</span></span>
<span data-ttu-id="2bf26-120">取得對應至指定 ASR 保護容器物件的保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="2bf26-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="2bf26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf26-121">CommonParameters</span></span>
<span data-ttu-id="2bf26-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2bf26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf26-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bf26-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf26-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2bf26-124">INPUTS</span></span>

### <span data-ttu-id="2bf26-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2bf26-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="2bf26-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2bf26-126">OUTPUTS</span></span>

### <span data-ttu-id="2bf26-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf26-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="2bf26-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2bf26-128">NOTES</span></span>

## <span data-ttu-id="2bf26-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bf26-129">RELATED LINKS</span></span>

[<span data-ttu-id="2bf26-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf26-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="2bf26-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bf26-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
