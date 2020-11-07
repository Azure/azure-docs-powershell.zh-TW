---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967252"
---
# <span data-ttu-id="ec024-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ec024-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="ec024-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec024-102">SYNOPSIS</span></span>
<span data-ttu-id="ec024-103">針對網站恢復保護實體或復原方案啟動未計畫的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ec024-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="ec024-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec024-104">SYNTAX</span></span>

### <span data-ttu-id="ec024-105">ByRPId (預設) </span><span class="sxs-lookup"><span data-stu-id="ec024-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec024-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="ec024-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ec024-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="ec024-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec024-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="ec024-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec024-109">說明</span><span class="sxs-lookup"><span data-stu-id="ec024-109">DESCRIPTION</span></span>
<span data-ttu-id="ec024-110">**Start AzureSiteRecoveryUnplannedFailoverJob** Cmdlet 會啟動 Azure Site Recovery 保護實體或復原方案的未計畫式容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ec024-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="ec024-111">您可以使用 **AzureSiteRecoveryJob** Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="ec024-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="ec024-112">示例</span><span class="sxs-lookup"><span data-stu-id="ec024-112">EXAMPLES</span></span>

### <span data-ttu-id="ec024-113">範例1：啟動未計畫的容錯移轉作業</span><span class="sxs-lookup"><span data-stu-id="ec024-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="ec024-114">第一個命令會使用 **AzureSiteRecoveryProtectionContainer** Cmdlet 取得受保護的容器，然後將它儲存在 $ProtectionContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="ec024-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="ec024-115">第二個命令會使用 **AzureSiteRecoveryProtectionEntity** Cmdlet 來取得屬於儲存在 $ProtectionContainer 中之受保護容器的受保護實體。</span><span class="sxs-lookup"><span data-stu-id="ec024-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="ec024-116">該命令會將結果儲存在 $ProtectionEntity 變數中。</span><span class="sxs-lookup"><span data-stu-id="ec024-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="ec024-117">最終命令會針對儲存在 $ProtectionEntity 中的受保護實體啟動容錯移轉，並指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="ec024-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="ec024-118">參數</span><span class="sxs-lookup"><span data-stu-id="ec024-118">PARAMETERS</span></span>

### <span data-ttu-id="ec024-119">方向</span><span class="sxs-lookup"><span data-stu-id="ec024-119">-Direction</span></span>
<span data-ttu-id="ec024-120">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="ec024-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="ec024-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ec024-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec024-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="ec024-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="ec024-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="ec024-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="ec024-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="ec024-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="ec024-125">指示動作可以執行源端動作。</span><span class="sxs-lookup"><span data-stu-id="ec024-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="ec024-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="ec024-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="ec024-127">表示可以執行來源網站作業。</span><span class="sxs-lookup"><span data-stu-id="ec024-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec024-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="ec024-128">-PrimaryAction</span></span>
<span data-ttu-id="ec024-129">表示需要主要網站動作。</span><span class="sxs-lookup"><span data-stu-id="ec024-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec024-130">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ec024-130">-Profile</span></span>
<span data-ttu-id="ec024-131">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ec024-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec024-132">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ec024-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec024-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="ec024-133">-ProtectionContainerId</span></span>
<span data-ttu-id="ec024-134">指定受保護容器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec024-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="ec024-135">這個 Cmdlet 會針對屬於這個 Cmdlet 所指定容器的受保護虛擬機器啟動作業。</span><span class="sxs-lookup"><span data-stu-id="ec024-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="ec024-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ec024-136">-ProtectionEntity</span></span>
<span data-ttu-id="ec024-137">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="ec024-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="ec024-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="ec024-138">-ProtectionEntityId</span></span>
<span data-ttu-id="ec024-139">指定要啟動作業之受保護虛擬機器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec024-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="ec024-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ec024-140">-RecoveryPlan</span></span>
<span data-ttu-id="ec024-141">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="ec024-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="ec024-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="ec024-142">-RPId</span></span>
<span data-ttu-id="ec024-143">指定要開始作業的復原方案識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec024-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="ec024-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ec024-144">-WaitForCompletion</span></span>
<span data-ttu-id="ec024-145">表示 Cmdlet 在將控制權傳回給 Windows PowerShell 主控台之前，先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="ec024-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ec024-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec024-146">CommonParameters</span></span>
<span data-ttu-id="ec024-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec024-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec024-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec024-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec024-149">輸入</span><span class="sxs-lookup"><span data-stu-id="ec024-149">INPUTS</span></span>

## <span data-ttu-id="ec024-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ec024-150">OUTPUTS</span></span>

## <span data-ttu-id="ec024-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ec024-151">NOTES</span></span>

## <span data-ttu-id="ec024-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec024-152">RELATED LINKS</span></span>

[<span data-ttu-id="ec024-153">AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ec024-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="ec024-154">AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ec024-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="ec024-155">AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="ec024-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="ec024-156">開始-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="ec024-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


