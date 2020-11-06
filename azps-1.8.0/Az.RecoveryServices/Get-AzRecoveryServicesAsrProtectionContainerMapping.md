---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 588c00dc877c4e451a4d8a0c0b44ec001b0787ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621176"
---
# <span data-ttu-id="d53c0-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d53c0-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d53c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d53c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d53c0-103">取得 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="d53c0-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="d53c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d53c0-104">SYNTAX</span></span>

### <span data-ttu-id="d53c0-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d53c0-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d53c0-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d53c0-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d53c0-107">說明</span><span class="sxs-lookup"><span data-stu-id="d53c0-107">DESCRIPTION</span></span>
<span data-ttu-id="d53c0-108">**AzRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會針對指定的 ASR 保護容器，取得保存庫中針對複製原則對應 (關聯性) 的保護容器資訊。</span><span class="sxs-lookup"><span data-stu-id="d53c0-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="d53c0-109">示例</span><span class="sxs-lookup"><span data-stu-id="d53c0-109">EXAMPLES</span></span>

### <span data-ttu-id="d53c0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d53c0-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="d53c0-111">容器的保護容器對應清單。</span><span class="sxs-lookup"><span data-stu-id="d53c0-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="d53c0-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d53c0-112">Example 2</span></span>
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

<span data-ttu-id="d53c0-113">取得指定保護容器的所有保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="d53c0-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="d53c0-114">參數</span><span class="sxs-lookup"><span data-stu-id="d53c0-114">PARAMETERS</span></span>

### <span data-ttu-id="d53c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53c0-115">-DefaultProfile</span></span>
<span data-ttu-id="d53c0-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d53c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d53c0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d53c0-117">-Name</span></span>
<span data-ttu-id="d53c0-118">指定要取得之保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="d53c0-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="d53c0-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d53c0-119">-ProtectionContainer</span></span>
<span data-ttu-id="d53c0-120">取得與指定的 ASR 保護容器物件相對應的保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="d53c0-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="d53c0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53c0-121">CommonParameters</span></span>
<span data-ttu-id="d53c0-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d53c0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53c0-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d53c0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53c0-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d53c0-124">INPUTS</span></span>

### <span data-ttu-id="d53c0-125">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d53c0-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d53c0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d53c0-126">OUTPUTS</span></span>

### <span data-ttu-id="d53c0-127">RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d53c0-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="d53c0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d53c0-128">NOTES</span></span>

## <span data-ttu-id="d53c0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d53c0-129">RELATED LINKS</span></span>

[<span data-ttu-id="d53c0-130">新-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d53c0-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d53c0-131">移除-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d53c0-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
