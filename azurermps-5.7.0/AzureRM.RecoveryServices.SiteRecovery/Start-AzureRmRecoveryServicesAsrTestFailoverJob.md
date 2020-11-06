---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: bab9cb87f347b198b430c1dadc65a002dfa94141
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444423"
---
# <span data-ttu-id="0eee1-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0eee1-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="0eee1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0eee1-102">SYNOPSIS</span></span>
<span data-ttu-id="0eee1-103">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="0eee1-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eee1-104">句法</span><span class="sxs-lookup"><span data-stu-id="0eee1-104">SYNTAX</span></span>

### <span data-ttu-id="0eee1-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="0eee1-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eee1-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0eee1-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eee1-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0eee1-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eee1-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eee1-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eee1-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0eee1-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0eee1-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eee1-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0eee1-111">說明</span><span class="sxs-lookup"><span data-stu-id="0eee1-111">DESCRIPTION</span></span>
<span data-ttu-id="0eee1-112">**Start-AzureRmRecoveryServicesAsrTestFailoverJob** Cmdlet 會開始測試 Azure 網站復原複製受保護的專案或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0eee1-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="0eee1-113">您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0eee1-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="0eee1-114">示例</span><span class="sxs-lookup"><span data-stu-id="0eee1-114">EXAMPLES</span></span>

### <span data-ttu-id="0eee1-115">範例1</span><span class="sxs-lookup"><span data-stu-id="0eee1-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="0eee1-116">使用指定的參數為復原方案啟動測試容錯移轉作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="0eee1-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0eee1-117">參數</span><span class="sxs-lookup"><span data-stu-id="0eee1-117">PARAMETERS</span></span>

### <span data-ttu-id="0eee1-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0eee1-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="0eee1-119">指定 Azure 虛擬網路識別碼，以將測試的容錯移轉到虛擬機器 (s) 。</span><span class="sxs-lookup"><span data-stu-id="0eee1-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="0eee1-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="0eee1-121">指定是否應建立新的雲端服務，或針對 VM 設定的復原雲端服務應該用於測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0eee1-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-122">-確認</span><span class="sxs-lookup"><span data-stu-id="0eee1-122">-Confirm</span></span>
<span data-ttu-id="0eee1-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0eee1-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-124">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0eee1-124">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0eee1-125">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="0eee1-125">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="0eee1-126">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0eee1-126">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0eee1-127">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="0eee1-127">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="0eee1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eee1-128">-DefaultProfile</span></span>
<span data-ttu-id="0eee1-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0eee1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-130">方向</span><span class="sxs-lookup"><span data-stu-id="0eee1-130">-Direction</span></span>
<span data-ttu-id="0eee1-131">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="0eee1-131">Specifies the failover direction.</span></span>
<span data-ttu-id="0eee1-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0eee1-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0eee1-133">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0eee1-133">PrimaryToRecovery</span></span>
- <span data-ttu-id="0eee1-134">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0eee1-134">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-135">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0eee1-135">-RecoveryPlan</span></span>
<span data-ttu-id="0eee1-136">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="0eee1-136">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0eee1-137">-RecoveryPoint</span></span>
<span data-ttu-id="0eee1-138">指定要測試將受保護電腦容錯移轉到哪個自訂復原點。</span><span class="sxs-lookup"><span data-stu-id="0eee1-138">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-139">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="0eee1-139">-RecoveryTag</span></span>
<span data-ttu-id="0eee1-140">指定要測試容錯移轉的復原標記</span><span class="sxs-lookup"><span data-stu-id="0eee1-140">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-141">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0eee1-141">-ReplicationProtectedItem</span></span>
<span data-ttu-id="0eee1-142">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="0eee1-142">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-143">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="0eee1-143">-VMNetwork</span></span>
<span data-ttu-id="0eee1-144">指定網站復原虛擬機器網路，以將) 的測試容錯移轉虛擬機器 (s 連線。</span><span class="sxs-lookup"><span data-stu-id="0eee1-144">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eee1-145">-WhatIf</span></span>
<span data-ttu-id="0eee1-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0eee1-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0eee1-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eee1-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eee1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eee1-148">CommonParameters</span></span>
<span data-ttu-id="0eee1-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0eee1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eee1-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0eee1-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eee1-151">輸入</span><span class="sxs-lookup"><span data-stu-id="0eee1-151">INPUTS</span></span>

### <span data-ttu-id="0eee1-152">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0eee1-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="0eee1-153">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0eee1-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="0eee1-154">輸出</span><span class="sxs-lookup"><span data-stu-id="0eee1-154">OUTPUTS</span></span>

### <span data-ttu-id="0eee1-155">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0eee1-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0eee1-156">筆記</span><span class="sxs-lookup"><span data-stu-id="0eee1-156">NOTES</span></span>

## <span data-ttu-id="0eee1-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eee1-157">RELATED LINKS</span></span>

[<span data-ttu-id="0eee1-158">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="0eee1-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
