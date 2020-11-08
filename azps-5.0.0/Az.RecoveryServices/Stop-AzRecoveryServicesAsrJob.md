---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: a86e58fe3c933ffaa9a382dc1e5140d3b42a34cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138295"
---
# <span data-ttu-id="d28fd-101">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d28fd-101">Stop-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="d28fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d28fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d28fd-103">停止 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="d28fd-103">Stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d28fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="d28fd-104">SYNTAX</span></span>

### <span data-ttu-id="d28fd-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d28fd-105">ByObject (Default)</span></span>
```
Stop-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d28fd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d28fd-106">ByName</span></span>
```
Stop-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d28fd-107">說明</span><span class="sxs-lookup"><span data-stu-id="d28fd-107">DESCRIPTION</span></span>
<span data-ttu-id="d28fd-108">**AzRecoveryServicesAsrJob** Cmdlet 會停止指定的 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="d28fd-108">The **Stop-AzRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="d28fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="d28fd-109">EXAMPLES</span></span>

### <span data-ttu-id="d28fd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d28fd-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="d28fd-111">嘗試停止指定的工作，並傳回更新的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="d28fd-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="d28fd-112">參數</span><span class="sxs-lookup"><span data-stu-id="d28fd-112">PARAMETERS</span></span>

### <span data-ttu-id="d28fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28fd-113">-DefaultProfile</span></span>
<span data-ttu-id="d28fd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d28fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d28fd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d28fd-115">-InputObject</span></span>
<span data-ttu-id="d28fd-116">輸入物件：指定要停止的 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="d28fd-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="d28fd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d28fd-117">-Name</span></span>
<span data-ttu-id="d28fd-118">指定 asr 作業名稱要停止的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="d28fd-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="d28fd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d28fd-119">-Confirm</span></span>
<span data-ttu-id="d28fd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d28fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d28fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d28fd-121">-WhatIf</span></span>
<span data-ttu-id="d28fd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d28fd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d28fd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d28fd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d28fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28fd-124">CommonParameters</span></span>
<span data-ttu-id="d28fd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d28fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28fd-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d28fd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28fd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d28fd-127">INPUTS</span></span>

### <span data-ttu-id="d28fd-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d28fd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d28fd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d28fd-129">OUTPUTS</span></span>

### <span data-ttu-id="d28fd-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d28fd-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d28fd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d28fd-131">NOTES</span></span>

## <span data-ttu-id="d28fd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d28fd-132">RELATED LINKS</span></span>

[<span data-ttu-id="d28fd-133">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d28fd-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="d28fd-134">重新開機-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d28fd-134">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="d28fd-135">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d28fd-135">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)
