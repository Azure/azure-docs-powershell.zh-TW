---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2a13466b792426cdf06b7c52a8067f3adf5b787d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912522"
---
# <span data-ttu-id="2e951-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e951-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="2e951-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2e951-102">SYNOPSIS</span></span>
<span data-ttu-id="2e951-103">停止 Stream Analytics 工作。</span><span class="sxs-lookup"><span data-stu-id="2e951-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="2e951-104">語法</span><span class="sxs-lookup"><span data-stu-id="2e951-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e951-105">描述</span><span class="sxs-lookup"><span data-stu-id="2e951-105">DESCRIPTION</span></span>
<span data-ttu-id="2e951-106">**Stop-AzStreamAnalyticsJob** Cmdlet 會非同步停止 Stream Analytics 工作在 Azure 中執行，並解除配置之前使用的資源。</span><span class="sxs-lookup"><span data-stu-id="2e951-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="2e951-107">您可以透過 Azure 入口網站和管理 API，在訂閱中持續提供工作定義和中繼資料，如此一來，工作就可以編輯並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="2e951-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="2e951-108">在已停止狀態的工作不會收取任何費用。</span><span class="sxs-lookup"><span data-stu-id="2e951-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="2e951-109">例子</span><span class="sxs-lookup"><span data-stu-id="2e951-109">EXAMPLES</span></span>

### <span data-ttu-id="2e951-110">範例 1：停止進行中的工作</span><span class="sxs-lookup"><span data-stu-id="2e951-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="2e951-111">此命令會停止 StreamingJob 的工作。</span><span class="sxs-lookup"><span data-stu-id="2e951-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="2e951-112">參數</span><span class="sxs-lookup"><span data-stu-id="2e951-112">PARAMETERS</span></span>

### <span data-ttu-id="2e951-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e951-113">-DefaultProfile</span></span>
<span data-ttu-id="2e951-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e951-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e951-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e951-115">-Name</span></span>
<span data-ttu-id="2e951-116">指定要停止的 Azure Stream Analytics 工作名稱。</span><span class="sxs-lookup"><span data-stu-id="2e951-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="2e951-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e951-117">-ResourceGroupName</span></span>
<span data-ttu-id="2e951-118">指定 Azure Stream Analytics 工作所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2e951-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="2e951-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e951-119">CommonParameters</span></span>
<span data-ttu-id="2e951-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2e951-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e951-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2e951-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e951-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2e951-122">INPUTS</span></span>

### <span data-ttu-id="2e951-123">System.String</span><span class="sxs-lookup"><span data-stu-id="2e951-123">System.String</span></span>

## <span data-ttu-id="2e951-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2e951-124">OUTPUTS</span></span>

### <span data-ttu-id="2e951-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2e951-125">System.Boolean</span></span>

## <span data-ttu-id="2e951-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2e951-126">NOTES</span></span>

## <span data-ttu-id="2e951-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e951-127">RELATED LINKS</span></span>

[<span data-ttu-id="2e951-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e951-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e951-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e951-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e951-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e951-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e951-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e951-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="2e951-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2e951-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


