---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967474"
---
# <span data-ttu-id="c3827-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c3827-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="c3827-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3827-102">SYNOPSIS</span></span>
<span data-ttu-id="c3827-103">針對網站恢復保護實體啟動測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c3827-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="c3827-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3827-104">SYNTAX</span></span>

### <span data-ttu-id="c3827-105">ByPEId (預設) </span><span class="sxs-lookup"><span data-stu-id="c3827-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3827-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="c3827-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3827-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3827-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c3827-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c3827-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c3827-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3827-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c3827-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3827-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c3827-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3827-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="c3827-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c3827-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="c3827-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3827-121">說明</span><span class="sxs-lookup"><span data-stu-id="c3827-121">DESCRIPTION</span></span>
<span data-ttu-id="c3827-122">**Start-AzureSiteRecoveryTestFailoverJob** Cmdlet 會開始測試 Azure Site Recovery 保護實體或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c3827-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="c3827-123">您可以使用 **AzureRMSiteRecoveryJob** Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="c3827-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="c3827-124">示例</span><span class="sxs-lookup"><span data-stu-id="c3827-124">EXAMPLES</span></span>

### <span data-ttu-id="c3827-125">範例1：啟動測試容錯移轉</span><span class="sxs-lookup"><span data-stu-id="c3827-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="c3827-126">第一個命令使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 來取得受保護的容器，然後將它儲存在 $ProtectionContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="c3827-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="c3827-127">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet 來取得屬於儲存在 $ProtectionContainer 中之受保護容器的受保護實體。</span><span class="sxs-lookup"><span data-stu-id="c3827-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="c3827-128">該命令會將結果儲存在 $ProtectionEntity 變數中。</span><span class="sxs-lookup"><span data-stu-id="c3827-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="c3827-129">最終命令會針對儲存在 $ProtectionEntity 中的受保護實體啟動測試容錯移轉作業，並指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="c3827-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="c3827-130">範例2：使用恢復方案啟動測試容錯移轉</span><span class="sxs-lookup"><span data-stu-id="c3827-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="c3827-131">這個命令會透過 **AzureSiteRecoveryRecoveryPlan** Cmdlet，為目前的 Azure Site recovery 保存庫取得名為 RecoveryPlan01 的復原方案。</span><span class="sxs-lookup"><span data-stu-id="c3827-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="c3827-132">該命令會將計畫儲存在 $RecoveryPlan 變數中。</span><span class="sxs-lookup"><span data-stu-id="c3827-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="c3827-133">第二個命令會針對儲存在 $RecoveryPlan 的復原方案啟動測試容錯移轉作業，並指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="c3827-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="c3827-134">參數</span><span class="sxs-lookup"><span data-stu-id="c3827-134">PARAMETERS</span></span>

### <span data-ttu-id="c3827-135">方向</span><span class="sxs-lookup"><span data-stu-id="c3827-135">-Direction</span></span>
<span data-ttu-id="c3827-136">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="c3827-136">Specifies the failover direction.</span></span>
<span data-ttu-id="c3827-137">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c3827-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3827-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c3827-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="c3827-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c3827-139">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="c3827-140">-LogicalNetworkId</span></span>
<span data-ttu-id="c3827-141">指定邏輯網路的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3827-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-142">-網路</span><span class="sxs-lookup"><span data-stu-id="c3827-142">-Network</span></span>
<span data-ttu-id="c3827-143">指定要用於測試容錯移轉的網路物件。</span><span class="sxs-lookup"><span data-stu-id="c3827-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="c3827-144">若要取得網路，請使用 **AzureSiteRecoveryNetwork** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3827-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="c3827-145">-NetworkType</span></span>
<span data-ttu-id="c3827-146">指定要用於測試容錯移轉的網路類型。</span><span class="sxs-lookup"><span data-stu-id="c3827-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="c3827-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c3827-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3827-148">所有</span><span class="sxs-lookup"><span data-stu-id="c3827-148">None</span></span>
- <span data-ttu-id="c3827-149">新增功能</span><span class="sxs-lookup"><span data-stu-id="c3827-149">New</span></span>
- <span data-ttu-id="c3827-150">有</span><span class="sxs-lookup"><span data-stu-id="c3827-150">Existing</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-151">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c3827-151">-Profile</span></span>
<span data-ttu-id="c3827-152">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c3827-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3827-153">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c3827-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="c3827-154">-ProtectionContainerId</span></span>
<span data-ttu-id="c3827-155">指定受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3827-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="c3827-156">這個 Cmdlet 會針對屬於這個 Cmdlet 所指定容器的受保護虛擬機器啟動作業。</span><span class="sxs-lookup"><span data-stu-id="c3827-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c3827-157">-ProtectionEntity</span></span>
<span data-ttu-id="c3827-158">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="c3827-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="c3827-159">-ProtectionEntityId</span></span>
<span data-ttu-id="c3827-160">指定要啟動作業之受保護虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3827-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c3827-161">-RecoveryPlan</span></span>
<span data-ttu-id="c3827-162">指定要開始作業的復原方案。</span><span class="sxs-lookup"><span data-stu-id="c3827-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="c3827-163">-RpId</span></span>
<span data-ttu-id="c3827-164">指定要開始作業的復原方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3827-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="c3827-165">-VmNetworkId</span></span>
<span data-ttu-id="c3827-166">指定虛擬機器網路的 ID。</span><span class="sxs-lookup"><span data-stu-id="c3827-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c3827-167">-WaitForCompletion</span></span>
<span data-ttu-id="c3827-168">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="c3827-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3827-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3827-169">CommonParameters</span></span>
<span data-ttu-id="c3827-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3827-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3827-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3827-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3827-172">輸入</span><span class="sxs-lookup"><span data-stu-id="c3827-172">INPUTS</span></span>

## <span data-ttu-id="c3827-173">輸出</span><span class="sxs-lookup"><span data-stu-id="c3827-173">OUTPUTS</span></span>

## <span data-ttu-id="c3827-174">筆記</span><span class="sxs-lookup"><span data-stu-id="c3827-174">NOTES</span></span>

## <span data-ttu-id="c3827-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3827-175">RELATED LINKS</span></span>

[<span data-ttu-id="c3827-176">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c3827-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="c3827-177">AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="c3827-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="c3827-178">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c3827-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="c3827-179">AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c3827-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c3827-180">開始-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c3827-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


