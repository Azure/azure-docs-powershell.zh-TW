---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 41d023abbb1eb4453b295e64d1ccfc3b146fb197
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910393"
---
# <span data-ttu-id="f8808-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8808-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f8808-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8808-102">SYNOPSIS</span></span>
<span data-ttu-id="f8808-103">建立 ASR 復原計畫。</span><span class="sxs-lookup"><span data-stu-id="f8808-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="f8808-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8808-104">SYNTAX</span></span>

### <span data-ttu-id="f8808-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="f8808-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8808-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="f8808-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8808-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="f8808-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8808-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="f8808-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8808-109">描述</span><span class="sxs-lookup"><span data-stu-id="f8808-109">DESCRIPTION</span></span>
<span data-ttu-id="f8808-110">**New-AzRecoveryServicesAsrRecoveryPlan** Cmdlet 在修復服務庫中建立 Azure 網站復原、復原計畫。</span><span class="sxs-lookup"><span data-stu-id="f8808-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="f8808-111">復原計畫會將屬於應用程式的虛擬機器收集到一個單位中，以便一起復原。</span><span class="sxs-lookup"><span data-stu-id="f8808-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="f8808-112">例子</span><span class="sxs-lookup"><span data-stu-id="f8808-112">EXAMPLES</span></span>

### <span data-ttu-id="f8808-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f8808-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="f8808-114">使用指定的參數啟動復原計畫建立作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="f8808-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="f8808-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="f8808-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="f8808-116">針對 Azure 區域開始復原計畫建立作業，以將複本專案分區，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="f8808-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f8808-117">參數</span><span class="sxs-lookup"><span data-stu-id="f8808-117">PARAMETERS</span></span>

### <span data-ttu-id="f8808-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="f8808-118">-Azure</span></span>
<span data-ttu-id="f8808-119">參數參數會指定 Azure 到 Azure 的災害復原、復原計畫建立案例。</span><span class="sxs-lookup"><span data-stu-id="f8808-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="f8808-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="f8808-120">-AzureZoneToZone</span></span>
<span data-ttu-id="f8808-121">參數參數指定在 Azure 區域中建立複製的專案至區域分析藍本。</span><span class="sxs-lookup"><span data-stu-id="f8808-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

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

### <span data-ttu-id="f8808-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8808-122">-DefaultProfile</span></span>
<span data-ttu-id="f8808-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8808-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f8808-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="f8808-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="f8808-125">指定傳統 (或 Resource Manager) 屬於此復原計畫之複本保護專案的容錯移轉部署模型。</span><span class="sxs-lookup"><span data-stu-id="f8808-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="f8808-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8808-126">-Name</span></span>
<span data-ttu-id="f8808-127">復原計畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8808-127">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="f8808-128">-路徑</span><span class="sxs-lookup"><span data-stu-id="f8808-128">-Path</span></span>
<span data-ttu-id="f8808-129">指定復原計畫定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="f8808-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="f8808-130">修復計畫定義 json 可用來建立復原計畫。</span><span class="sxs-lookup"><span data-stu-id="f8808-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="f8808-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="f8808-131">-PrimaryFabric</span></span>
<span data-ttu-id="f8808-132">指定屬於此復原計畫之複本受保護專案之主要 ASR 結構物件的 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="f8808-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="f8808-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="f8808-133">-PrimaryZone</span></span>
<span data-ttu-id="f8808-134">指定屬於此復原計畫之複本保護專案的主要可用區域。</span><span class="sxs-lookup"><span data-stu-id="f8808-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="f8808-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="f8808-135">-RecoveryFabric</span></span>
<span data-ttu-id="f8808-136">指定將屬於此復原計畫之複本保護專案的 ASR 結構復原 ASR 結構物件。</span><span class="sxs-lookup"><span data-stu-id="f8808-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="f8808-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="f8808-137">-RecoveryZone</span></span>
<span data-ttu-id="f8808-138">指定屬於此復原計畫之複本保護專案的主要可用區域。</span><span class="sxs-lookup"><span data-stu-id="f8808-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="f8808-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f8808-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f8808-140">要新增到復原計畫第一個群組的複本保護專案清單。</span><span class="sxs-lookup"><span data-stu-id="f8808-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="f8808-141">-確認</span><span class="sxs-lookup"><span data-stu-id="f8808-141">-Confirm</span></span>
<span data-ttu-id="f8808-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f8808-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8808-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8808-143">-WhatIf</span></span>
<span data-ttu-id="f8808-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8808-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8808-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8808-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8808-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8808-146">CommonParameters</span></span>
<span data-ttu-id="f8808-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8808-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8808-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8808-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8808-149">輸入</span><span class="sxs-lookup"><span data-stu-id="f8808-149">INPUTS</span></span>

### <span data-ttu-id="f8808-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="f8808-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="f8808-151">輸出</span><span class="sxs-lookup"><span data-stu-id="f8808-151">OUTPUTS</span></span>

### <span data-ttu-id="f8808-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8808-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8808-153">筆記</span><span class="sxs-lookup"><span data-stu-id="f8808-153">NOTES</span></span>

## <span data-ttu-id="f8808-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8808-154">RELATED LINKS</span></span>

[<span data-ttu-id="f8808-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8808-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f8808-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8808-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f8808-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f8808-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


