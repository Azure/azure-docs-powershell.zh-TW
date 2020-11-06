---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 7eec69a441efbf1a4d9f73e85a0385c24a012e34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453280"
---
# <span data-ttu-id="3f4c2-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="3f4c2-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="3f4c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4c2-103">取得作業歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f4c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f4c2-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f4c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f4c2-105">DESCRIPTION</span></span>
<span data-ttu-id="3f4c2-106">**AzureRmSchedulerJobHistory** Cmdlet 會取得 Azure 排程作業的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="3f4c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="3f4c2-107">EXAMPLES</span></span>

## <span data-ttu-id="3f4c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="3f4c2-108">PARAMETERS</span></span>

### <span data-ttu-id="3f4c2-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="3f4c2-109">-JobCollectionName</span></span>
<span data-ttu-id="3f4c2-110">指定作業集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-110">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="3f4c2-111">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="3f4c2-111">-JobExecutionStatus</span></span>
<span data-ttu-id="3f4c2-112">指定工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-112">Specifies the status of a job.</span></span>
<span data-ttu-id="3f4c2-113">這個 Cmdlet 會取得與您指定的狀態相符的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-113">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="3f4c2-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3f4c2-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f4c2-115">完畢</span><span class="sxs-lookup"><span data-stu-id="3f4c2-115">Completed</span></span> 
- <span data-ttu-id="3f4c2-116">成功</span><span class="sxs-lookup"><span data-stu-id="3f4c2-116">Failed</span></span> 
- <span data-ttu-id="3f4c2-117">延</span><span class="sxs-lookup"><span data-stu-id="3f4c2-117">Postponed</span></span>

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

### <span data-ttu-id="3f4c2-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="3f4c2-118">-JobName</span></span>
<span data-ttu-id="3f4c2-119">指定此 Cmdlet 取得其歷程記錄的作業名稱。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-119">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="3f4c2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f4c2-120">-ResourceGroupName</span></span>
<span data-ttu-id="3f4c2-121">指定作業所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-121">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="3f4c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4c2-122">-DefaultProfile</span></span>
<span data-ttu-id="3f4c2-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f4c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4c2-124">CommonParameters</span></span>
<span data-ttu-id="3f4c2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4c2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f4c2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4c2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3f4c2-127">INPUTS</span></span>

## <span data-ttu-id="3f4c2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3f4c2-128">OUTPUTS</span></span>

### <span data-ttu-id="3f4c2-129">PSJobHistory 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3f4c2-129">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="3f4c2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3f4c2-130">NOTES</span></span>

## <span data-ttu-id="3f4c2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f4c2-131">RELATED LINKS</span></span>

[<span data-ttu-id="3f4c2-132">AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="3f4c2-132">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


