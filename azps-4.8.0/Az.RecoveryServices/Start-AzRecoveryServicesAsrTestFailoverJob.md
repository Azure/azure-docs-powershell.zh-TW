---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969128"
---
# <span data-ttu-id="8d36c-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8d36c-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="8d36c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d36c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d36c-103">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="8d36c-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="8d36c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d36c-104">SYNTAX</span></span>

### <span data-ttu-id="8d36c-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="8d36c-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d36c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8d36c-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d36c-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8d36c-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d36c-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d36c-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d36c-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="8d36c-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d36c-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d36c-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d36c-111">說明</span><span class="sxs-lookup"><span data-stu-id="8d36c-111">DESCRIPTION</span></span>
<span data-ttu-id="8d36c-112">**Start-AzRecoveryServicesAsrTestFailoverJob** Cmdlet 會開始測試 Azure 網站復原複製受保護的專案或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="8d36c-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="8d36c-113">您可以使用 Get-AzRecoveryServicesAsrJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="8d36c-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="8d36c-114">示例</span><span class="sxs-lookup"><span data-stu-id="8d36c-114">EXAMPLES</span></span>

### <span data-ttu-id="8d36c-115">範例1</span><span class="sxs-lookup"><span data-stu-id="8d36c-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="8d36c-116">使用指定的參數為復原方案啟動測試容錯移轉作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="8d36c-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="8d36c-117">範例2</span><span class="sxs-lookup"><span data-stu-id="8d36c-117">Example 2</span></span>

<span data-ttu-id="8d36c-118">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="8d36c-118">Starts a test failover operation.</span></span> <span data-ttu-id="8d36c-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="8d36c-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="8d36c-120">參數</span><span class="sxs-lookup"><span data-stu-id="8d36c-120">PARAMETERS</span></span>

### <span data-ttu-id="8d36c-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d36c-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="8d36c-122">指定容錯移轉之後的 [恢復 VM 的 Azure vm 網路識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8d36c-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="8d36c-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="8d36c-124">指定是否應建立新的雲端服務，或針對 VM 設定的復原雲端服務應該用於測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="8d36c-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8d36c-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8d36c-126">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="8d36c-126">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8d36c-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8d36c-128">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="8d36c-128">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d36c-129">-DefaultProfile</span></span>
<span data-ttu-id="8d36c-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d36c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8d36c-131">方向</span><span class="sxs-lookup"><span data-stu-id="8d36c-131">-Direction</span></span>
<span data-ttu-id="8d36c-132">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="8d36c-132">Specifies the failover direction.</span></span>
<span data-ttu-id="8d36c-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8d36c-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d36c-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8d36c-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="8d36c-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8d36c-135">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8d36c-136">-RecoveryPlan</span></span>
<span data-ttu-id="8d36c-137">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="8d36c-137">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8d36c-138">-RecoveryPoint</span></span>
<span data-ttu-id="8d36c-139">指定要測試將受保護電腦容錯移轉到哪個自訂復原點。</span><span class="sxs-lookup"><span data-stu-id="8d36c-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="8d36c-140">-RecoveryTag</span></span>
<span data-ttu-id="8d36c-141">指定要測試容錯移轉的復原標記</span><span class="sxs-lookup"><span data-stu-id="8d36c-141">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d36c-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8d36c-143">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="8d36c-143">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="8d36c-144">-VMNetwork</span></span>
<span data-ttu-id="8d36c-145">指定網站復原虛擬機器網路，以將) 的測試容錯移轉虛擬機器 (s 連線。</span><span class="sxs-lookup"><span data-stu-id="8d36c-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d36c-146">-確認</span><span class="sxs-lookup"><span data-stu-id="8d36c-146">-Confirm</span></span>
<span data-ttu-id="8d36c-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d36c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d36c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d36c-148">-WhatIf</span></span>
<span data-ttu-id="8d36c-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d36c-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d36c-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d36c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d36c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d36c-151">CommonParameters</span></span>
<span data-ttu-id="8d36c-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d36c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d36c-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d36c-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d36c-154">輸入</span><span class="sxs-lookup"><span data-stu-id="8d36c-154">INPUTS</span></span>

### <span data-ttu-id="8d36c-155">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8d36c-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="8d36c-156">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d36c-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8d36c-157">輸出</span><span class="sxs-lookup"><span data-stu-id="8d36c-157">OUTPUTS</span></span>

### <span data-ttu-id="8d36c-158">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8d36c-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8d36c-159">筆記</span><span class="sxs-lookup"><span data-stu-id="8d36c-159">NOTES</span></span>

## <span data-ttu-id="8d36c-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d36c-160">RELATED LINKS</span></span>

[<span data-ttu-id="8d36c-161">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8d36c-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
