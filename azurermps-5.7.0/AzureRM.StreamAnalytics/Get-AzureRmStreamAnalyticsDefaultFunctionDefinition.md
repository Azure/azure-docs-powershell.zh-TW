---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: bc04c78538e808ce67813a3d706c35817102cfc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447570"
---
# <span data-ttu-id="4b316-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="4b316-101">Get-AzureRmStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="4b316-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b316-102">SYNOPSIS</span></span>
<span data-ttu-id="4b316-103">取得資料流程分析中函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="4b316-103">Gets the default definition of a function in Stream Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b316-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b316-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b316-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b316-105">DESCRIPTION</span></span>
<span data-ttu-id="4b316-106">**AzureRmStreamAnalyticsDefaultFunctionDefinition** Cmdlet 會取得 Azure 資料流程分析中函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="4b316-106">The **Get-AzureRmStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="4b316-107">您可以使用預設定義和 New-AzureRmStreamAnalyticsFunction Cmdlet 來建立函數。</span><span class="sxs-lookup"><span data-stu-id="4b316-107">You can use the default definition and the New-AzureRmStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="4b316-108">您可以在建立函數之前修改預設定義。</span><span class="sxs-lookup"><span data-stu-id="4b316-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="4b316-109">示例</span><span class="sxs-lookup"><span data-stu-id="4b316-109">EXAMPLES</span></span>

### <span data-ttu-id="4b316-110">範例1：取得串流分析函數的預設定義</span><span class="sxs-lookup"><span data-stu-id="4b316-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="4b316-111">這個命令會使用 RetrieveDefaultDefinitionRequest.js的檔案中指定的參數，來取得名為 ScoreTweet 之函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="4b316-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="4b316-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b316-112">PARAMETERS</span></span>

### <span data-ttu-id="4b316-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b316-113">-DefaultProfile</span></span>
<span data-ttu-id="4b316-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b316-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b316-115">檔案</span><span class="sxs-lookup"><span data-stu-id="4b316-115">-File</span></span>
<span data-ttu-id="4b316-116">指定包含 JavaScript 物件符號的 json 檔案的路徑，該檔案在取得預設函式定義要求的要求主體 (JSON) 表示形式。</span><span class="sxs-lookup"><span data-stu-id="4b316-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b316-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="4b316-117">-JobName</span></span>
<span data-ttu-id="4b316-118">指定函數所歸屬之串流分析作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b316-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="4b316-119">這個 Cmdlet 會取得此參數指定作業中函數的預設定義。</span><span class="sxs-lookup"><span data-stu-id="4b316-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b316-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b316-120">-Name</span></span>
<span data-ttu-id="4b316-121">指定此 Cmdlet 取得預設定義的資料流程分析函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b316-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b316-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b316-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b316-123">指定串流分析函數所歸屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b316-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="4b316-124">這個 Cmdlet 會取得此參數指定之群組的函式定義。</span><span class="sxs-lookup"><span data-stu-id="4b316-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b316-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b316-125">CommonParameters</span></span>
<span data-ttu-id="4b316-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b316-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b316-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b316-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b316-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4b316-128">INPUTS</span></span>

### <span data-ttu-id="4b316-129">所有</span><span class="sxs-lookup"><span data-stu-id="4b316-129">None</span></span>
<span data-ttu-id="4b316-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4b316-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b316-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4b316-131">OUTPUTS</span></span>

### <span data-ttu-id="4b316-132">PSFunction 中的 StreamAnalytics。</span><span class="sxs-lookup"><span data-stu-id="4b316-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="4b316-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4b316-133">NOTES</span></span>

## <span data-ttu-id="4b316-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b316-134">RELATED LINKS</span></span>

[<span data-ttu-id="4b316-135">新-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4b316-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)


