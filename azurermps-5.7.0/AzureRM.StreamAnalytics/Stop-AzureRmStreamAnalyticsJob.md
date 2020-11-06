---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444211"
---
# <span data-ttu-id="e43c0-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e43c0-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="e43c0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e43c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e43c0-103">停止資料流程分析作業。</span><span class="sxs-lookup"><span data-stu-id="e43c0-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e43c0-104">句法</span><span class="sxs-lookup"><span data-stu-id="e43c0-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e43c0-105">說明</span><span class="sxs-lookup"><span data-stu-id="e43c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e43c0-106">**AzureRmStreamAnalyticsJob** Cmdlet 會以非同步方式停止資料流程分析作業，使其在 Azure 中執行，並解除所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="e43c0-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="e43c0-107">您可以透過 Azure 入口網站和管理 Api，在您的訂閱中保留作業定義與中繼資料，這樣就可以編輯及重新開機作業。</span><span class="sxs-lookup"><span data-stu-id="e43c0-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="e43c0-108">您不會針對處於停止狀態的工作收取費用。</span><span class="sxs-lookup"><span data-stu-id="e43c0-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="e43c0-109">示例</span><span class="sxs-lookup"><span data-stu-id="e43c0-109">EXAMPLES</span></span>

### <span data-ttu-id="e43c0-110">範例1：停止正在執行的工作</span><span class="sxs-lookup"><span data-stu-id="e43c0-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e43c0-111">這個命令會停止作業 StreamingJob。</span><span class="sxs-lookup"><span data-stu-id="e43c0-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="e43c0-112">參數</span><span class="sxs-lookup"><span data-stu-id="e43c0-112">PARAMETERS</span></span>

### <span data-ttu-id="e43c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43c0-113">-DefaultProfile</span></span>
<span data-ttu-id="e43c0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e43c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e43c0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e43c0-115">-Name</span></span>
<span data-ttu-id="e43c0-116">指定要停止的 Azure 串流分析作業名稱。</span><span class="sxs-lookup"><span data-stu-id="e43c0-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43c0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43c0-117">-ResourceGroupName</span></span>
<span data-ttu-id="e43c0-118">指定 Azure 資料流程分析作業所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e43c0-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43c0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43c0-119">CommonParameters</span></span>
<span data-ttu-id="e43c0-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e43c0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43c0-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e43c0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43c0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e43c0-122">INPUTS</span></span>

### <span data-ttu-id="e43c0-123">所有</span><span class="sxs-lookup"><span data-stu-id="e43c0-123">None</span></span>
<span data-ttu-id="e43c0-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e43c0-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e43c0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e43c0-125">OUTPUTS</span></span>

### <span data-ttu-id="e43c0-126">System.object</span><span class="sxs-lookup"><span data-stu-id="e43c0-126">System.Object</span></span>

## <span data-ttu-id="e43c0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e43c0-127">NOTES</span></span>

## <span data-ttu-id="e43c0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e43c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="e43c0-129">AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e43c0-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e43c0-130">AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e43c0-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e43c0-131">新-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e43c0-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e43c0-132">移除-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e43c0-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e43c0-133">開始-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e43c0-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


