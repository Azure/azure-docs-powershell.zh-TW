---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: DC151161-72C0-40F7-B2F0-45FA01142AE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJob.md
ms.openlocfilehash: 89c4a6bd9d009456c97aa246f608c1920c27c823
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455028"
---
# <span data-ttu-id="4c01d-101">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-101">Get-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="4c01d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c01d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c01d-103">取得排程作業。</span><span class="sxs-lookup"><span data-stu-id="4c01d-103">Gets Scheduler jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c01d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c01d-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> [-JobName <String>]
 [-JobState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c01d-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c01d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c01d-106">**AzureRmSchedulerJob** Cmdlet 會取得 Azure 排程作業。</span><span class="sxs-lookup"><span data-stu-id="4c01d-106">The **Get-AzureRmSchedulerJob** cmdlet gets Azure Scheduler jobs.</span></span>

## <span data-ttu-id="4c01d-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c01d-107">EXAMPLES</span></span>

## <span data-ttu-id="4c01d-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c01d-108">PARAMETERS</span></span>

### <span data-ttu-id="4c01d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c01d-109">-DefaultProfile</span></span>
<span data-ttu-id="4c01d-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c01d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c01d-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="4c01d-111">-JobCollectionName</span></span>
<span data-ttu-id="4c01d-112">指定包含要取得之工作的作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c01d-112">Specifies the name of a job collection that contains jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c01d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="4c01d-113">-JobName</span></span>
<span data-ttu-id="4c01d-114">指定要取得的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="4c01d-114">Specifies the name of a job to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c01d-115">-JobState</span><span class="sxs-lookup"><span data-stu-id="4c01d-115">-JobState</span></span>
<span data-ttu-id="4c01d-116">指定要取得作業的作業狀態。</span><span class="sxs-lookup"><span data-stu-id="4c01d-116">Specifies a job state of jobs to get.</span></span>
<span data-ttu-id="4c01d-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4c01d-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c01d-118">後</span><span class="sxs-lookup"><span data-stu-id="4c01d-118">Enabled</span></span> 
- <span data-ttu-id="4c01d-119">禁止</span><span class="sxs-lookup"><span data-stu-id="4c01d-119">Disabled</span></span> 
- <span data-ttu-id="4c01d-120">錯誤</span><span class="sxs-lookup"><span data-stu-id="4c01d-120">Faulted</span></span> 
- <span data-ttu-id="4c01d-121">完畢</span><span class="sxs-lookup"><span data-stu-id="4c01d-121">Completed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Faulted, Completed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c01d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c01d-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c01d-123">指定要取得作業的資源群組。</span><span class="sxs-lookup"><span data-stu-id="4c01d-123">Specifies the resource group of the jobs to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c01d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c01d-124">CommonParameters</span></span>
<span data-ttu-id="4c01d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c01d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c01d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c01d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c01d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4c01d-127">INPUTS</span></span>

### <span data-ttu-id="4c01d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="4c01d-128">System.String</span></span>

## <span data-ttu-id="4c01d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4c01d-129">OUTPUTS</span></span>

### <span data-ttu-id="4c01d-130">PSSchedulerJobDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c01d-130">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="4c01d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4c01d-131">NOTES</span></span>

## <span data-ttu-id="4c01d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c01d-132">RELATED LINKS</span></span>

[<span data-ttu-id="4c01d-133">新-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-133">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4c01d-134">新-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="4c01d-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="4c01d-135">新-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-135">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4c01d-136">新-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-136">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4c01d-137">新-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-137">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="4c01d-138">移除-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-138">Remove-AzureRmSchedulerJob</span></span>](./Remove-AzureRmSchedulerJob.md)

[<span data-ttu-id="4c01d-139">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-139">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="4c01d-140">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-140">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="4c01d-141">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-141">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="4c01d-142">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="4c01d-142">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)

