---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130954"
---
# <span data-ttu-id="082b0-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="082b0-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="082b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="082b0-102">SYNOPSIS</span></span>
<span data-ttu-id="082b0-103">停止 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="082b0-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="082b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="082b0-104">SYNTAX</span></span>

### <span data-ttu-id="082b0-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="082b0-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="082b0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="082b0-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="082b0-107">說明</span><span class="sxs-lookup"><span data-stu-id="082b0-107">DESCRIPTION</span></span>
<span data-ttu-id="082b0-108">**AzRecoveryServicesAsrJob** Cmdlet 會停止指定的 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="082b0-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="082b0-109">示例</span><span class="sxs-lookup"><span data-stu-id="082b0-109">EXAMPLES</span></span>

### <span data-ttu-id="082b0-110">範例1</span><span class="sxs-lookup"><span data-stu-id="082b0-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="082b0-111">嘗試停止指定的工作，並傳回更新的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="082b0-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="082b0-112">參數</span><span class="sxs-lookup"><span data-stu-id="082b0-112">PARAMETERS</span></span>

### <span data-ttu-id="082b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082b0-113">-DefaultProfile</span></span>
<span data-ttu-id="082b0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="082b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="082b0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="082b0-115">-InputObject</span></span>
<span data-ttu-id="082b0-116">輸入物件：指定要停止的 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="082b0-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="082b0-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="082b0-117">-Name</span></span>
<span data-ttu-id="082b0-118">指定 asr 作業名稱要停止的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="082b0-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="082b0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="082b0-119">-Confirm</span></span>
<span data-ttu-id="082b0-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="082b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082b0-121">-WhatIf</span></span>
<span data-ttu-id="082b0-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="082b0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="082b0-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="082b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082b0-124">CommonParameters</span></span>
<span data-ttu-id="082b0-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="082b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082b0-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="082b0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082b0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="082b0-127">INPUTS</span></span>

### <span data-ttu-id="082b0-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="082b0-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="082b0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="082b0-129">OUTPUTS</span></span>

### <span data-ttu-id="082b0-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="082b0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="082b0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="082b0-131">NOTES</span></span>

## <span data-ttu-id="082b0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="082b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="082b0-133">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="082b0-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="082b0-134">重新開機-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="082b0-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="082b0-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="082b0-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
