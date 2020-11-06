---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 5bf5745270db8cea076ccac9cff2d4e9b7a4bc06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455019"
---
# <span data-ttu-id="41b97-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="41b97-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="41b97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41b97-102">SYNOPSIS</span></span>
<span data-ttu-id="41b97-103">取得作業歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="41b97-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41b97-104">句法</span><span class="sxs-lookup"><span data-stu-id="41b97-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41b97-105">說明</span><span class="sxs-lookup"><span data-stu-id="41b97-105">DESCRIPTION</span></span>
<span data-ttu-id="41b97-106">**AzureRmSchedulerJobHistory** Cmdlet 會取得 Azure 排程作業的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="41b97-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="41b97-107">示例</span><span class="sxs-lookup"><span data-stu-id="41b97-107">EXAMPLES</span></span>

## <span data-ttu-id="41b97-108">參數</span><span class="sxs-lookup"><span data-stu-id="41b97-108">PARAMETERS</span></span>

### <span data-ttu-id="41b97-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b97-109">-DefaultProfile</span></span>
<span data-ttu-id="41b97-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41b97-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b97-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="41b97-111">-JobCollectionName</span></span>
<span data-ttu-id="41b97-112">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="41b97-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="41b97-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="41b97-113">-JobExecutionStatus</span></span>
<span data-ttu-id="41b97-114">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="41b97-114">Specifies the status of a job.</span></span>
<span data-ttu-id="41b97-115">這個 Cmdlet 會取得與您指定的狀態相符的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="41b97-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="41b97-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="41b97-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="41b97-117">完畢</span><span class="sxs-lookup"><span data-stu-id="41b97-117">Completed</span></span> 
- <span data-ttu-id="41b97-118">成功</span><span class="sxs-lookup"><span data-stu-id="41b97-118">Failed</span></span> 
- <span data-ttu-id="41b97-119">延</span><span class="sxs-lookup"><span data-stu-id="41b97-119">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41b97-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="41b97-120">-JobName</span></span>
<span data-ttu-id="41b97-121">指定此 Cmdlet 取得其歷程記錄的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="41b97-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="41b97-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41b97-122">-ResourceGroupName</span></span>
<span data-ttu-id="41b97-123">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="41b97-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="41b97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b97-124">CommonParameters</span></span>
<span data-ttu-id="41b97-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41b97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b97-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="41b97-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b97-127">輸入</span><span class="sxs-lookup"><span data-stu-id="41b97-127">INPUTS</span></span>

### <span data-ttu-id="41b97-128">System.object</span><span class="sxs-lookup"><span data-stu-id="41b97-128">System.String</span></span>

## <span data-ttu-id="41b97-129">輸出</span><span class="sxs-lookup"><span data-stu-id="41b97-129">OUTPUTS</span></span>

### <span data-ttu-id="41b97-130">PSJobHistory 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="41b97-130">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="41b97-131">筆記</span><span class="sxs-lookup"><span data-stu-id="41b97-131">NOTES</span></span>

## <span data-ttu-id="41b97-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="41b97-132">RELATED LINKS</span></span>

[<span data-ttu-id="41b97-133">AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="41b97-133">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


