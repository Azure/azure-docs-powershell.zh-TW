---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: ff9ab6f4efe5794b3f1eca9b8ceab91b5cd11316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450419"
---
# <span data-ttu-id="c22c4-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c22c4-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="c22c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c22c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c22c4-103">取得指定串流分析作業或輸出中定義的輸出。</span><span class="sxs-lookup"><span data-stu-id="c22c4-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c22c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="c22c4-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="c22c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c22c4-106">**AzureRmStreamAnalyticsOutput** Cmdlet 會列出在指定的資料流程分析作業中定義的所有輸出，或取得特定輸出的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c22c4-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="c22c4-107">示例</span><span class="sxs-lookup"><span data-stu-id="c22c4-107">EXAMPLES</span></span>

### <span data-ttu-id="c22c4-108">範例1：取得作業輸出的相關資訊</span><span class="sxs-lookup"><span data-stu-id="c22c4-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="c22c4-109">這個命令會傳回有關作業 StreamingJob 上所定義之輸出的資訊。</span><span class="sxs-lookup"><span data-stu-id="c22c4-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="c22c4-110">範例2：取得特定作業輸出的相關資訊</span><span class="sxs-lookup"><span data-stu-id="c22c4-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="c22c4-111">這個命令會傳回有關作業 StreamingJob 上所定義之輸出命名輸出的資訊。</span><span class="sxs-lookup"><span data-stu-id="c22c4-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="c22c4-112">參數</span><span class="sxs-lookup"><span data-stu-id="c22c4-112">PARAMETERS</span></span>

### <span data-ttu-id="c22c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22c4-113">-DefaultProfile</span></span>
<span data-ttu-id="c22c4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c22c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c22c4-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="c22c4-115">-JobName</span></span>
<span data-ttu-id="c22c4-116">指定 Azure 資料流程分析輸出所屬之 Azure 串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="c22c4-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c22c4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c22c4-117">-Name</span></span>
<span data-ttu-id="c22c4-118">指定要檢索之 Azure 串流分析輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="c22c4-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="c22c4-120">指定 Azure 資料流程分析輸出所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c22c4-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="c22c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22c4-121">CommonParameters</span></span>
<span data-ttu-id="c22c4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c22c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22c4-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c22c4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22c4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c22c4-124">INPUTS</span></span>

### <span data-ttu-id="c22c4-125">所有</span><span class="sxs-lookup"><span data-stu-id="c22c4-125">None</span></span>
<span data-ttu-id="c22c4-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c22c4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c22c4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c22c4-127">OUTPUTS</span></span>

### <span data-ttu-id="c22c4-128">[System.object]. 清單 ' 1 [StreamAnalytics. PSOutput，StreamAnalytics]]]]]]]]]]]]</span><span class="sxs-lookup"><span data-stu-id="c22c4-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="c22c4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c22c4-129">NOTES</span></span>

## <span data-ttu-id="c22c4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c22c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="c22c4-131">新-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c22c4-131">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="c22c4-132">移除-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c22c4-132">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="c22c4-133">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="c22c4-133">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


