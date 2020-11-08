---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969129"
---
# <span data-ttu-id="478d9-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="478d9-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="478d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="478d9-102">SYNOPSIS</span></span>
<span data-ttu-id="478d9-103">繼續已暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="478d9-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="478d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="478d9-104">SYNTAX</span></span>

### <span data-ttu-id="478d9-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="478d9-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478d9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="478d9-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478d9-107">說明</span><span class="sxs-lookup"><span data-stu-id="478d9-107">DESCRIPTION</span></span>
<span data-ttu-id="478d9-108">**Resume AzRecoveryServicesAsrJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="478d9-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="478d9-109">示例</span><span class="sxs-lookup"><span data-stu-id="478d9-109">EXAMPLES</span></span>

### <span data-ttu-id="478d9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="478d9-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="478d9-111">如果指定的工作處於 [等待] 或 [暫停] 狀態，並傳回對應至 ASR 作業的更新 ASR 工作物件，請繼續執行該作業。</span><span class="sxs-lookup"><span data-stu-id="478d9-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="478d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="478d9-112">PARAMETERS</span></span>

### <span data-ttu-id="478d9-113">-批註</span><span class="sxs-lookup"><span data-stu-id="478d9-113">-Comment</span></span>
<span data-ttu-id="478d9-114">作業記錄的批註。</span><span class="sxs-lookup"><span data-stu-id="478d9-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="478d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478d9-115">-DefaultProfile</span></span>
<span data-ttu-id="478d9-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="478d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="478d9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="478d9-117">-InputObject</span></span>
<span data-ttu-id="478d9-118">Cmdlet 的輸入物件：對應至要繼續作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="478d9-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="478d9-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="478d9-119">-Name</span></span>
<span data-ttu-id="478d9-120">依名稱指定 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="478d9-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="478d9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="478d9-121">-Confirm</span></span>
<span data-ttu-id="478d9-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="478d9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478d9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478d9-123">-WhatIf</span></span>
<span data-ttu-id="478d9-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="478d9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="478d9-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="478d9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478d9-126">CommonParameters</span></span>
<span data-ttu-id="478d9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="478d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478d9-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="478d9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478d9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="478d9-129">INPUTS</span></span>

### <span data-ttu-id="478d9-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="478d9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="478d9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="478d9-131">OUTPUTS</span></span>

### <span data-ttu-id="478d9-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="478d9-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="478d9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="478d9-133">NOTES</span></span>

## <span data-ttu-id="478d9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="478d9-134">RELATED LINKS</span></span>

[<span data-ttu-id="478d9-135">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="478d9-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="478d9-136">重新開機-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="478d9-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="478d9-137">停止 AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="478d9-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)