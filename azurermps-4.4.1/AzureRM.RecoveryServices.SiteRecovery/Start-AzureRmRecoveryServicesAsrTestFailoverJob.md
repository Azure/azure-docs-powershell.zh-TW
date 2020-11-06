---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453324"
---
# <span data-ttu-id="e0b5b-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e0b5b-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="e0b5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b5b-103">啟動測試容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0b5b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0b5b-104">SYNTAX</span></span>

### <span data-ttu-id="e0b5b-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="e0b5b-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b5b-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e0b5b-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0b5b-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e0b5b-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b5b-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e0b5b-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b5b-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="e0b5b-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b5b-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e0b5b-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0b5b-111">說明</span><span class="sxs-lookup"><span data-stu-id="e0b5b-111">DESCRIPTION</span></span>
<span data-ttu-id="e0b5b-112">**Start-AzureRmRecoveryServicesAsrTestFailoverJob** Cmdlet 會開始測試 Azure 網站復原複製受保護的專案或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="e0b5b-113">您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="e0b5b-114">示例</span><span class="sxs-lookup"><span data-stu-id="e0b5b-114">EXAMPLES</span></span>

### <span data-ttu-id="e0b5b-115">範例1</span><span class="sxs-lookup"><span data-stu-id="e0b5b-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="e0b5b-116">使用指定的參數為復原方案啟動測試容錯移轉作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e0b5b-117">參數</span><span class="sxs-lookup"><span data-stu-id="e0b5b-117">PARAMETERS</span></span>

### <span data-ttu-id="e0b5b-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="e0b5b-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="e0b5b-119">指定 Azure 虛擬網路識別碼，以將測試的容錯移轉到虛擬機器 (s) 。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

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

### <span data-ttu-id="e0b5b-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e0b5b-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="e0b5b-121">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="e0b5b-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="e0b5b-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="e0b5b-123">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="e0b5b-124">方向</span><span class="sxs-lookup"><span data-stu-id="e0b5b-124">-Direction</span></span>
<span data-ttu-id="e0b5b-125">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-125">Specifies the failover direction.</span></span>
<span data-ttu-id="e0b5b-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e0b5b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e0b5b-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e0b5b-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="e0b5b-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e0b5b-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="e0b5b-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0b5b-129">-RecoveryPlan</span></span>
<span data-ttu-id="e0b5b-130">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-130">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="e0b5b-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e0b5b-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e0b5b-132">指定 ASR 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-132">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="e0b5b-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="e0b5b-133">-VMNetwork</span></span>
<span data-ttu-id="e0b5b-134">指定網站復原虛擬機器網路，以將) 的測試容錯移轉虛擬機器 (s 連線。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="e0b5b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="e0b5b-135">-Confirm</span></span>
<span data-ttu-id="e0b5b-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b5b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b5b-137">-WhatIf</span></span>
<span data-ttu-id="e0b5b-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0b5b-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b5b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b5b-140">CommonParameters</span></span>
<span data-ttu-id="e0b5b-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b5b-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0b5b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b5b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="e0b5b-143">INPUTS</span></span>

### <span data-ttu-id="e0b5b-144">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e0b5b-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="e0b5b-145">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e0b5b-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e0b5b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="e0b5b-146">OUTPUTS</span></span>

### <span data-ttu-id="e0b5b-147">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e0b5b-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e0b5b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="e0b5b-148">NOTES</span></span>

## <span data-ttu-id="e0b5b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0b5b-149">RELATED LINKS</span></span>

[<span data-ttu-id="e0b5b-150">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e0b5b-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
