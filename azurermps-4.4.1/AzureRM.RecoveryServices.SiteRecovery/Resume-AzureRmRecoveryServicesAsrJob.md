---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453327"
---
# <span data-ttu-id="f526b-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f526b-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f526b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f526b-102">SYNOPSIS</span></span>
<span data-ttu-id="f526b-103">繼續已暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="f526b-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f526b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f526b-104">SYNTAX</span></span>

### <span data-ttu-id="f526b-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f526b-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f526b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f526b-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f526b-107">說明</span><span class="sxs-lookup"><span data-stu-id="f526b-107">DESCRIPTION</span></span>
<span data-ttu-id="f526b-108">**Resume AzureRmRecoveryServicesAsrJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="f526b-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="f526b-109">示例</span><span class="sxs-lookup"><span data-stu-id="f526b-109">EXAMPLES</span></span>

### <span data-ttu-id="f526b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f526b-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="f526b-111">如果指定的工作處於 [等待] 或 [暫停] 狀態，並傳回對應至 ASR 作業的更新 ASR 工作物件，請繼續執行該作業。</span><span class="sxs-lookup"><span data-stu-id="f526b-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="f526b-112">參數</span><span class="sxs-lookup"><span data-stu-id="f526b-112">PARAMETERS</span></span>

### <span data-ttu-id="f526b-113">-批註</span><span class="sxs-lookup"><span data-stu-id="f526b-113">-Comment</span></span>
<span data-ttu-id="f526b-114">作業記錄的批註。</span><span class="sxs-lookup"><span data-stu-id="f526b-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f526b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f526b-115">-InputObject</span></span>
<span data-ttu-id="f526b-116">Cmdlet 的輸入物件：對應至要繼續作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="f526b-116">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f526b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f526b-117">-Name</span></span>
<span data-ttu-id="f526b-118">依名稱指定 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="f526b-118">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="f526b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f526b-119">-Confirm</span></span>
<span data-ttu-id="f526b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f526b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f526b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f526b-121">-WhatIf</span></span>
<span data-ttu-id="f526b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f526b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f526b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f526b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f526b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f526b-124">CommonParameters</span></span>
<span data-ttu-id="f526b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f526b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f526b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f526b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f526b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f526b-127">INPUTS</span></span>

### <span data-ttu-id="f526b-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f526b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f526b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f526b-129">OUTPUTS</span></span>

### <span data-ttu-id="f526b-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f526b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f526b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f526b-131">NOTES</span></span>

## <span data-ttu-id="f526b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f526b-132">RELATED LINKS</span></span>

[<span data-ttu-id="f526b-133">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f526b-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f526b-134">重新開機-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f526b-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f526b-135">停止 AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f526b-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
