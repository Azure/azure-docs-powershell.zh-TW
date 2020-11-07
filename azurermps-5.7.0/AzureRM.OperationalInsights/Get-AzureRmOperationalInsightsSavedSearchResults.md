---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623809"
---
# <span data-ttu-id="e5da9-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="e5da9-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="e5da9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5da9-102">SYNOPSIS</span></span>
<span data-ttu-id="e5da9-103">傳回查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="e5da9-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5da9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5da9-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5da9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5da9-105">DESCRIPTION</span></span>
<span data-ttu-id="e5da9-106">**AzureRmOperationalInsightsSavedSearchResults** Cmdlet 會傳回搜尋識別碼所指定之查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="e5da9-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="e5da9-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5da9-107">EXAMPLES</span></span>

### <span data-ttu-id="e5da9-108">範例1：取得已儲存之搜尋的所有搜尋結果</span><span class="sxs-lookup"><span data-stu-id="e5da9-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="e5da9-109">這個命令會取得已儲存之搜尋的所有搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="e5da9-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="e5da9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5da9-110">PARAMETERS</span></span>

### <span data-ttu-id="e5da9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5da9-111">-DefaultProfile</span></span>
<span data-ttu-id="e5da9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5da9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5da9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5da9-113">-ResourceGroupName</span></span>
<span data-ttu-id="e5da9-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5da9-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e5da9-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e5da9-115">-SavedSearchId</span></span>
<span data-ttu-id="e5da9-116">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5da9-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="e5da9-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5da9-117">-WorkspaceName</span></span>
<span data-ttu-id="e5da9-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e5da9-118">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5da9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5da9-119">CommonParameters</span></span>
<span data-ttu-id="e5da9-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5da9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5da9-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5da9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5da9-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e5da9-122">INPUTS</span></span>

### <span data-ttu-id="e5da9-123">所有</span><span class="sxs-lookup"><span data-stu-id="e5da9-123">None</span></span>
<span data-ttu-id="e5da9-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e5da9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5da9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e5da9-125">OUTPUTS</span></span>

### <span data-ttu-id="e5da9-126">PSSearchGetSearchResultsResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="e5da9-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="e5da9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e5da9-127">NOTES</span></span>

## <span data-ttu-id="e5da9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5da9-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5da9-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5da9-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


