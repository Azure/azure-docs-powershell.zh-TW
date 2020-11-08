---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138328"
---
# <span data-ttu-id="c1a9b-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="c1a9b-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="c1a9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a9b-103">傳回指定工作區的所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="c1a9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1a9b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a9b-106">如果您沒有指定已儲存的搜尋識別碼， **AzOperationalInsightsSavedSearch** Cmdlet 會針對指定的資源群組中的指定工作區傳回所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="c1a9b-107">如果您指定已儲存的搜尋識別碼，則會傳回對應至該識別碼的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="c1a9b-108">示例</span><span class="sxs-lookup"><span data-stu-id="c1a9b-108">EXAMPLES</span></span>

### <span data-ttu-id="c1a9b-109">範例1：取得工作區的所有已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="c1a9b-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c1a9b-110">這個命令會取得與工作區關聯的所有已儲存資源。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="c1a9b-111">範例2：依識別碼取得特定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="c1a9b-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="c1a9b-112">這個命令會根據其識別碼來取得特定已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="c1a9b-113">參數</span><span class="sxs-lookup"><span data-stu-id="c1a9b-113">PARAMETERS</span></span>

### <span data-ttu-id="c1a9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a9b-114">-DefaultProfile</span></span>
<span data-ttu-id="c1a9b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c1a9b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1a9b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a9b-116">-ResourceGroupName</span></span>
<span data-ttu-id="c1a9b-117">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c1a9b-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="c1a9b-118">-SavedSearchId</span></span>
<span data-ttu-id="c1a9b-119">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="c1a9b-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c1a9b-120">-WorkspaceName</span></span>
<span data-ttu-id="c1a9b-121">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c1a9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a9b-122">CommonParameters</span></span>
<span data-ttu-id="c1a9b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a9b-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a9b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c1a9b-125">INPUTS</span></span>

### <span data-ttu-id="c1a9b-126">System.object</span><span class="sxs-lookup"><span data-stu-id="c1a9b-126">System.String</span></span>

## <span data-ttu-id="c1a9b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c1a9b-127">OUTPUTS</span></span>

### <span data-ttu-id="c1a9b-128">PSSearchListSavedSearchResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="c1a9b-129">PSSearchGetSavedSearchResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="c1a9b-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="c1a9b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="c1a9b-130">NOTES</span></span>

## <span data-ttu-id="c1a9b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1a9b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c1a9b-132">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c1a9b-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


