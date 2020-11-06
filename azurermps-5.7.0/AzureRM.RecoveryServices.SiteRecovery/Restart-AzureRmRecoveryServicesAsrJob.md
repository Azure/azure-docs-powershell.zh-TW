---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/restart-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 0ac09a527aff78648d3af14413baa33da137d59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448609"
---
# <span data-ttu-id="f8d03-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f8d03-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f8d03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8d03-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d03-103">重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="f8d03-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8d03-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8d03-104">SYNTAX</span></span>

### <span data-ttu-id="f8d03-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="f8d03-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d03-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f8d03-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d03-107">說明</span><span class="sxs-lookup"><span data-stu-id="f8d03-107">DESCRIPTION</span></span>
<span data-ttu-id="f8d03-108">**Restart AzureRmRecoveryServicesAsrJob** Cmdlet 會重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="f8d03-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="f8d03-109">示例</span><span class="sxs-lookup"><span data-stu-id="f8d03-109">EXAMPLES</span></span>

### <span data-ttu-id="f8d03-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f8d03-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="f8d03-111">重新開機指定的 ASR 作業，並傳回 ASR 作業的更新 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="f8d03-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="f8d03-112">參數</span><span class="sxs-lookup"><span data-stu-id="f8d03-112">PARAMETERS</span></span>

### <span data-ttu-id="f8d03-113">-確認</span><span class="sxs-lookup"><span data-stu-id="f8d03-113">-Confirm</span></span>
<span data-ttu-id="f8d03-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8d03-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d03-115">-DefaultProfile</span></span>
<span data-ttu-id="f8d03-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8d03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8d03-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8d03-117">-InputObject</span></span>
<span data-ttu-id="f8d03-118">Cmdlet 的輸入物件：與要重新開機之 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="f8d03-118">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="f8d03-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8d03-119">-Name</span></span>
<span data-ttu-id="f8d03-120">依名稱指定作業。</span><span class="sxs-lookup"><span data-stu-id="f8d03-120">Specify the job by name.</span></span>

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

### <span data-ttu-id="f8d03-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d03-121">-WhatIf</span></span>
<span data-ttu-id="f8d03-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8d03-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8d03-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8d03-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d03-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d03-124">CommonParameters</span></span>
<span data-ttu-id="f8d03-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8d03-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d03-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8d03-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d03-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f8d03-127">INPUTS</span></span>

### <span data-ttu-id="f8d03-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8d03-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8d03-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f8d03-129">OUTPUTS</span></span>

### <span data-ttu-id="f8d03-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8d03-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8d03-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f8d03-131">NOTES</span></span>

## <span data-ttu-id="f8d03-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8d03-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8d03-133">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f8d03-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f8d03-134">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f8d03-134">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f8d03-135">停止 AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f8d03-135">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
