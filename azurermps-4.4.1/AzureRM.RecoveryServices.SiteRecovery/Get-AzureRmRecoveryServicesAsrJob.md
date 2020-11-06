---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455640"
---
# <span data-ttu-id="09abd-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="09abd-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="09abd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09abd-102">SYNOPSIS</span></span>
<span data-ttu-id="09abd-103">取得所指定 ASR 作業的詳細資料，或 [復原服務] 保存庫中最近的 ASR 作業清單。</span><span class="sxs-lookup"><span data-stu-id="09abd-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09abd-104">句法</span><span class="sxs-lookup"><span data-stu-id="09abd-104">SYNTAX</span></span>

### <span data-ttu-id="09abd-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="09abd-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="09abd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="09abd-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="09abd-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="09abd-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="09abd-108">說明</span><span class="sxs-lookup"><span data-stu-id="09abd-108">DESCRIPTION</span></span>
<span data-ttu-id="09abd-109">**AzureRmRecoveryServicesAsrJob** Cmdlet 會取得 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="09abd-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="09abd-110">您可以使用此 Cmdlet 來查看 [復原服務] 保存庫中的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="09abd-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="09abd-111">示例</span><span class="sxs-lookup"><span data-stu-id="09abd-111">EXAMPLES</span></span>

### <span data-ttu-id="09abd-112">範例1</span><span class="sxs-lookup"><span data-stu-id="09abd-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="09abd-113">傳回特定 ASR 物件上的所有工作 (參照 ASR 物件（例如複製的專案或復原方案的識別碼）。 ) </span><span class="sxs-lookup"><span data-stu-id="09abd-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="09abd-114">參數</span><span class="sxs-lookup"><span data-stu-id="09abd-114">PARAMETERS</span></span>

### <span data-ttu-id="09abd-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="09abd-115">-EndTime</span></span>
<span data-ttu-id="09abd-116">指定作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="09abd-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="09abd-117">這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="09abd-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="09abd-118">若要取得此參數的 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09abd-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="09abd-119">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="09abd-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="09abd-120">-工作</span><span class="sxs-lookup"><span data-stu-id="09abd-120">-Job</span></span>
<span data-ttu-id="09abd-121">指定要取得更新詳細資料的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="09abd-121">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="09abd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="09abd-122">-Name</span></span>
<span data-ttu-id="09abd-123">依名稱指定 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="09abd-123">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09abd-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="09abd-124">-StartTime</span></span>
<span data-ttu-id="09abd-125">指定作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="09abd-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="09abd-126">這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="09abd-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="09abd-127">-State</span><span class="sxs-lookup"><span data-stu-id="09abd-127">-State</span></span>
<span data-ttu-id="09abd-128">指定 ASR 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="09abd-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="09abd-129">這個 Cmdlet 會取得符合指定狀態的所有作業。</span><span class="sxs-lookup"><span data-stu-id="09abd-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="09abd-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="09abd-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09abd-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="09abd-131">NotStarted</span></span>
- <span data-ttu-id="09abd-132">正在</span><span class="sxs-lookup"><span data-stu-id="09abd-132">InProgress</span></span>
- <span data-ttu-id="09abd-133">成功</span><span class="sxs-lookup"><span data-stu-id="09abd-133">Succeeded</span></span>
- <span data-ttu-id="09abd-134">換句話說</span><span class="sxs-lookup"><span data-stu-id="09abd-134">Other</span></span>
- <span data-ttu-id="09abd-135">成功</span><span class="sxs-lookup"><span data-stu-id="09abd-135">Failed</span></span>
- <span data-ttu-id="09abd-136">取消</span><span class="sxs-lookup"><span data-stu-id="09abd-136">Cancelled</span></span>
- <span data-ttu-id="09abd-137">封存</span><span class="sxs-lookup"><span data-stu-id="09abd-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09abd-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="09abd-138">-TargetObjectId</span></span>
<span data-ttu-id="09abd-139">指定物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="09abd-139">Specifies the ID of the object.</span></span> <span data-ttu-id="09abd-140">用來搜尋指定物件上的工作。</span><span class="sxs-lookup"><span data-stu-id="09abd-140">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="09abd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09abd-141">CommonParameters</span></span>
<span data-ttu-id="09abd-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09abd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09abd-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09abd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09abd-144">輸入</span><span class="sxs-lookup"><span data-stu-id="09abd-144">INPUTS</span></span>

### <span data-ttu-id="09abd-145">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="09abd-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="09abd-146">輸出</span><span class="sxs-lookup"><span data-stu-id="09abd-146">OUTPUTS</span></span>

### <span data-ttu-id="09abd-147">System.object. IEnumerable "1 [ASRJob，RecoveryServices. SiteRecovery，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="09abd-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="09abd-148">筆記</span><span class="sxs-lookup"><span data-stu-id="09abd-148">NOTES</span></span>

## <span data-ttu-id="09abd-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="09abd-149">RELATED LINKS</span></span>

[<span data-ttu-id="09abd-150">重新開機-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="09abd-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="09abd-151">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="09abd-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="09abd-152">停止 AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="09abd-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
