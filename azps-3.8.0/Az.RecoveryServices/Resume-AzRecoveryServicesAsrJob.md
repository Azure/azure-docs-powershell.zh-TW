---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959476"
---
# <span data-ttu-id="41b4c-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41b4c-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="41b4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="41b4c-103">繼續已暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="41b4c-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="41b4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="41b4c-104">SYNTAX</span></span>

### <span data-ttu-id="41b4c-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="41b4c-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41b4c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="41b4c-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b4c-107">說明</span><span class="sxs-lookup"><span data-stu-id="41b4c-107">DESCRIPTION</span></span>
<span data-ttu-id="41b4c-108">**Resume AzRecoveryServicesAsrJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="41b4c-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="41b4c-109">示例</span><span class="sxs-lookup"><span data-stu-id="41b4c-109">EXAMPLES</span></span>

### <span data-ttu-id="41b4c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="41b4c-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="41b4c-111">如果指定的工作處於 [等待] 或 [暫停] 狀態，並傳回對應至 ASR 作業的更新 ASR 工作物件，請繼續執行該作業。</span><span class="sxs-lookup"><span data-stu-id="41b4c-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="41b4c-112">參數</span><span class="sxs-lookup"><span data-stu-id="41b4c-112">PARAMETERS</span></span>

### <span data-ttu-id="41b4c-113">-批註</span><span class="sxs-lookup"><span data-stu-id="41b4c-113">-Comment</span></span>
<span data-ttu-id="41b4c-114">作業記錄的批註。</span><span class="sxs-lookup"><span data-stu-id="41b4c-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b4c-115">-DefaultProfile</span></span>
<span data-ttu-id="41b4c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41b4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="41b4c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41b4c-117">-InputObject</span></span>
<span data-ttu-id="41b4c-118">Cmdlet 的輸入物件：對應至要繼續作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="41b4c-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41b4c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="41b4c-119">-Name</span></span>
<span data-ttu-id="41b4c-120">依名稱指定 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="41b4c-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="41b4c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="41b4c-121">-Confirm</span></span>
<span data-ttu-id="41b4c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41b4c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b4c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b4c-123">-WhatIf</span></span>
<span data-ttu-id="41b4c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41b4c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41b4c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41b4c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41b4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b4c-126">CommonParameters</span></span>
<span data-ttu-id="41b4c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41b4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b4c-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41b4c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b4c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="41b4c-129">INPUTS</span></span>

### <span data-ttu-id="41b4c-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="41b4c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="41b4c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="41b4c-131">OUTPUTS</span></span>

### <span data-ttu-id="41b4c-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="41b4c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="41b4c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="41b4c-133">NOTES</span></span>

## <span data-ttu-id="41b4c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="41b4c-134">RELATED LINKS</span></span>

[<span data-ttu-id="41b4c-135">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41b4c-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="41b4c-136">重新開機-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41b4c-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="41b4c-137">停止 AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="41b4c-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)