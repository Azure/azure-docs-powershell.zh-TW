---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: f0350cfa9facfe8fc21e6c039c2fa5838bba8875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448953"
---
# <span data-ttu-id="0d837-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0d837-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="0d837-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d837-102">SYNOPSIS</span></span>
<span data-ttu-id="0d837-103">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="0d837-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d837-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d837-104">SYNTAX</span></span>

### <span data-ttu-id="0d837-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="0d837-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d837-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0d837-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d837-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0d837-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d837-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0d837-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d837-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0d837-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d837-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0d837-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d837-111">說明</span><span class="sxs-lookup"><span data-stu-id="0d837-111">DESCRIPTION</span></span>
<span data-ttu-id="0d837-112">**Start-AzureRmRecoveryServicesAsrTestFailoverJob** Cmdlet 會開始測試 Azure 網站復原複製受保護的專案或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0d837-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="0d837-113">您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0d837-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="0d837-114">示例</span><span class="sxs-lookup"><span data-stu-id="0d837-114">EXAMPLES</span></span>

### <span data-ttu-id="0d837-115">範例1</span><span class="sxs-lookup"><span data-stu-id="0d837-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="0d837-116">使用指定的參數為復原方案啟動測試容錯移轉作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="0d837-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0d837-117">參數</span><span class="sxs-lookup"><span data-stu-id="0d837-117">PARAMETERS</span></span>

### <span data-ttu-id="0d837-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0d837-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="0d837-119">指定 Azure 虛擬網路識別碼，以將測試的容錯移轉到虛擬機器 (s) 。</span><span class="sxs-lookup"><span data-stu-id="0d837-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

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

### <span data-ttu-id="0d837-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="0d837-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="0d837-121">指定是否應建立新的雲端服務，或針對 VM 設定的復原雲端服務應該用於測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0d837-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="0d837-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0d837-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0d837-123">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="0d837-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="0d837-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0d837-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0d837-125">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="0d837-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="0d837-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d837-126">-DefaultProfile</span></span>
<span data-ttu-id="0d837-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d837-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0d837-128">方向</span><span class="sxs-lookup"><span data-stu-id="0d837-128">-Direction</span></span>
<span data-ttu-id="0d837-129">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="0d837-129">Specifies the failover direction.</span></span>
<span data-ttu-id="0d837-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0d837-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d837-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0d837-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="0d837-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0d837-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="0d837-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0d837-133">-RecoveryPlan</span></span>
<span data-ttu-id="0d837-134">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="0d837-134">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="0d837-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0d837-135">-RecoveryPoint</span></span>
<span data-ttu-id="0d837-136">指定要測試將受保護電腦容錯移轉到哪個自訂復原點。</span><span class="sxs-lookup"><span data-stu-id="0d837-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="0d837-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0d837-137">-RecoveryTag</span></span>
<span data-ttu-id="0d837-138">指定要測試容錯移轉的復原標記</span><span class="sxs-lookup"><span data-stu-id="0d837-138">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="0d837-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0d837-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0d837-140">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="0d837-140">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="0d837-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="0d837-141">-VMNetwork</span></span>
<span data-ttu-id="0d837-142">指定網站復原虛擬機器網路，以將) 的測試容錯移轉虛擬機器 (s 連線。</span><span class="sxs-lookup"><span data-stu-id="0d837-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="0d837-143">-確認</span><span class="sxs-lookup"><span data-stu-id="0d837-143">-Confirm</span></span>
<span data-ttu-id="0d837-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d837-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d837-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d837-145">-WhatIf</span></span>
<span data-ttu-id="0d837-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d837-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d837-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d837-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d837-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d837-148">CommonParameters</span></span>
<span data-ttu-id="0d837-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d837-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d837-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d837-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d837-151">輸入</span><span class="sxs-lookup"><span data-stu-id="0d837-151">INPUTS</span></span>

### <span data-ttu-id="0d837-152">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0d837-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="0d837-153">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0d837-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0d837-154">輸出</span><span class="sxs-lookup"><span data-stu-id="0d837-154">OUTPUTS</span></span>

### <span data-ttu-id="0d837-155">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0d837-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0d837-156">筆記</span><span class="sxs-lookup"><span data-stu-id="0d837-156">NOTES</span></span>

## <span data-ttu-id="0d837-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d837-157">RELATED LINKS</span></span>

[<span data-ttu-id="0d837-158">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0d837-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
