---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 14f24f9b9659b6668041b800462eca422fb67c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623544"
---
# <span data-ttu-id="b5548-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b5548-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="b5548-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5548-102">SYNOPSIS</span></span>
<span data-ttu-id="b5548-103">停止 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="b5548-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5548-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5548-104">SYNTAX</span></span>

### <span data-ttu-id="b5548-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="b5548-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5548-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b5548-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5548-107">說明</span><span class="sxs-lookup"><span data-stu-id="b5548-107">DESCRIPTION</span></span>
<span data-ttu-id="b5548-108">**AzureRmRecoveryServicesAsrJob** Cmdlet 會停止指定的 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="b5548-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="b5548-109">示例</span><span class="sxs-lookup"><span data-stu-id="b5548-109">EXAMPLES</span></span>

### <span data-ttu-id="b5548-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b5548-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="b5548-111">嘗試停止指定的工作，並傳回更新的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="b5548-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="b5548-112">參數</span><span class="sxs-lookup"><span data-stu-id="b5548-112">PARAMETERS</span></span>

### <span data-ttu-id="b5548-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5548-113">-DefaultProfile</span></span>
<span data-ttu-id="b5548-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5548-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b5548-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5548-115">-InputObject</span></span>
<span data-ttu-id="b5548-116">輸入物件：指定要停止的 ASR 作業對應的 ASR 工作物件</span><span class="sxs-lookup"><span data-stu-id="b5548-116">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="b5548-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5548-117">-Name</span></span>
<span data-ttu-id="b5548-118">指定 asr 作業名稱要停止的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="b5548-118">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="b5548-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b5548-119">-Confirm</span></span>
<span data-ttu-id="b5548-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b5548-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5548-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5548-121">-WhatIf</span></span>
<span data-ttu-id="b5548-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5548-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5548-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5548-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5548-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5548-124">CommonParameters</span></span>
<span data-ttu-id="b5548-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5548-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5548-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5548-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5548-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b5548-127">INPUTS</span></span>

### <span data-ttu-id="b5548-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b5548-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5548-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b5548-129">OUTPUTS</span></span>

### <span data-ttu-id="b5548-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b5548-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5548-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b5548-131">NOTES</span></span>

## <span data-ttu-id="b5548-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5548-132">RELATED LINKS</span></span>

[<span data-ttu-id="b5548-133">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b5548-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="b5548-134">重新開機-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b5548-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="b5548-135">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b5548-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
