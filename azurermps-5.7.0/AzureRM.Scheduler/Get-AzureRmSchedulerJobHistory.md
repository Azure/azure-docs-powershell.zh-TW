---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 6c1582c8e82bf344685f9e1feb002625bddd6748
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623959"
---
# <span data-ttu-id="e76b3-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="e76b3-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="e76b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e76b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e76b3-103">取得作業歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="e76b3-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e76b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="e76b3-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e76b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="e76b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e76b3-106">**AzureRmSchedulerJobHistory** Cmdlet 會取得 Azure 排程作業的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="e76b3-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="e76b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="e76b3-107">EXAMPLES</span></span>

## <span data-ttu-id="e76b3-108">參數</span><span class="sxs-lookup"><span data-stu-id="e76b3-108">PARAMETERS</span></span>

### <span data-ttu-id="e76b3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e76b3-109">-DefaultProfile</span></span>
<span data-ttu-id="e76b3-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e76b3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e76b3-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="e76b3-111">-JobCollectionName</span></span>
<span data-ttu-id="e76b3-112">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="e76b3-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76b3-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="e76b3-113">-JobExecutionStatus</span></span>
<span data-ttu-id="e76b3-114">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="e76b3-114">Specifies the status of a job.</span></span>
<span data-ttu-id="e76b3-115">這個 Cmdlet 會取得與您指定的狀態相符的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="e76b3-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="e76b3-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e76b3-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e76b3-117">完畢</span><span class="sxs-lookup"><span data-stu-id="e76b3-117">Completed</span></span> 
- <span data-ttu-id="e76b3-118">成功</span><span class="sxs-lookup"><span data-stu-id="e76b3-118">Failed</span></span> 
- <span data-ttu-id="e76b3-119">延</span><span class="sxs-lookup"><span data-stu-id="e76b3-119">Postponed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76b3-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="e76b3-120">-JobName</span></span>
<span data-ttu-id="e76b3-121">指定此 Cmdlet 取得其歷程記錄的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="e76b3-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e76b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e76b3-123">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e76b3-123">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e76b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e76b3-124">CommonParameters</span></span>
<span data-ttu-id="e76b3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e76b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e76b3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e76b3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e76b3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e76b3-127">INPUTS</span></span>

### <span data-ttu-id="e76b3-128">所有</span><span class="sxs-lookup"><span data-stu-id="e76b3-128">None</span></span>
<span data-ttu-id="e76b3-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e76b3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e76b3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e76b3-130">OUTPUTS</span></span>

### <span data-ttu-id="e76b3-131">PSJobHistory 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e76b3-131">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="e76b3-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e76b3-132">NOTES</span></span>

## <span data-ttu-id="e76b3-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e76b3-133">RELATED LINKS</span></span>

[<span data-ttu-id="e76b3-134">AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e76b3-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


