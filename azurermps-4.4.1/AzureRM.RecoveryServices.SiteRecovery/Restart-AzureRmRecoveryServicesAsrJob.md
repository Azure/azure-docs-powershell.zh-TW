---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625100"
---
# <span data-ttu-id="56836-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="56836-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="56836-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56836-102">SYNOPSIS</span></span>
<span data-ttu-id="56836-103">重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="56836-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56836-104">句法</span><span class="sxs-lookup"><span data-stu-id="56836-104">SYNTAX</span></span>

### <span data-ttu-id="56836-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="56836-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56836-106">ByName</span><span class="sxs-lookup"><span data-stu-id="56836-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56836-107">說明</span><span class="sxs-lookup"><span data-stu-id="56836-107">DESCRIPTION</span></span>
<span data-ttu-id="56836-108">**Restart AzureRmRecoveryServicesAsrJob** Cmdlet 會重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="56836-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="56836-109">示例</span><span class="sxs-lookup"><span data-stu-id="56836-109">EXAMPLES</span></span>

### <span data-ttu-id="56836-110">範例1</span><span class="sxs-lookup"><span data-stu-id="56836-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="56836-111">重新開機指定的 ASR 作業，並傳回 ASR 作業的更新 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="56836-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="56836-112">參數</span><span class="sxs-lookup"><span data-stu-id="56836-112">PARAMETERS</span></span>

### <span data-ttu-id="56836-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56836-113">-InputObject</span></span>
<span data-ttu-id="56836-114">Cmdlet 的輸入物件：與要重新開機之 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="56836-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="56836-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="56836-115">-Name</span></span>
<span data-ttu-id="56836-116">依名稱指定作業。</span><span class="sxs-lookup"><span data-stu-id="56836-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="56836-117">-確認</span><span class="sxs-lookup"><span data-stu-id="56836-117">-Confirm</span></span>
<span data-ttu-id="56836-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56836-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56836-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56836-119">-WhatIf</span></span>
<span data-ttu-id="56836-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56836-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56836-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56836-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56836-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56836-122">CommonParameters</span></span>
<span data-ttu-id="56836-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56836-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56836-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56836-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56836-125">輸入</span><span class="sxs-lookup"><span data-stu-id="56836-125">INPUTS</span></span>

### <span data-ttu-id="56836-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="56836-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56836-127">輸出</span><span class="sxs-lookup"><span data-stu-id="56836-127">OUTPUTS</span></span>

### <span data-ttu-id="56836-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="56836-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56836-129">筆記</span><span class="sxs-lookup"><span data-stu-id="56836-129">NOTES</span></span>

## <span data-ttu-id="56836-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="56836-130">RELATED LINKS</span></span>

[<span data-ttu-id="56836-131">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="56836-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="56836-132">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="56836-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="56836-133">停止 AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="56836-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
