---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: cf8b2617e01e472de32f128d4907d68edaebb2e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278087"
---
# <span data-ttu-id="6fce5-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6fce5-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="6fce5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fce5-102">SYNOPSIS</span></span>
<span data-ttu-id="6fce5-103">重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="6fce5-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="6fce5-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fce5-104">SYNTAX</span></span>

### <span data-ttu-id="6fce5-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="6fce5-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fce5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6fce5-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fce5-107">說明</span><span class="sxs-lookup"><span data-stu-id="6fce5-107">DESCRIPTION</span></span>
<span data-ttu-id="6fce5-108">**Restart AzRecoveryServicesAsrJob** Cmdlet 會重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="6fce5-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="6fce5-109">示例</span><span class="sxs-lookup"><span data-stu-id="6fce5-109">EXAMPLES</span></span>

### <span data-ttu-id="6fce5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6fce5-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="6fce5-111">重新開機指定的 ASR 作業，並傳回 ASR 作業的更新 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="6fce5-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="6fce5-112">參數</span><span class="sxs-lookup"><span data-stu-id="6fce5-112">PARAMETERS</span></span>

### <span data-ttu-id="6fce5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fce5-113">-DefaultProfile</span></span>
<span data-ttu-id="6fce5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6fce5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6fce5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fce5-115">-InputObject</span></span>
<span data-ttu-id="6fce5-116">Cmdlet 的輸入物件：與要重新開機之 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="6fce5-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="6fce5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6fce5-117">-Name</span></span>
<span data-ttu-id="6fce5-118">依名稱指定作業。</span><span class="sxs-lookup"><span data-stu-id="6fce5-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="6fce5-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6fce5-119">-Confirm</span></span>
<span data-ttu-id="6fce5-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fce5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fce5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fce5-121">-WhatIf</span></span>
<span data-ttu-id="6fce5-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fce5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fce5-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fce5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fce5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fce5-124">CommonParameters</span></span>
<span data-ttu-id="6fce5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fce5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fce5-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6fce5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fce5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6fce5-127">INPUTS</span></span>

### <span data-ttu-id="6fce5-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6fce5-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6fce5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6fce5-129">OUTPUTS</span></span>

### <span data-ttu-id="6fce5-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6fce5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6fce5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6fce5-131">NOTES</span></span>

## <span data-ttu-id="6fce5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fce5-132">RELATED LINKS</span></span>

[<span data-ttu-id="6fce5-133">AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6fce5-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="6fce5-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6fce5-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="6fce5-135">停止 AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6fce5-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
