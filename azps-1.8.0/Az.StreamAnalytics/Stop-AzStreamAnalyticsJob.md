---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 050bfccef2b6286ef45a96a9feedc99ef4745115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614373"
---
# <span data-ttu-id="097fd-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="097fd-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="097fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="097fd-102">SYNOPSIS</span></span>
<span data-ttu-id="097fd-103">停止資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="097fd-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="097fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="097fd-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="097fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="097fd-105">DESCRIPTION</span></span>
<span data-ttu-id="097fd-106">**AzStreamAnalyticsJob** Cmdlet 會以非同步方式停止資料流程分析作業，使其在 Azure 中執行，並解除所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="097fd-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="097fd-107">您可以透過 Azure 入口網站和管理 Api，在您的訂閱中保留作業定義與中繼資料，這樣就可以編輯及重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="097fd-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="097fd-108">您不會針對處於停止狀態的工作收取費用。</span><span class="sxs-lookup"><span data-stu-id="097fd-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="097fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="097fd-109">EXAMPLES</span></span>

### <span data-ttu-id="097fd-110">範例1：停止正在執行的工作</span><span class="sxs-lookup"><span data-stu-id="097fd-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="097fd-111">這個命令會停止作業 StreamingJob。</span><span class="sxs-lookup"><span data-stu-id="097fd-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="097fd-112">參數</span><span class="sxs-lookup"><span data-stu-id="097fd-112">PARAMETERS</span></span>

### <span data-ttu-id="097fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097fd-113">-DefaultProfile</span></span>
<span data-ttu-id="097fd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="097fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="097fd-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="097fd-115">-Name</span></span>
<span data-ttu-id="097fd-116">指定要停止的 Azure 串流分析作業名稱。</span><span class="sxs-lookup"><span data-stu-id="097fd-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="097fd-118">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="097fd-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="097fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097fd-119">CommonParameters</span></span>
<span data-ttu-id="097fd-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="097fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097fd-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="097fd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097fd-122">輸入</span><span class="sxs-lookup"><span data-stu-id="097fd-122">INPUTS</span></span>

### <span data-ttu-id="097fd-123">System.object</span><span class="sxs-lookup"><span data-stu-id="097fd-123">System.String</span></span>

## <span data-ttu-id="097fd-124">輸出</span><span class="sxs-lookup"><span data-stu-id="097fd-124">OUTPUTS</span></span>

### <span data-ttu-id="097fd-125">System.object</span><span class="sxs-lookup"><span data-stu-id="097fd-125">System.Boolean</span></span>

## <span data-ttu-id="097fd-126">筆記</span><span class="sxs-lookup"><span data-stu-id="097fd-126">NOTES</span></span>

## <span data-ttu-id="097fd-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="097fd-127">RELATED LINKS</span></span>

[<span data-ttu-id="097fd-128">AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="097fd-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="097fd-129">AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="097fd-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="097fd-130">新-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="097fd-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="097fd-131">移除-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="097fd-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="097fd-132">開始-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="097fd-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


