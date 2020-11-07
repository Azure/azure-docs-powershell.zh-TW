---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967197"
---
# <span data-ttu-id="b4a59-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b4a59-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="b4a59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4a59-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a59-103">啟動網站復原計畫的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="b4a59-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="b4a59-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4a59-104">SYNTAX</span></span>

### <span data-ttu-id="b4a59-105">ByRPId (預設) </span><span class="sxs-lookup"><span data-stu-id="b4a59-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b4a59-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="b4a59-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b4a59-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b4a59-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b4a59-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="b4a59-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4a59-109">說明</span><span class="sxs-lookup"><span data-stu-id="b4a59-109">DESCRIPTION</span></span>
<span data-ttu-id="b4a59-110">**AzureSiteRecoveryPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 保護實體或復原方案啟動計畫的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b4a59-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="b4a59-111">您可以使用 **AzureSiteRecoveryJob** Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="b4a59-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="b4a59-112">示例</span><span class="sxs-lookup"><span data-stu-id="b4a59-112">EXAMPLES</span></span>

### <span data-ttu-id="b4a59-113">範例1：啟動計畫的容錯移轉作業</span><span class="sxs-lookup"><span data-stu-id="b4a59-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
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

<span data-ttu-id="b4a59-114">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet，在目前的 Azure Site Recovery 保存庫中取得所有受保護的容器，然後將結果儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="b4a59-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="b4a59-115">在這個範例中，只有一個容器。</span><span class="sxs-lookup"><span data-stu-id="b4a59-115">In this example, there is a single container.</span></span>

<span data-ttu-id="b4a59-116">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet，來取得屬於儲存在 $Container 中之容器的受保護虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b4a59-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="b4a59-117">該命令會將結果儲存在 $Protected 變數中。</span><span class="sxs-lookup"><span data-stu-id="b4a59-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="b4a59-118">最終命令會針對儲存在 $Protected 中之受保護的虛擬機器，以方向 PrimaryToRecovery 啟動容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="b4a59-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="b4a59-119">參數</span><span class="sxs-lookup"><span data-stu-id="b4a59-119">PARAMETERS</span></span>

### <span data-ttu-id="b4a59-120">方向</span><span class="sxs-lookup"><span data-stu-id="b4a59-120">-Direction</span></span>
<span data-ttu-id="b4a59-121">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="b4a59-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="b4a59-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b4a59-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4a59-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="b4a59-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="b4a59-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="b4a59-124">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="b4a59-125">-優化</span><span class="sxs-lookup"><span data-stu-id="b4a59-125">-Optimize</span></span>
<span data-ttu-id="b4a59-126">指定要優化的專案。</span><span class="sxs-lookup"><span data-stu-id="b4a59-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="b4a59-127">此參數適用于從 Azure 網站到內部部署網站的容錯移轉，這需要大量的資料同步處理。</span><span class="sxs-lookup"><span data-stu-id="b4a59-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="b4a59-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b4a59-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4a59-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="b4a59-129">ForDowntime</span></span>
- <span data-ttu-id="b4a59-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="b4a59-130">ForSynchronization</span></span>

<span data-ttu-id="b4a59-131">指定 **ForDowntime** 時，這表示資料在進行容錯移轉前已同步處理，以將停機時間降至最低。</span><span class="sxs-lookup"><span data-stu-id="b4a59-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="b4a59-132">不需關閉虛擬機器，就能執行同步處理。</span><span class="sxs-lookup"><span data-stu-id="b4a59-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="b4a59-133">同步處理完成後，作業就會暫停。</span><span class="sxs-lookup"><span data-stu-id="b4a59-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="b4a59-134">繼續工作以執行額外的同步處理操作，以關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b4a59-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="b4a59-135">指定 **ForSynchronization** 時，這表示資料只會在容錯移轉期間進行同步處理，因此資料同步處理會最小化。</span><span class="sxs-lookup"><span data-stu-id="b4a59-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="b4a59-136">因為已啟用此設定，所以會立即關閉虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b4a59-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="b4a59-137">[關閉] 後開始進行同步處理，以完成容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="b4a59-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="b4a59-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b4a59-138">-Profile</span></span>
<span data-ttu-id="b4a59-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b4a59-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4a59-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b4a59-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4a59-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="b4a59-141">-ProtectionContainerId</span></span>
<span data-ttu-id="b4a59-142">指定要啟動作業之受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4a59-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a59-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b4a59-143">-ProtectionEntity</span></span>
<span data-ttu-id="b4a59-144">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="b4a59-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a59-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="b4a59-145">-ProtectionEntityId</span></span>
<span data-ttu-id="b4a59-146">指定要開始作業的 **ASRProtectionEntity** 物件。</span><span class="sxs-lookup"><span data-stu-id="b4a59-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="b4a59-147">若要取得 **ASRProtectionEntity** 物件，請使用 **AzureSiteRecoveryProtectionEntity** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4a59-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a59-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b4a59-148">-RecoveryPlan</span></span>
<span data-ttu-id="b4a59-149">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="b4a59-149">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a59-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="b4a59-150">-RPId</span></span>
<span data-ttu-id="b4a59-151">指定要開始作業的復原方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4a59-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a59-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b4a59-152">-WaitForCompletion</span></span>
<span data-ttu-id="b4a59-153">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="b4a59-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="b4a59-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a59-154">CommonParameters</span></span>
<span data-ttu-id="b4a59-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4a59-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a59-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4a59-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a59-157">輸入</span><span class="sxs-lookup"><span data-stu-id="b4a59-157">INPUTS</span></span>

## <span data-ttu-id="b4a59-158">輸出</span><span class="sxs-lookup"><span data-stu-id="b4a59-158">OUTPUTS</span></span>

## <span data-ttu-id="b4a59-159">筆記</span><span class="sxs-lookup"><span data-stu-id="b4a59-159">NOTES</span></span>

## <span data-ttu-id="b4a59-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4a59-160">RELATED LINKS</span></span>

[<span data-ttu-id="b4a59-161">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b4a59-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="b4a59-162">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b4a59-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


