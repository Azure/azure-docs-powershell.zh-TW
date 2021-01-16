---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437376"
---
# <span data-ttu-id="ff3eb-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ff3eb-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="ff3eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3eb-103">將指定的複製原則與指定的 ASR 保護容器產生關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="ff3eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff3eb-104">SYNTAX</span></span>

### <span data-ttu-id="ff3eb-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="ff3eb-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff3eb-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ff3eb-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff3eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="ff3eb-107">DESCRIPTION</span></span>
<span data-ttu-id="ff3eb-108">**新的-AzRecoveryServicesAsrProtectionContainerMapping** Cmdlet 會將指定的複製原則與指定的保護容器建立關聯，以建立 Azure Site Recovery 保護容器對應。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="ff3eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="ff3eb-109">EXAMPLES</span></span>

### <span data-ttu-id="ff3eb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ff3eb-110">Example 1</span></span>
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

<span data-ttu-id="ff3eb-111">使用指定的參數開始建立保護容器對應，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="ff3eb-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ff3eb-112">Example 2</span></span>
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

<span data-ttu-id="ff3eb-113">使用指定的參數開始建立保護容器對應，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ff3eb-114">參數</span><span class="sxs-lookup"><span data-stu-id="ff3eb-114">PARAMETERS</span></span>

### <span data-ttu-id="ff3eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3eb-115">-DefaultProfile</span></span>
<span data-ttu-id="ff3eb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ff3eb-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff3eb-117">-Name</span></span>
<span data-ttu-id="ff3eb-118">指定保護容器對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="ff3eb-119">-原則</span><span class="sxs-lookup"><span data-stu-id="ff3eb-119">-Policy</span></span>
<span data-ttu-id="ff3eb-120">指定要在對應中使用之複製原則的 ASR 複製原則物件。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="ff3eb-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff3eb-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="ff3eb-122">針對要在對應中使用的主要保護容器，指定 ASR 保護容器物件。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="ff3eb-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ff3eb-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="ff3eb-124">針對將在複製到非 Azure 的復原位置所使用的對應 (，指定要在所使用之對應中使用之 [恢復保護] 容器的 [ASR 保護] 容器物件。 ) </span><span class="sxs-lookup"><span data-stu-id="ff3eb-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="ff3eb-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ff3eb-125">-Confirm</span></span>
<span data-ttu-id="ff3eb-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3eb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3eb-127">-WhatIf</span></span>
<span data-ttu-id="ff3eb-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff3eb-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3eb-130">CommonParameters</span></span>
<span data-ttu-id="ff3eb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3eb-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ff3eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3eb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ff3eb-133">INPUTS</span></span>

### <span data-ttu-id="ff3eb-134">RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ff3eb-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="ff3eb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ff3eb-135">OUTPUTS</span></span>

### <span data-ttu-id="ff3eb-136">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ff3eb-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ff3eb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ff3eb-137">NOTES</span></span>

## <span data-ttu-id="ff3eb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff3eb-138">RELATED LINKS</span></span>

[<span data-ttu-id="ff3eb-139">AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ff3eb-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="ff3eb-140">移除-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ff3eb-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
