---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 94f4f44da8da4b2ad16db6dff86ad22908847a62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454564"
---
# <span data-ttu-id="8a055-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8a055-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="8a055-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a055-102">SYNOPSIS</span></span>
<span data-ttu-id="8a055-103">重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="8a055-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a055-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a055-104">SYNTAX</span></span>

### <span data-ttu-id="8a055-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="8a055-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a055-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8a055-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a055-107">說明</span><span class="sxs-lookup"><span data-stu-id="8a055-107">DESCRIPTION</span></span>
<span data-ttu-id="8a055-108">**Restart AzureRmRecoveryServicesAsrJob** Cmdlet 會重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="8a055-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="8a055-109">示例</span><span class="sxs-lookup"><span data-stu-id="8a055-109">EXAMPLES</span></span>

### <span data-ttu-id="8a055-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8a055-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="8a055-111">重新開機指定的 ASR 作業，並傳回 ASR 作業的更新 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="8a055-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="8a055-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a055-112">PARAMETERS</span></span>

### <span data-ttu-id="8a055-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a055-113">-DefaultProfile</span></span>
<span data-ttu-id="8a055-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a055-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a055-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a055-115">-InputObject</span></span>
<span data-ttu-id="8a055-116">Cmdlet 的輸入物件：與要重新開機之 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="8a055-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


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

### <span data-ttu-id="8a055-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a055-117">-Name</span></span>
<span data-ttu-id="8a055-118">依名稱指定作業。</span><span class="sxs-lookup"><span data-stu-id="8a055-118">Specify the job by name.</span></span>

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

### <span data-ttu-id="8a055-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8a055-119">-Confirm</span></span>
<span data-ttu-id="8a055-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a055-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a055-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a055-121">-WhatIf</span></span>
<span data-ttu-id="8a055-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a055-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a055-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a055-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a055-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a055-124">CommonParameters</span></span>
<span data-ttu-id="8a055-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a055-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a055-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a055-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a055-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8a055-127">INPUTS</span></span>

### <span data-ttu-id="8a055-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8a055-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8a055-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8a055-129">OUTPUTS</span></span>

### <span data-ttu-id="8a055-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8a055-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8a055-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8a055-131">NOTES</span></span>

## <span data-ttu-id="8a055-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a055-132">RELATED LINKS</span></span>

[<span data-ttu-id="8a055-133">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8a055-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8a055-134">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8a055-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="8a055-135">停止 AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8a055-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
