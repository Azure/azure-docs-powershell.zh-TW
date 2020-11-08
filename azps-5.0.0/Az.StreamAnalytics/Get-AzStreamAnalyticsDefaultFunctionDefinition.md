---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139427"
---
# <span data-ttu-id="53a1c-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="53a1c-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="53a1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="53a1c-103">取得資料流程分析中函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="53a1c-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="53a1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="53a1c-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="53a1c-105">DESCRIPTION</span></span>
<span data-ttu-id="53a1c-106">**AzStreamAnalyticsDefaultFunctionDefinition** Cmdlet 會取得 Azure 資料流程分析中函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="53a1c-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="53a1c-107">您可以使用預設定義和 New-AzStreamAnalyticsFunction Cmdlet 來建立函數。</span><span class="sxs-lookup"><span data-stu-id="53a1c-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="53a1c-108">您可以在建立函數之前修改預設定義。</span><span class="sxs-lookup"><span data-stu-id="53a1c-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="53a1c-109">示例</span><span class="sxs-lookup"><span data-stu-id="53a1c-109">EXAMPLES</span></span>

### <span data-ttu-id="53a1c-110">範例1：取得串流分析函數的預設定義</span><span class="sxs-lookup"><span data-stu-id="53a1c-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="53a1c-111">這個命令會使用 RetrieveDefaultDefinitionRequest.js的檔案中指定的參數，來取得名為 ScoreTweet 之函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="53a1c-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="53a1c-112">參數</span><span class="sxs-lookup"><span data-stu-id="53a1c-112">PARAMETERS</span></span>

### <span data-ttu-id="53a1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a1c-113">-DefaultProfile</span></span>
<span data-ttu-id="53a1c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a1c-115">檔案</span><span class="sxs-lookup"><span data-stu-id="53a1c-115">-File</span></span>
<span data-ttu-id="53a1c-116">指定包含 JavaScript 物件符號的 json 檔案的路徑，該檔案在取得預設函式定義要求的要求主體 (JSON) 表示形式。</span><span class="sxs-lookup"><span data-stu-id="53a1c-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a1c-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="53a1c-117">-JobName</span></span>
<span data-ttu-id="53a1c-118">指定函數所歸屬之串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a1c-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="53a1c-119">這個 Cmdlet 會取得此參數指定作業中函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="53a1c-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="53a1c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="53a1c-120">-Name</span></span>
<span data-ttu-id="53a1c-121">指定此 Cmdlet 取得預設定義的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a1c-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="53a1c-123">指定串流分析函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a1c-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="53a1c-124">這個 Cmdlet 會取得此參數指定之群組的函式定義。</span><span class="sxs-lookup"><span data-stu-id="53a1c-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53a1c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a1c-125">CommonParameters</span></span>
<span data-ttu-id="53a1c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53a1c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a1c-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53a1c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a1c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="53a1c-128">INPUTS</span></span>

### <span data-ttu-id="53a1c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="53a1c-129">System.String</span></span>

## <span data-ttu-id="53a1c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="53a1c-130">OUTPUTS</span></span>

### <span data-ttu-id="53a1c-131">PSFunction 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="53a1c-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="53a1c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="53a1c-132">NOTES</span></span>

## <span data-ttu-id="53a1c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a1c-133">RELATED LINKS</span></span>

[<span data-ttu-id="53a1c-134">新-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53a1c-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


