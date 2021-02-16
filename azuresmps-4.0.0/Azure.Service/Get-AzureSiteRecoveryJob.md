---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a7c99e2ce307d700e43094ffa9be47e5449acc0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411648"
---
# <span data-ttu-id="43b7c-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="43b7c-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="43b7c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="43b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="43b7c-103">獲得網站復原儲存庫的作業資訊。</span><span class="sxs-lookup"><span data-stu-id="43b7c-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="43b7c-104">語法</span><span class="sxs-lookup"><span data-stu-id="43b7c-104">SYNTAX</span></span>

### <span data-ttu-id="43b7c-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="43b7c-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="43b7c-106">ById</span><span class="sxs-lookup"><span data-stu-id="43b7c-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="43b7c-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="43b7c-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43b7c-108">描述</span><span class="sxs-lookup"><span data-stu-id="43b7c-108">DESCRIPTION</span></span>
<span data-ttu-id="43b7c-109">**Get-AzureSiteRecoveryJob** Cmdlet 會取得 Azure 網站復原工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="43b7c-110">您可以使用此 Cmdlet 來查看目前網站復原庫的作業資訊。</span><span class="sxs-lookup"><span data-stu-id="43b7c-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="43b7c-111">例子</span><span class="sxs-lookup"><span data-stu-id="43b7c-111">EXAMPLES</span></span>

### <span data-ttu-id="43b7c-112">範例 1：指定識別碼以取得工作</span><span class="sxs-lookup"><span data-stu-id="43b7c-112">Example 1: Get a job by specifying an ID</span></span>
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

<span data-ttu-id="43b7c-113">此命令會獲得具有指定識別碼的 Azure 網站修復工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="43b7c-114">範例 2：根據時間獲得工作</span><span class="sxs-lookup"><span data-stu-id="43b7c-114">Example 2: Gets a job based on time</span></span>
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

<span data-ttu-id="43b7c-115">此命令會獲得介於指定開始時間和結束時間之間的網站復原工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="43b7c-116">參數</span><span class="sxs-lookup"><span data-stu-id="43b7c-116">PARAMETERS</span></span>

### <span data-ttu-id="43b7c-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="43b7c-117">-EndTime</span></span>
<span data-ttu-id="43b7c-118">指定工作的結束時間。</span><span class="sxs-lookup"><span data-stu-id="43b7c-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="43b7c-119">此 Cmdlet 會獲得指定時間之前開始的所有工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="43b7c-120">若要取得 **DateTime** 物件，請使用 **Get-Date** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43b7c-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="43b7c-121">如需要詳細資訊，請鍵入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="43b7c-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="43b7c-122">-Id</span><span class="sxs-lookup"><span data-stu-id="43b7c-122">-Id</span></span>
<span data-ttu-id="43b7c-123">指定要取得的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="43b7c-123">Specifies the ID of a job to get.</span></span>

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

### <span data-ttu-id="43b7c-124">-Job</span><span class="sxs-lookup"><span data-stu-id="43b7c-124">-Job</span></span>
<span data-ttu-id="43b7c-125">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="43b7c-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="43b7c-126">-Profile</span></span>
<span data-ttu-id="43b7c-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="43b7c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43b7c-128">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="43b7c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43b7c-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="43b7c-129">-StartTime</span></span>
<span data-ttu-id="43b7c-130">指定工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="43b7c-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="43b7c-131">此 Cmdlet 會獲得指定時間之後開始的所有工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="43b7c-132">-State</span><span class="sxs-lookup"><span data-stu-id="43b7c-132">-State</span></span>
<span data-ttu-id="43b7c-133">指定網站復原工作的輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="43b7c-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="43b7c-134">此 Cmdlet 會獲得符合指定狀態的所有工作。</span><span class="sxs-lookup"><span data-stu-id="43b7c-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="43b7c-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="43b7c-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43b7c-136">尚未啟動</span><span class="sxs-lookup"><span data-stu-id="43b7c-136">NotStarted</span></span>
- <span data-ttu-id="43b7c-137">InProgress</span><span class="sxs-lookup"><span data-stu-id="43b7c-137">InProgress</span></span>
- <span data-ttu-id="43b7c-138">成功</span><span class="sxs-lookup"><span data-stu-id="43b7c-138">Succeeded</span></span>
- <span data-ttu-id="43b7c-139">其他</span><span class="sxs-lookup"><span data-stu-id="43b7c-139">Other</span></span>
- <span data-ttu-id="43b7c-140">失敗</span><span class="sxs-lookup"><span data-stu-id="43b7c-140">Failed</span></span>
- <span data-ttu-id="43b7c-141">取消</span><span class="sxs-lookup"><span data-stu-id="43b7c-141">Cancelled</span></span>
- <span data-ttu-id="43b7c-142">暫停</span><span class="sxs-lookup"><span data-stu-id="43b7c-142">Suspended</span></span>

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

### <span data-ttu-id="43b7c-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="43b7c-143">-TargetObjectId</span></span>
<span data-ttu-id="43b7c-144">指定工作所針對物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="43b7c-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="43b7c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b7c-145">CommonParameters</span></span>
<span data-ttu-id="43b7c-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="43b7c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b7c-147">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="43b7c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b7c-148">輸入</span><span class="sxs-lookup"><span data-stu-id="43b7c-148">INPUTS</span></span>

## <span data-ttu-id="43b7c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="43b7c-149">OUTPUTS</span></span>

## <span data-ttu-id="43b7c-150">筆記</span><span class="sxs-lookup"><span data-stu-id="43b7c-150">NOTES</span></span>

## <span data-ttu-id="43b7c-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="43b7c-151">RELATED LINKS</span></span>



[<span data-ttu-id="43b7c-152">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="43b7c-152">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="43b7c-153">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="43b7c-153">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="43b7c-154">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="43b7c-154">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


