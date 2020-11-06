---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: cd947a29a9312c056133e5e7e302b130623bd698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443668"
---
# <span data-ttu-id="4cd06-101">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4cd06-101">Get-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="4cd06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cd06-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd06-103">取得資料流程分析作業中的函數。</span><span class="sxs-lookup"><span data-stu-id="4cd06-103">Gets functions in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cd06-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cd06-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cd06-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cd06-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd06-106">**AzureRmStreamAnalyticsFunction** Cmdlet 會取得 Azure 資料流程分析作業中定義的函數清單，或特定函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4cd06-106">The **Get-AzureRmStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="4cd06-107">示例</span><span class="sxs-lookup"><span data-stu-id="4cd06-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd06-108">範例1：取得所有串流分析函數</span><span class="sxs-lookup"><span data-stu-id="4cd06-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="4cd06-109">這個命令會取得在名為 StreamJob22 的作業中定義的函數。</span><span class="sxs-lookup"><span data-stu-id="4cd06-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="4cd06-110">範例2：取得特定的資料流程分析函式函數</span><span class="sxs-lookup"><span data-stu-id="4cd06-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="4cd06-111">這個命令會在名為 StreamJob22 的作業上，取得名為 ScoreTweet 定義之函數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4cd06-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="4cd06-112">參數</span><span class="sxs-lookup"><span data-stu-id="4cd06-112">PARAMETERS</span></span>

### <span data-ttu-id="4cd06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd06-113">-DefaultProfile</span></span>
<span data-ttu-id="4cd06-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cd06-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cd06-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="4cd06-115">-JobName</span></span>
<span data-ttu-id="4cd06-116">指定函數所歸屬之串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cd06-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="4cd06-117">這個 Cmdlet 會取得此參數指定作業的功能。</span><span class="sxs-lookup"><span data-stu-id="4cd06-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cd06-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cd06-118">-Name</span></span>
<span data-ttu-id="4cd06-119">指定此 Cmdlet 取得的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cd06-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd06-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cd06-121">指定串流分析函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cd06-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="4cd06-122">這個 Cmdlet 會取得此參數指定之群組的函數。</span><span class="sxs-lookup"><span data-stu-id="4cd06-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cd06-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd06-123">CommonParameters</span></span>
<span data-ttu-id="4cd06-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cd06-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd06-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cd06-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd06-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4cd06-126">INPUTS</span></span>

### <span data-ttu-id="4cd06-127">System.object</span><span class="sxs-lookup"><span data-stu-id="4cd06-127">System.String</span></span>

## <span data-ttu-id="4cd06-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4cd06-128">OUTPUTS</span></span>

### <span data-ttu-id="4cd06-129">PSFunction 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="4cd06-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="4cd06-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4cd06-130">NOTES</span></span>

## <span data-ttu-id="4cd06-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cd06-131">RELATED LINKS</span></span>

[<span data-ttu-id="4cd06-132">新-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4cd06-132">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="4cd06-133">移除-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4cd06-133">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="4cd06-134">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4cd06-134">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)

