---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 5f76c9a1adabf69872b4d529df7e3289e4d6745b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913765"
---
# <span data-ttu-id="c6a51-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c6a51-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c6a51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6a51-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a51-103">繼續暫停的 Azure 網站復原工作。</span><span class="sxs-lookup"><span data-stu-id="c6a51-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="c6a51-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6a51-104">SYNTAX</span></span>

### <span data-ttu-id="c6a51-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c6a51-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a51-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c6a51-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6a51-107">描述</span><span class="sxs-lookup"><span data-stu-id="c6a51-107">DESCRIPTION</span></span>
<span data-ttu-id="c6a51-108">**Resume-AzRecoveryServicesAsrJob** Cmdlet 會繼續執行暫停的 Azure 網站復原工作。</span><span class="sxs-lookup"><span data-stu-id="c6a51-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="c6a51-109">例子</span><span class="sxs-lookup"><span data-stu-id="c6a51-109">EXAMPLES</span></span>

### <span data-ttu-id="c6a51-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c6a51-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="c6a51-111">如果指定的工作為等待或暫停狀態，則繼續該工作，並返回對應至 ASR 工作的更新 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="c6a51-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="c6a51-112">參數</span><span class="sxs-lookup"><span data-stu-id="c6a51-112">PARAMETERS</span></span>

### <span data-ttu-id="c6a51-113">-批註</span><span class="sxs-lookup"><span data-stu-id="c6a51-113">-Comment</span></span>
<span data-ttu-id="c6a51-114">工作記錄批註。</span><span class="sxs-lookup"><span data-stu-id="c6a51-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="c6a51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a51-115">-DefaultProfile</span></span>
<span data-ttu-id="c6a51-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6a51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c6a51-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6a51-117">-InputObject</span></span>
<span data-ttu-id="c6a51-118">Cmdlet 的輸入物件：對應到要繼續之工作的 ASR Job 物件。</span><span class="sxs-lookup"><span data-stu-id="c6a51-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="c6a51-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6a51-119">-Name</span></span>
<span data-ttu-id="c6a51-120">根據名稱指定 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="c6a51-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="c6a51-121">-確認</span><span class="sxs-lookup"><span data-stu-id="c6a51-121">-Confirm</span></span>
<span data-ttu-id="c6a51-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6a51-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a51-123">-WhatIf</span></span>
<span data-ttu-id="c6a51-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6a51-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6a51-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6a51-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a51-126">CommonParameters</span></span>
<span data-ttu-id="c6a51-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6a51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a51-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6a51-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a51-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c6a51-129">INPUTS</span></span>

### <span data-ttu-id="c6a51-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c6a51-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c6a51-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c6a51-131">OUTPUTS</span></span>

### <span data-ttu-id="c6a51-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c6a51-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c6a51-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c6a51-133">NOTES</span></span>

## <span data-ttu-id="c6a51-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6a51-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6a51-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c6a51-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c6a51-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c6a51-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="c6a51-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c6a51-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
