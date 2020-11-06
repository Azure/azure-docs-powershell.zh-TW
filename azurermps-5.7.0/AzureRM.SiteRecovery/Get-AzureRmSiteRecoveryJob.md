---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450470"
---
# <span data-ttu-id="87b52-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="87b52-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="87b52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87b52-102">SYNOPSIS</span></span>
<span data-ttu-id="87b52-103">取得目前網站復原電子倉庫的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="87b52-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b52-104">句法</span><span class="sxs-lookup"><span data-stu-id="87b52-104">SYNTAX</span></span>

### <span data-ttu-id="87b52-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="87b52-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b52-106">ByName</span><span class="sxs-lookup"><span data-stu-id="87b52-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87b52-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="87b52-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b52-108">說明</span><span class="sxs-lookup"><span data-stu-id="87b52-108">DESCRIPTION</span></span>
<span data-ttu-id="87b52-109">**AzureRmSiteRecoveryJob** Cmdlet 會取得 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="87b52-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="87b52-110">您可以使用這個 Cmdlet 來查看目前網站復原電子倉庫的操作資訊。</span><span class="sxs-lookup"><span data-stu-id="87b52-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="87b52-111">示例</span><span class="sxs-lookup"><span data-stu-id="87b52-111">EXAMPLES</span></span>

## <span data-ttu-id="87b52-112">參數</span><span class="sxs-lookup"><span data-stu-id="87b52-112">PARAMETERS</span></span>

### <span data-ttu-id="87b52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b52-113">-DefaultProfile</span></span>
<span data-ttu-id="87b52-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87b52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b52-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="87b52-115">-EndTime</span></span>
<span data-ttu-id="87b52-116">指定作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="87b52-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="87b52-117">這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="87b52-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="87b52-118">若要取得此參數的 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87b52-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="87b52-119">如需詳細資訊，請輸入 `Get-Help Get-Date` 。</span><span class="sxs-lookup"><span data-stu-id="87b52-119">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="87b52-120">-工作</span><span class="sxs-lookup"><span data-stu-id="87b52-120">-Job</span></span>
<span data-ttu-id="87b52-121">指定網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="87b52-121">Specifies the Site Recovery job.</span></span>

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

### <span data-ttu-id="87b52-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="87b52-122">-Name</span></span>
<span data-ttu-id="87b52-123">指定識別作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="87b52-123">Specifies a unique name that identifies the job.</span></span>

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

### <span data-ttu-id="87b52-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="87b52-124">-StartTime</span></span>
<span data-ttu-id="87b52-125">指定作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="87b52-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="87b52-126">這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。</span><span class="sxs-lookup"><span data-stu-id="87b52-126">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="87b52-127">-State</span><span class="sxs-lookup"><span data-stu-id="87b52-127">-State</span></span>
<span data-ttu-id="87b52-128">指定網站還原作業的輸入狀態。</span><span class="sxs-lookup"><span data-stu-id="87b52-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="87b52-129">這個 Cmdlet 會取得符合指定狀態的所有作業。</span><span class="sxs-lookup"><span data-stu-id="87b52-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="87b52-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="87b52-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87b52-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="87b52-131">NotStarted</span></span>
- <span data-ttu-id="87b52-132">正在</span><span class="sxs-lookup"><span data-stu-id="87b52-132">InProgress</span></span>
- <span data-ttu-id="87b52-133">成功</span><span class="sxs-lookup"><span data-stu-id="87b52-133">Succeeded</span></span>
- <span data-ttu-id="87b52-134">換句話說</span><span class="sxs-lookup"><span data-stu-id="87b52-134">Other</span></span>
- <span data-ttu-id="87b52-135">成功</span><span class="sxs-lookup"><span data-stu-id="87b52-135">Failed</span></span>
- <span data-ttu-id="87b52-136">取消</span><span class="sxs-lookup"><span data-stu-id="87b52-136">Cancelled</span></span>
- <span data-ttu-id="87b52-137">封存</span><span class="sxs-lookup"><span data-stu-id="87b52-137">Suspended</span></span>

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

### <span data-ttu-id="87b52-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="87b52-138">-TargetObjectId</span></span>
<span data-ttu-id="87b52-139">指定作業目標物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="87b52-139">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="87b52-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b52-140">CommonParameters</span></span>
<span data-ttu-id="87b52-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87b52-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b52-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87b52-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b52-143">輸入</span><span class="sxs-lookup"><span data-stu-id="87b52-143">INPUTS</span></span>

### <span data-ttu-id="87b52-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="87b52-144">ASRJob</span></span>
<span data-ttu-id="87b52-145">參數「作業」接受管道中類型 ' ASRJob」的值</span><span class="sxs-lookup"><span data-stu-id="87b52-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="87b52-146">輸出</span><span class="sxs-lookup"><span data-stu-id="87b52-146">OUTPUTS</span></span>

### <span data-ttu-id="87b52-147">System.object. IEnumerable ' 1 [SiteRecovery. ASRJob] （）</span><span class="sxs-lookup"><span data-stu-id="87b52-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="87b52-148">筆記</span><span class="sxs-lookup"><span data-stu-id="87b52-148">NOTES</span></span>

## <span data-ttu-id="87b52-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="87b52-149">RELATED LINKS</span></span>

[<span data-ttu-id="87b52-150">重新開機-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="87b52-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="87b52-151">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="87b52-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="87b52-152">停止 AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="87b52-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
