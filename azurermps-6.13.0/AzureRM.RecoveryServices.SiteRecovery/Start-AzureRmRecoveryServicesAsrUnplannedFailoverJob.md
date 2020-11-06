---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: b7a9dffe443ca7603b8b5a3bdd100560d83a498e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445540"
---
# <span data-ttu-id="d59bd-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d59bd-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="d59bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d59bd-102">SYNOPSIS</span></span>
<span data-ttu-id="d59bd-103">啟動未計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="d59bd-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d59bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="d59bd-104">SYNTAX</span></span>

### <span data-ttu-id="d59bd-105">ByRPIObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d59bd-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d59bd-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d59bd-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d59bd-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d59bd-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d59bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="d59bd-108">DESCRIPTION</span></span>
<span data-ttu-id="d59bd-109">**Start-AzureRmRecoveryServicesAsrTestFailoverJob** Cmdlet 會開始測試 Azure 網站復原複製受保護的專案或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="d59bd-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="d59bd-110">您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d59bd-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="d59bd-111">示例</span><span class="sxs-lookup"><span data-stu-id="d59bd-111">EXAMPLES</span></span>

### <span data-ttu-id="d59bd-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d59bd-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="d59bd-113">使用指定的參數為復原方案啟動測試容錯移轉作業，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="d59bd-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d59bd-114">參數</span><span class="sxs-lookup"><span data-stu-id="d59bd-114">PARAMETERS</span></span>

### <span data-ttu-id="d59bd-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d59bd-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="d59bd-116">指定受保護專案容錯移轉的資料加密主要憑證檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d59bd-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d59bd-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d59bd-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="d59bd-118">指定受保護專案容錯移轉的資料加密次要憑證檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="d59bd-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d59bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59bd-119">-DefaultProfile</span></span>
<span data-ttu-id="d59bd-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d59bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d59bd-121">方向</span><span class="sxs-lookup"><span data-stu-id="d59bd-121">-Direction</span></span>
<span data-ttu-id="d59bd-122">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="d59bd-122">Specifies the failover direction.</span></span>
<span data-ttu-id="d59bd-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d59bd-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d59bd-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d59bd-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="d59bd-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d59bd-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="d59bd-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="d59bd-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="d59bd-127">在開始未計畫的容錯移轉前，請在源端執行操作。</span><span class="sxs-lookup"><span data-stu-id="d59bd-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59bd-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d59bd-128">-RecoveryPlan</span></span>
<span data-ttu-id="d59bd-129">指定 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="d59bd-129">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d59bd-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d59bd-130">-RecoveryPoint</span></span>
<span data-ttu-id="d59bd-131">指定要將受保護電腦容錯移轉至其中的自訂復原點。</span><span class="sxs-lookup"><span data-stu-id="d59bd-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59bd-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d59bd-132">-RecoveryTag</span></span>
<span data-ttu-id="d59bd-133">指定要容錯移轉至的復原標記。</span><span class="sxs-lookup"><span data-stu-id="d59bd-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59bd-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d59bd-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d59bd-135">指定 azure site recovery 複製受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="d59bd-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d59bd-136">-確認</span><span class="sxs-lookup"><span data-stu-id="d59bd-136">-Confirm</span></span>
<span data-ttu-id="d59bd-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d59bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d59bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d59bd-138">-WhatIf</span></span>
<span data-ttu-id="d59bd-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d59bd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d59bd-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d59bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d59bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59bd-141">CommonParameters</span></span>
<span data-ttu-id="d59bd-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d59bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59bd-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d59bd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59bd-144">輸入</span><span class="sxs-lookup"><span data-stu-id="d59bd-144">INPUTS</span></span>

### <span data-ttu-id="d59bd-145">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d59bd-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="d59bd-146">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d59bd-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d59bd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d59bd-147">OUTPUTS</span></span>

### <span data-ttu-id="d59bd-148">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d59bd-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d59bd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d59bd-149">NOTES</span></span>

## <span data-ttu-id="d59bd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d59bd-150">RELATED LINKS</span></span>

[<span data-ttu-id="d59bd-151">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d59bd-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
