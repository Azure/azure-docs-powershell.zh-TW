---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: b71c9a5da3c89916b18bdb5446f311e3d71615bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796858"
---
# <span data-ttu-id="f86cc-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f86cc-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f86cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f86cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f86cc-103">取得所指定 ASR 作業的詳細資料，或 [復原服務] 保存庫中最近的 ASR 作業清單。</span><span class="sxs-lookup"><span data-stu-id="f86cc-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="f86cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f86cc-104">SYNTAX</span></span>

### <span data-ttu-id="f86cc-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="f86cc-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f86cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f86cc-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f86cc-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="f86cc-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f86cc-108">說明</span><span class="sxs-lookup"><span data-stu-id="f86cc-108">DESCRIPTION</span></span>
<span data-ttu-id="f86cc-109">**AzRecoveryServicesAsrJob** Cmdlet 會取得 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="f86cc-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="f86cc-110">您可以使用此 Cmdlet 來查看 [復原服務] 保存庫中的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f86cc-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="f86cc-111">示例</span><span class="sxs-lookup"><span data-stu-id="f86cc-111">EXAMPLES</span></span>

### <span data-ttu-id="f86cc-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f86cc-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="f86cc-113">傳回特定 ASR 物件上的所有工作 (參照 ASR 物件（例如複製的專案或復原方案的識別碼）。 ) </span><span class="sxs-lookup"><span data-stu-id="f86cc-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="f86cc-114">參數</span><span class="sxs-lookup"><span data-stu-id="f86cc-114">PARAMETERS</span></span>

### <span data-ttu-id="f86cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86cc-115">-DefaultProfile</span></span>
<span data-ttu-id="f86cc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f86cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f86cc-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f86cc-117">-EndTime</span></span>
<span data-ttu-id="f86cc-118">指定作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="f86cc-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="f86cc-119">這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="f86cc-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="f86cc-120">若要取得此參數的 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f86cc-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f86cc-121">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="f86cc-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86cc-122">-工作</span><span class="sxs-lookup"><span data-stu-id="f86cc-122">-Job</span></span>
<span data-ttu-id="f86cc-123">指定要取得更新詳細資料的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="f86cc-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f86cc-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f86cc-124">-Name</span></span>
<span data-ttu-id="f86cc-125">依名稱指定 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f86cc-125">Specify the ASR job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86cc-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f86cc-126">-StartTime</span></span>
<span data-ttu-id="f86cc-127">指定作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="f86cc-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="f86cc-128">這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="f86cc-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86cc-129">-State</span><span class="sxs-lookup"><span data-stu-id="f86cc-129">-State</span></span>
<span data-ttu-id="f86cc-130">指定 ASR 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f86cc-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="f86cc-131">這個 Cmdlet 會取得符合指定狀態的所有作業。</span><span class="sxs-lookup"><span data-stu-id="f86cc-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="f86cc-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f86cc-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f86cc-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="f86cc-133">NotStarted</span></span>
- <span data-ttu-id="f86cc-134">正在</span><span class="sxs-lookup"><span data-stu-id="f86cc-134">InProgress</span></span>
- <span data-ttu-id="f86cc-135">成功</span><span class="sxs-lookup"><span data-stu-id="f86cc-135">Succeeded</span></span>
- <span data-ttu-id="f86cc-136">換句話說</span><span class="sxs-lookup"><span data-stu-id="f86cc-136">Other</span></span>
- <span data-ttu-id="f86cc-137">成功</span><span class="sxs-lookup"><span data-stu-id="f86cc-137">Failed</span></span>
- <span data-ttu-id="f86cc-138">取消</span><span class="sxs-lookup"><span data-stu-id="f86cc-138">Cancelled</span></span>
- <span data-ttu-id="f86cc-139">封存</span><span class="sxs-lookup"><span data-stu-id="f86cc-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86cc-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="f86cc-140">-TargetObjectId</span></span>
<span data-ttu-id="f86cc-141">指定物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f86cc-141">Specifies the ID of the object.</span></span> <span data-ttu-id="f86cc-142">用來搜尋指定物件上的工作。</span><span class="sxs-lookup"><span data-stu-id="f86cc-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f86cc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86cc-143">CommonParameters</span></span>
<span data-ttu-id="f86cc-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f86cc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86cc-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f86cc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86cc-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f86cc-146">INPUTS</span></span>

### <span data-ttu-id="f86cc-147">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f86cc-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f86cc-148">輸出</span><span class="sxs-lookup"><span data-stu-id="f86cc-148">OUTPUTS</span></span>

### <span data-ttu-id="f86cc-149">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f86cc-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f86cc-150">筆記</span><span class="sxs-lookup"><span data-stu-id="f86cc-150">NOTES</span></span>

## <span data-ttu-id="f86cc-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f86cc-151">RELATED LINKS</span></span>

[<span data-ttu-id="f86cc-152">重新開機-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f86cc-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="f86cc-153">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f86cc-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="f86cc-154">停止 AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f86cc-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
