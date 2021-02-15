---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135447"
---
# <span data-ttu-id="9d149-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d149-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9d149-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d149-102">SYNOPSIS</span></span>
<span data-ttu-id="9d149-103">建立 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="9d149-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="9d149-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d149-104">SYNTAX</span></span>

### <span data-ttu-id="9d149-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="9d149-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d149-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="9d149-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d149-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="9d149-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d149-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="9d149-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d149-109">說明</span><span class="sxs-lookup"><span data-stu-id="9d149-109">DESCRIPTION</span></span>
<span data-ttu-id="9d149-110">**新的-AzRecoveryServicesAsrRecoveryPlan** Cmdlet 會在復原服務電子倉庫中建立 Azure Site recovery、復原方案。</span><span class="sxs-lookup"><span data-stu-id="9d149-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="9d149-111">復原方案會將屬於應用程式的虛擬機器收集到單元中，讓它們能夠一起復原。</span><span class="sxs-lookup"><span data-stu-id="9d149-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="9d149-112">示例</span><span class="sxs-lookup"><span data-stu-id="9d149-112">EXAMPLES</span></span>

### <span data-ttu-id="9d149-113">範例1</span><span class="sxs-lookup"><span data-stu-id="9d149-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="9d149-114">使用指定的參數啟動復原方案建立作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="9d149-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="9d149-115">範例2</span><span class="sxs-lookup"><span data-stu-id="9d149-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="9d149-116">開始針對 Azure zone 的復原方案建立作業來區域複製的專案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="9d149-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9d149-117">參數</span><span class="sxs-lookup"><span data-stu-id="9d149-117">PARAMETERS</span></span>

### <span data-ttu-id="9d149-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="9d149-118">-Azure</span></span>
<span data-ttu-id="9d149-119">Switch 參數指定 azure 到 azure 災害復原的案例，以及如何建立恢復方案。</span><span class="sxs-lookup"><span data-stu-id="9d149-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="9d149-120">-AzureZoneToZone</span></span>
<span data-ttu-id="9d149-121">Switch 參數指定在 azure zone 中建立複製專案至 zone 案例。</span><span class="sxs-lookup"><span data-stu-id="9d149-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d149-122">-DefaultProfile</span></span>
<span data-ttu-id="9d149-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d149-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9d149-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="9d149-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="9d149-125">指定將成為此復原方案一部分之複製受保護專案 (傳統或資源管理員) 的容錯移轉部署模型。</span><span class="sxs-lookup"><span data-stu-id="9d149-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d149-126">-Name</span></span>
<span data-ttu-id="9d149-127">修復方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d149-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-128">-Path</span><span class="sxs-lookup"><span data-stu-id="9d149-128">-Path</span></span>
<span data-ttu-id="9d149-129">指定恢復方案定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9d149-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="9d149-130">復原方案定義 json 可以用來建立復原方案。</span><span class="sxs-lookup"><span data-stu-id="9d149-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="9d149-131">-PrimaryFabric</span></span>
<span data-ttu-id="9d149-132">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件的初始 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="9d149-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="9d149-133">-PrimaryZone</span></span>
<span data-ttu-id="9d149-134">指定將成為此復原方案一部分之複製受保護專案的主要 Availabilty 區域。</span><span class="sxs-lookup"><span data-stu-id="9d149-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="9d149-135">-RecoveryFabric</span></span>
<span data-ttu-id="9d149-136">針對將成為此復原方案一部分之複製受保護專案，指定 ASR fabric 物件來取得恢復 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="9d149-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="9d149-137">-RecoveryZone</span></span>
<span data-ttu-id="9d149-138">指定將成為此復原方案一部分之複製受保護專案的主要 Availabilty 區域。</span><span class="sxs-lookup"><span data-stu-id="9d149-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9d149-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9d149-140">要新增至第一個恢復方案群組的複製受保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="9d149-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d149-141">-確認</span><span class="sxs-lookup"><span data-stu-id="9d149-141">-Confirm</span></span>
<span data-ttu-id="9d149-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d149-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d149-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d149-143">-WhatIf</span></span>
<span data-ttu-id="9d149-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d149-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d149-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d149-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d149-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d149-146">CommonParameters</span></span>
<span data-ttu-id="9d149-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d149-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d149-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d149-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d149-149">輸入</span><span class="sxs-lookup"><span data-stu-id="9d149-149">INPUTS</span></span>

### <span data-ttu-id="9d149-150">ASRReplicationProtectedItem []. RecoveryServices. SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9d149-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="9d149-151">輸出</span><span class="sxs-lookup"><span data-stu-id="9d149-151">OUTPUTS</span></span>

### <span data-ttu-id="9d149-152">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9d149-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9d149-153">筆記</span><span class="sxs-lookup"><span data-stu-id="9d149-153">NOTES</span></span>

## <span data-ttu-id="9d149-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d149-154">RELATED LINKS</span></span>

[<span data-ttu-id="9d149-155">AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d149-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9d149-156">移除-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d149-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9d149-157">更新-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d149-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


