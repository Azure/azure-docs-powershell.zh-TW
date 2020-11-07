---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 7b1b3af4a311b923880253573019c62ee399571c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798017"
---
# <span data-ttu-id="3b92f-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3b92f-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="3b92f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b92f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b92f-103">停止資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="3b92f-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="3b92f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b92f-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b92f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b92f-105">DESCRIPTION</span></span>
<span data-ttu-id="3b92f-106">**AzStreamAnalyticsJob** Cmdlet 會以非同步方式停止資料流程分析作業，使其在 Azure 中執行，並解除所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="3b92f-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="3b92f-107">您可以透過 Azure 入口網站和管理 Api，在您的訂閱中保留作業定義與中繼資料，這樣就可以編輯及重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="3b92f-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="3b92f-108">您不會針對處於停止狀態的工作收取費用。</span><span class="sxs-lookup"><span data-stu-id="3b92f-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="3b92f-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b92f-109">EXAMPLES</span></span>

### <span data-ttu-id="3b92f-110">範例1：停止正在執行的工作</span><span class="sxs-lookup"><span data-stu-id="3b92f-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="3b92f-111">這個命令會停止作業 StreamingJob。</span><span class="sxs-lookup"><span data-stu-id="3b92f-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="3b92f-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b92f-112">PARAMETERS</span></span>

### <span data-ttu-id="3b92f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b92f-113">-DefaultProfile</span></span>
<span data-ttu-id="3b92f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b92f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b92f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b92f-115">-Name</span></span>
<span data-ttu-id="3b92f-116">指定要停止的 Azure 串流分析作業名稱。</span><span class="sxs-lookup"><span data-stu-id="3b92f-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="3b92f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b92f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b92f-118">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b92f-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="3b92f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b92f-119">CommonParameters</span></span>
<span data-ttu-id="3b92f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b92f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b92f-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b92f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b92f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3b92f-122">INPUTS</span></span>

### <span data-ttu-id="3b92f-123">System.object</span><span class="sxs-lookup"><span data-stu-id="3b92f-123">System.String</span></span>

## <span data-ttu-id="3b92f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3b92f-124">OUTPUTS</span></span>

### <span data-ttu-id="3b92f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="3b92f-125">System.Boolean</span></span>

## <span data-ttu-id="3b92f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3b92f-126">NOTES</span></span>

## <span data-ttu-id="3b92f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b92f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3b92f-128">AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3b92f-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3b92f-129">AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3b92f-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3b92f-130">新-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3b92f-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3b92f-131">移除-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3b92f-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="3b92f-132">開始-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3b92f-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


