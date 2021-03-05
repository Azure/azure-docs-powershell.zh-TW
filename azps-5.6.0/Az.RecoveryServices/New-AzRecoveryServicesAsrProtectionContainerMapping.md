---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f9fe364f680722b1fc34398f0e31a24f53a352ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917958"
---
# <span data-ttu-id="28cba-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="28cba-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="28cba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28cba-102">SYNOPSIS</span></span>
<span data-ttu-id="28cba-103">將指定的複本策略與指定的 ASR 保護容器建立關聯，以建立 Azure 網站復原保護容器的映射。</span><span class="sxs-lookup"><span data-stu-id="28cba-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="28cba-104">語法</span><span class="sxs-lookup"><span data-stu-id="28cba-104">SYNTAX</span></span>

### <span data-ttu-id="28cba-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="28cba-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cba-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="28cba-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cba-107">描述</span><span class="sxs-lookup"><span data-stu-id="28cba-107">DESCRIPTION</span></span>
<span data-ttu-id="28cba-108">**New-AzRecoveryServicesAsrProtectionContainerMadlet** Cmdlet 會建立 Azure 網站修復保護容器的關聯，將指定的複本策略與指定的保護容器建立關聯。</span><span class="sxs-lookup"><span data-stu-id="28cba-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="28cba-109">例子</span><span class="sxs-lookup"><span data-stu-id="28cba-109">EXAMPLES</span></span>

### <span data-ttu-id="28cba-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="28cba-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="28cba-111">開始建立具有指定參數的保護容器，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="28cba-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="28cba-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="28cba-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="28cba-113">開始建立具有指定參數的保護容器，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="28cba-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="28cba-114">參數</span><span class="sxs-lookup"><span data-stu-id="28cba-114">PARAMETERS</span></span>

### <span data-ttu-id="28cba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cba-115">-DefaultProfile</span></span>
<span data-ttu-id="28cba-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28cba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="28cba-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="28cba-117">-Name</span></span>
<span data-ttu-id="28cba-118">指定保護容器的映射名稱。</span><span class="sxs-lookup"><span data-stu-id="28cba-118">Specifies the name of the Protection Container mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cba-119">-策略</span><span class="sxs-lookup"><span data-stu-id="28cba-119">-Policy</span></span>
<span data-ttu-id="28cba-120">指定要用於地圖的複寫原則的 ASR 複寫原則物件。</span><span class="sxs-lookup"><span data-stu-id="28cba-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28cba-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="28cba-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="28cba-122">指定要用於地圖的主要保護容器的 ASR 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="28cba-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cba-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="28cba-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="28cba-124">指定要用於復原保護容器的 ASR 保護容器物件，用於 (如果複製到非 Azure.) 的復原位置時所使用的復原容器) </span><span class="sxs-lookup"><span data-stu-id="28cba-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cba-125">-確認</span><span class="sxs-lookup"><span data-stu-id="28cba-125">-Confirm</span></span>
<span data-ttu-id="28cba-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28cba-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cba-127">-WhatIf</span></span>
<span data-ttu-id="28cba-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28cba-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28cba-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28cba-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cba-130">CommonParameters</span></span>
<span data-ttu-id="28cba-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28cba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cba-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28cba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cba-133">輸入</span><span class="sxs-lookup"><span data-stu-id="28cba-133">INPUTS</span></span>

### <span data-ttu-id="28cba-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="28cba-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="28cba-135">輸出</span><span class="sxs-lookup"><span data-stu-id="28cba-135">OUTPUTS</span></span>

### <span data-ttu-id="28cba-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="28cba-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="28cba-137">筆記</span><span class="sxs-lookup"><span data-stu-id="28cba-137">NOTES</span></span>

## <span data-ttu-id="28cba-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="28cba-138">RELATED LINKS</span></span>

[<span data-ttu-id="28cba-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="28cba-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="28cba-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="28cba-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
