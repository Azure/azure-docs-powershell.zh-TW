---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 2609ed7483499445dbdd093d0059b76b7e781ef8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902198"
---
# <span data-ttu-id="bdf38-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdf38-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="bdf38-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bdf38-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf38-103">重新開機 Azure 網站復原工作。</span><span class="sxs-lookup"><span data-stu-id="bdf38-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="bdf38-104">語法</span><span class="sxs-lookup"><span data-stu-id="bdf38-104">SYNTAX</span></span>

### <span data-ttu-id="bdf38-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="bdf38-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdf38-106">ByName</span><span class="sxs-lookup"><span data-stu-id="bdf38-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bdf38-107">描述</span><span class="sxs-lookup"><span data-stu-id="bdf38-107">DESCRIPTION</span></span>
<span data-ttu-id="bdf38-108">**Restart-AzRecoveryServicesAsrJob** Cmdlet 會重新開機 Azure 網站復原工作。</span><span class="sxs-lookup"><span data-stu-id="bdf38-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="bdf38-109">例子</span><span class="sxs-lookup"><span data-stu-id="bdf38-109">EXAMPLES</span></span>

### <span data-ttu-id="bdf38-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="bdf38-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="bdf38-111">重新開機指定的 ASR 工作，並返回 ASR 工作已更新的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="bdf38-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="bdf38-112">參數</span><span class="sxs-lookup"><span data-stu-id="bdf38-112">PARAMETERS</span></span>

### <span data-ttu-id="bdf38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf38-113">-DefaultProfile</span></span>
<span data-ttu-id="bdf38-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bdf38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bdf38-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdf38-115">-InputObject</span></span>
<span data-ttu-id="bdf38-116">Cmdlet 的輸入物件：對應至要重新開機之 ASR 工作的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="bdf38-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="bdf38-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bdf38-117">-Name</span></span>
<span data-ttu-id="bdf38-118">根據名稱指定工作。</span><span class="sxs-lookup"><span data-stu-id="bdf38-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="bdf38-119">-確認</span><span class="sxs-lookup"><span data-stu-id="bdf38-119">-Confirm</span></span>
<span data-ttu-id="bdf38-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bdf38-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdf38-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdf38-121">-WhatIf</span></span>
<span data-ttu-id="bdf38-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bdf38-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdf38-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bdf38-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdf38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf38-124">CommonParameters</span></span>
<span data-ttu-id="bdf38-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bdf38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf38-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdf38-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf38-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bdf38-127">INPUTS</span></span>

### <span data-ttu-id="bdf38-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bdf38-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bdf38-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bdf38-129">OUTPUTS</span></span>

### <span data-ttu-id="bdf38-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bdf38-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bdf38-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bdf38-131">NOTES</span></span>

## <span data-ttu-id="bdf38-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bdf38-132">RELATED LINKS</span></span>

[<span data-ttu-id="bdf38-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdf38-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="bdf38-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdf38-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="bdf38-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="bdf38-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
