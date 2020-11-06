---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: dd2a52167a773b241364311ed4e0e00c03ea8459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448526"
---
# <span data-ttu-id="97a2c-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="97a2c-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="97a2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="97a2c-103">取得資料流程分析作業中的函數。</span><span class="sxs-lookup"><span data-stu-id="97a2c-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="97a2c-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="97a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="97a2c-106">**AzureRmStreamAnalyticsFunction** Cmdlet 會取得 Azure 資料流程分析作業中定義的函數清單，或特定函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97a2c-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="97a2c-107">示例</span><span class="sxs-lookup"><span data-stu-id="97a2c-107">EXAMPLES</span></span>

### <span data-ttu-id="97a2c-108">範例1：取得所有串流分析函數</span><span class="sxs-lookup"><span data-stu-id="97a2c-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="97a2c-109">這個命令會取得在名為 StreamJob22 的作業中定義的函數。</span><span class="sxs-lookup"><span data-stu-id="97a2c-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="97a2c-110">範例2：取得特定的資料流程分析函式函數</span><span class="sxs-lookup"><span data-stu-id="97a2c-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="97a2c-111">這個命令會在名為 StreamJob22 的作業上，取得名為 ScoreTweet 定義之函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97a2c-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="97a2c-112">參數</span><span class="sxs-lookup"><span data-stu-id="97a2c-112">PARAMETERS</span></span>

### <span data-ttu-id="97a2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a2c-113">-DefaultProfile</span></span>
<span data-ttu-id="97a2c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97a2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a2c-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="97a2c-115">-JobName</span></span>
<span data-ttu-id="97a2c-116">指定函數所歸屬之串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="97a2c-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="97a2c-117">這個 Cmdlet 會取得此參數指定作業的功能。</span><span class="sxs-lookup"><span data-stu-id="97a2c-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="97a2c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="97a2c-118">-Name</span></span>
<span data-ttu-id="97a2c-119">指定此 Cmdlet 取得的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="97a2c-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97a2c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a2c-120">-ResourceGroupName</span></span>
<span data-ttu-id="97a2c-121">指定串流分析函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97a2c-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="97a2c-122">這個 Cmdlet 會取得此參數指定之群組的函數。</span><span class="sxs-lookup"><span data-stu-id="97a2c-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="97a2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a2c-123">CommonParameters</span></span>
<span data-ttu-id="97a2c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97a2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a2c-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97a2c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a2c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="97a2c-126">INPUTS</span></span>

### <span data-ttu-id="97a2c-127">所有</span><span class="sxs-lookup"><span data-stu-id="97a2c-127">None</span></span>
<span data-ttu-id="97a2c-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="97a2c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97a2c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="97a2c-129">OUTPUTS</span></span>

### <span data-ttu-id="97a2c-130">[PSFunction]、[StreamAnalytics]、[StreamAnalytics]、[]、[]、[]、[StreamAnalytics. PSFunction]</span><span class="sxs-lookup"><span data-stu-id="97a2c-130">System.Collections.Generic.List[Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction, Microsoft.Azure.Commands.StreamAnalytics], Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="97a2c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="97a2c-131">NOTES</span></span>

## <span data-ttu-id="97a2c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="97a2c-132">RELATED LINKS</span></span>

[<span data-ttu-id="97a2c-133">新-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="97a2c-133">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="97a2c-134">移除-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="97a2c-134">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="97a2c-135">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="97a2c-135">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


