---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 0d813f6d0834a40708cc828d5b508cc6452dffc1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93623383"
---
# <span data-ttu-id="d8cea-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="d8cea-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="d8cea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8cea-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cea-103">傳回查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="d8cea-103">Returns the results from a query.</span></span>

## <span data-ttu-id="d8cea-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8cea-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8cea-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8cea-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cea-106">**AzOperationalInsightsSavedSearchResult** Cmdlet 會傳回搜尋識別碼所指定之查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="d8cea-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="d8cea-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8cea-107">EXAMPLES</span></span>

### <span data-ttu-id="d8cea-108">範例1：取得已儲存之搜尋的所有搜尋結果</span><span class="sxs-lookup"><span data-stu-id="d8cea-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="d8cea-109">這個命令會取得已儲存之搜尋的所有搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="d8cea-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="d8cea-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8cea-110">PARAMETERS</span></span>

### <span data-ttu-id="d8cea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cea-111">-DefaultProfile</span></span>
<span data-ttu-id="d8cea-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d8cea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8cea-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cea-113">-ResourceGroupName</span></span>
<span data-ttu-id="d8cea-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8cea-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d8cea-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d8cea-115">-SavedSearchId</span></span>
<span data-ttu-id="d8cea-116">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8cea-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="d8cea-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8cea-117">-WorkspaceName</span></span>
<span data-ttu-id="d8cea-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d8cea-118">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cea-119">CommonParameters</span></span>
<span data-ttu-id="d8cea-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8cea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cea-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8cea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cea-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d8cea-122">INPUTS</span></span>

### <span data-ttu-id="d8cea-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d8cea-123">System.String</span></span>

## <span data-ttu-id="d8cea-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d8cea-124">OUTPUTS</span></span>

### <span data-ttu-id="d8cea-125">PSSearchGetSearchResultsResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="d8cea-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="d8cea-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d8cea-126">NOTES</span></span>

## <span data-ttu-id="d8cea-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8cea-127">RELATED LINKS</span></span>

[<span data-ttu-id="d8cea-128">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d8cea-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


