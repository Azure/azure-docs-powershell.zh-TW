---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 88adac87543c0a51542cc0f79f2f1eb10ca8184b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453347"
---
# <span data-ttu-id="e0682-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="e0682-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="e0682-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0682-102">SYNOPSIS</span></span>
<span data-ttu-id="e0682-103">傳回查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="e0682-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0682-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0682-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0682-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0682-105">DESCRIPTION</span></span>
<span data-ttu-id="e0682-106">**AzureRmOperationalInsightsSavedSearchResults** Cmdlet 會傳回搜尋識別碼所指定之查詢的結果。</span><span class="sxs-lookup"><span data-stu-id="e0682-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="e0682-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0682-107">EXAMPLES</span></span>

### <span data-ttu-id="e0682-108">範例1：取得已儲存之搜尋的所有搜尋結果</span><span class="sxs-lookup"><span data-stu-id="e0682-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="e0682-109">這個命令會取得已儲存之搜尋的所有搜尋結果。</span><span class="sxs-lookup"><span data-stu-id="e0682-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="e0682-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0682-110">PARAMETERS</span></span>

### <span data-ttu-id="e0682-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0682-111">-ResourceGroupName</span></span>
<span data-ttu-id="e0682-112">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0682-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="e0682-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e0682-113">-SavedSearchId</span></span>
<span data-ttu-id="e0682-114">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0682-114">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="e0682-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0682-115">-WorkspaceName</span></span>
<span data-ttu-id="e0682-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e0682-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="e0682-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0682-117">-DefaultProfile</span></span>
<span data-ttu-id="e0682-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0682-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0682-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0682-119">CommonParameters</span></span>
<span data-ttu-id="e0682-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0682-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0682-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0682-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0682-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e0682-122">INPUTS</span></span>

## <span data-ttu-id="e0682-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e0682-123">OUTPUTS</span></span>

### <span data-ttu-id="e0682-124">PSSearchGetSearchResultsResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="e0682-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="e0682-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e0682-125">NOTES</span></span>

## <span data-ttu-id="e0682-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0682-126">RELATED LINKS</span></span>

[<span data-ttu-id="e0682-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e0682-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


