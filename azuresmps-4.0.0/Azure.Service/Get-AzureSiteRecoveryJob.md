---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967041"
---
# <span data-ttu-id="1127d-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1127d-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="1127d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1127d-102">SYNOPSIS</span></span>
<span data-ttu-id="1127d-103">取得網站復原電子倉庫的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="1127d-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="1127d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1127d-104">SYNTAX</span></span>

### <span data-ttu-id="1127d-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="1127d-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1127d-106">ById</span><span class="sxs-lookup"><span data-stu-id="1127d-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1127d-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="1127d-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1127d-108">說明</span><span class="sxs-lookup"><span data-stu-id="1127d-108">DESCRIPTION</span></span>
<span data-ttu-id="1127d-109">**AzureSiteRecoveryJob** Cmdlet 會取得 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="1127d-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="1127d-110">您可以使用這個 Cmdlet 來查看目前網站復原電子倉庫的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="1127d-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="1127d-111">示例</span><span class="sxs-lookup"><span data-stu-id="1127d-111">EXAMPLES</span></span>

### <span data-ttu-id="1127d-112">範例1：透過指定識別碼來取得工作</span><span class="sxs-lookup"><span data-stu-id="1127d-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="1127d-113">這個命令會取得具有指定識別碼的 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="1127d-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="1127d-114">範例2：根據時間來取得作業</span><span class="sxs-lookup"><span data-stu-id="1127d-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="1127d-115">這個命令會取得位於指定的開始時間和結束時間之間的網站復原作業。</span><span class="sxs-lookup"><span data-stu-id="1127d-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="1127d-116">參數</span><span class="sxs-lookup"><span data-stu-id="1127d-116">PARAMETERS</span></span>

### <span data-ttu-id="1127d-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1127d-117">-EndTime</span></span>
<span data-ttu-id="1127d-118">指定作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="1127d-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="1127d-119">這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="1127d-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="1127d-120">若要取得 **DateTime** 物件，請使用 [ **取得日期** ] Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1127d-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="1127d-121">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="1127d-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1127d-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="1127d-122">-Id</span></span>
<span data-ttu-id="1127d-123">指定要取得作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1127d-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1127d-124">-工作</span><span class="sxs-lookup"><span data-stu-id="1127d-124">-Job</span></span>
<span data-ttu-id="1127d-125">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="1127d-125">Specifies a job to get.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1127d-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1127d-126">-Profile</span></span>
<span data-ttu-id="1127d-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1127d-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1127d-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1127d-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1127d-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1127d-129">-StartTime</span></span>
<span data-ttu-id="1127d-130">指定作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="1127d-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="1127d-131">這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="1127d-131">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1127d-132">-State</span><span class="sxs-lookup"><span data-stu-id="1127d-132">-State</span></span>
<span data-ttu-id="1127d-133">指定網站還原作業的輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="1127d-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="1127d-134">這個 Cmdlet 會取得符合指定狀態的所有作業。</span><span class="sxs-lookup"><span data-stu-id="1127d-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="1127d-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1127d-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1127d-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="1127d-136">NotStarted</span></span>
- <span data-ttu-id="1127d-137">正在</span><span class="sxs-lookup"><span data-stu-id="1127d-137">InProgress</span></span>
- <span data-ttu-id="1127d-138">成功</span><span class="sxs-lookup"><span data-stu-id="1127d-138">Succeeded</span></span>
- <span data-ttu-id="1127d-139">換句話說</span><span class="sxs-lookup"><span data-stu-id="1127d-139">Other</span></span>
- <span data-ttu-id="1127d-140">成功</span><span class="sxs-lookup"><span data-stu-id="1127d-140">Failed</span></span>
- <span data-ttu-id="1127d-141">取消</span><span class="sxs-lookup"><span data-stu-id="1127d-141">Cancelled</span></span>
- <span data-ttu-id="1127d-142">封存</span><span class="sxs-lookup"><span data-stu-id="1127d-142">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1127d-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="1127d-143">-TargetObjectId</span></span>
<span data-ttu-id="1127d-144">指定作業目標物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1127d-144">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1127d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1127d-145">CommonParameters</span></span>
<span data-ttu-id="1127d-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1127d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1127d-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1127d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1127d-148">輸入</span><span class="sxs-lookup"><span data-stu-id="1127d-148">INPUTS</span></span>

## <span data-ttu-id="1127d-149">輸出</span><span class="sxs-lookup"><span data-stu-id="1127d-149">OUTPUTS</span></span>

## <span data-ttu-id="1127d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="1127d-150">NOTES</span></span>

## <span data-ttu-id="1127d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="1127d-151">RELATED LINKS</span></span>

[<span data-ttu-id="1127d-152">Azure Site Recovery 服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1127d-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="1127d-153">重新開機-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1127d-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="1127d-154">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1127d-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="1127d-155">停止 AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="1127d-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


