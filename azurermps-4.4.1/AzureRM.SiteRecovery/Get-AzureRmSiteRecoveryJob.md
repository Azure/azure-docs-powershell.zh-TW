---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623847"
---
# <span data-ttu-id="5c335-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c335-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="5c335-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c335-102">SYNOPSIS</span></span>
<span data-ttu-id="5c335-103">取得目前網站復原電子倉庫的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="5c335-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c335-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c335-104">SYNTAX</span></span>

### <span data-ttu-id="5c335-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="5c335-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c335-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5c335-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c335-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="5c335-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c335-108">說明</span><span class="sxs-lookup"><span data-stu-id="5c335-108">DESCRIPTION</span></span>
<span data-ttu-id="5c335-109">**AzureRmSiteRecoveryJob** Cmdlet 會取得 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="5c335-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="5c335-110">您可以使用這個 Cmdlet 來查看目前網站復原電子倉庫的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="5c335-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="5c335-111">示例</span><span class="sxs-lookup"><span data-stu-id="5c335-111">EXAMPLES</span></span>

## <span data-ttu-id="5c335-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c335-112">PARAMETERS</span></span>

### <span data-ttu-id="5c335-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5c335-113">-EndTime</span></span>
<span data-ttu-id="5c335-114">指定作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="5c335-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="5c335-115">這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="5c335-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="5c335-116">若要取得此參數的 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c335-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="5c335-117">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="5c335-117">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5c335-118">-工作</span><span class="sxs-lookup"><span data-stu-id="5c335-118">-Job</span></span>
<span data-ttu-id="5c335-119">指定網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="5c335-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c335-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c335-120">-Name</span></span>
<span data-ttu-id="5c335-121">指定識別作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="5c335-121">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="5c335-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5c335-122">-StartTime</span></span>
<span data-ttu-id="5c335-123">指定作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="5c335-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="5c335-124">這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="5c335-124">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="5c335-125">-State</span><span class="sxs-lookup"><span data-stu-id="5c335-125">-State</span></span>
<span data-ttu-id="5c335-126">指定網站還原作業的輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="5c335-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="5c335-127">這個 Cmdlet 會取得符合指定狀態的所有作業。</span><span class="sxs-lookup"><span data-stu-id="5c335-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="5c335-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5c335-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c335-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="5c335-129">NotStarted</span></span>
- <span data-ttu-id="5c335-130">正在</span><span class="sxs-lookup"><span data-stu-id="5c335-130">InProgress</span></span>
- <span data-ttu-id="5c335-131">成功</span><span class="sxs-lookup"><span data-stu-id="5c335-131">Succeeded</span></span>
- <span data-ttu-id="5c335-132">換句話說</span><span class="sxs-lookup"><span data-stu-id="5c335-132">Other</span></span>
- <span data-ttu-id="5c335-133">成功</span><span class="sxs-lookup"><span data-stu-id="5c335-133">Failed</span></span>
- <span data-ttu-id="5c335-134">取消</span><span class="sxs-lookup"><span data-stu-id="5c335-134">Cancelled</span></span>
- <span data-ttu-id="5c335-135">封存</span><span class="sxs-lookup"><span data-stu-id="5c335-135">Suspended</span></span>

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

### <span data-ttu-id="5c335-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="5c335-136">-TargetObjectId</span></span>
<span data-ttu-id="5c335-137">指定作業目標物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c335-137">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="5c335-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c335-138">-DefaultProfile</span></span>
<span data-ttu-id="5c335-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c335-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c335-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c335-140">CommonParameters</span></span>
<span data-ttu-id="5c335-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c335-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c335-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c335-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c335-143">輸入</span><span class="sxs-lookup"><span data-stu-id="5c335-143">INPUTS</span></span>

### <span data-ttu-id="5c335-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="5c335-144">ASRJob</span></span>
<span data-ttu-id="5c335-145">參數「作業」接受管道中類型 ' ASRJob」的值</span><span class="sxs-lookup"><span data-stu-id="5c335-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="5c335-146">輸出</span><span class="sxs-lookup"><span data-stu-id="5c335-146">OUTPUTS</span></span>

### <span data-ttu-id="5c335-147">System.object. IEnumerable ' 1 [SiteRecovery. ASRJob] （）</span><span class="sxs-lookup"><span data-stu-id="5c335-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="5c335-148">筆記</span><span class="sxs-lookup"><span data-stu-id="5c335-148">NOTES</span></span>

## <span data-ttu-id="5c335-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c335-149">RELATED LINKS</span></span>

[<span data-ttu-id="5c335-150">重新開機-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c335-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5c335-151">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c335-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5c335-152">停止 AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5c335-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
