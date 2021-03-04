---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: b5a06683e5254077a63d4c0b1933d51d9c1ad8e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910926"
---
# <span data-ttu-id="2ff15-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="2ff15-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="2ff15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2ff15-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff15-103">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="2ff15-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="2ff15-104">語法</span><span class="sxs-lookup"><span data-stu-id="2ff15-104">SYNTAX</span></span>

### <span data-ttu-id="2ff15-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="2ff15-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff15-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="2ff15-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff15-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="2ff15-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff15-108">ByRPObjectWithAzureEVNETworkId</span><span class="sxs-lookup"><span data-stu-id="2ff15-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff15-109">ByRPIObjectWithNETNETwork</span><span class="sxs-lookup"><span data-stu-id="2ff15-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ff15-110">ByRPIObjectWithAzureEVNETworkId</span><span class="sxs-lookup"><span data-stu-id="2ff15-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ff15-111">描述</span><span class="sxs-lookup"><span data-stu-id="2ff15-111">DESCRIPTION</span></span>
<span data-ttu-id="2ff15-112">**Start-AzRecoveryServicesrTestFailoverJob** Cmdlet 會啟動 Azure 網站復原複本保護專案或復原計畫的測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="2ff15-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="2ff15-113">您可以使用 Cmdlet 檢查工作是否Get-AzRecoveryServicesAsrJob成功。</span><span class="sxs-lookup"><span data-stu-id="2ff15-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="2ff15-114">例子</span><span class="sxs-lookup"><span data-stu-id="2ff15-114">EXAMPLES</span></span>

### <span data-ttu-id="2ff15-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="2ff15-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="2ff15-116">使用指定的參數啟動復原計畫的測試容錯移轉作業，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="2ff15-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2ff15-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="2ff15-117">Example 2</span></span>

<span data-ttu-id="2ff15-118">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="2ff15-118">Starts a test failover operation.</span></span> <span data-ttu-id="2ff15-119"> (自動) </span><span class="sxs-lookup"><span data-stu-id="2ff15-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="2ff15-120">參數</span><span class="sxs-lookup"><span data-stu-id="2ff15-120">PARAMETERS</span></span>

### <span data-ttu-id="2ff15-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="2ff15-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="2ff15-122">指定容錯移轉後復原 VM 的 Azure vm 網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ff15-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="2ff15-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="2ff15-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="2ff15-124">指定是否應該建立新的雲端服務，或應該使用為 VM 所配置的復原雲端服務進行測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="2ff15-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="2ff15-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="2ff15-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="2ff15-126">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="2ff15-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="2ff15-127">-DataEncryption二元CertFile</span><span class="sxs-lookup"><span data-stu-id="2ff15-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="2ff15-128">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="2ff15-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="2ff15-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff15-129">-DefaultProfile</span></span>
<span data-ttu-id="2ff15-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ff15-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2ff15-131">-方向</span><span class="sxs-lookup"><span data-stu-id="2ff15-131">-Direction</span></span>
<span data-ttu-id="2ff15-132">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="2ff15-132">Specifies the failover direction.</span></span>
<span data-ttu-id="2ff15-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2ff15-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ff15-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="2ff15-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="2ff15-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="2ff15-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="2ff15-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ff15-136">-RecoveryPlan</span></span>
<span data-ttu-id="2ff15-137">指定 ASR 復原計畫物件。</span><span class="sxs-lookup"><span data-stu-id="2ff15-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="2ff15-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2ff15-138">-RecoveryPoint</span></span>
<span data-ttu-id="2ff15-139">指定自訂修復點以測試受保護電腦容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="2ff15-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="2ff15-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="2ff15-140">-RecoveryTag</span></span>
<span data-ttu-id="2ff15-141">指定要測試容錯移轉的修復標記</span><span class="sxs-lookup"><span data-stu-id="2ff15-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="2ff15-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ff15-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2ff15-143">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="2ff15-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="2ff15-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="2ff15-144">-VMNetwork</span></span>
<span data-ttu-id="2ff15-145">指定網站復原虛擬機器網路，以將測試容錯移轉虛擬機器 () 。</span><span class="sxs-lookup"><span data-stu-id="2ff15-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="2ff15-146">-確認</span><span class="sxs-lookup"><span data-stu-id="2ff15-146">-Confirm</span></span>
<span data-ttu-id="2ff15-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2ff15-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff15-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff15-148">-WhatIf</span></span>
<span data-ttu-id="2ff15-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ff15-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ff15-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ff15-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff15-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff15-151">CommonParameters</span></span>
<span data-ttu-id="2ff15-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2ff15-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff15-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ff15-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff15-154">輸入</span><span class="sxs-lookup"><span data-stu-id="2ff15-154">INPUTS</span></span>

### <span data-ttu-id="2ff15-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2ff15-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="2ff15-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2ff15-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2ff15-157">輸出</span><span class="sxs-lookup"><span data-stu-id="2ff15-157">OUTPUTS</span></span>

### <span data-ttu-id="2ff15-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="2ff15-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2ff15-159">筆記</span><span class="sxs-lookup"><span data-stu-id="2ff15-159">NOTES</span></span>

## <span data-ttu-id="2ff15-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ff15-160">RELATED LINKS</span></span>

[<span data-ttu-id="2ff15-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="2ff15-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
