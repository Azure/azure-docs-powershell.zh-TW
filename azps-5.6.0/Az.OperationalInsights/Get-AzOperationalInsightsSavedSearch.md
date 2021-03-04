---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903446"
---
# <span data-ttu-id="54767-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="54767-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="54767-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54767-102">SYNOPSIS</span></span>
<span data-ttu-id="54767-103">會針對指定的工作區，會返回所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="54767-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="54767-104">語法</span><span class="sxs-lookup"><span data-stu-id="54767-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54767-105">描述</span><span class="sxs-lookup"><span data-stu-id="54767-105">DESCRIPTION</span></span>
<span data-ttu-id="54767-106">**Get-AzOperationalInsightsSavedSearch** Cmdlet 會針對指定的資源群組中指定的指定工作區，會針對您未指定儲存的搜尋識別碼，來將所有已儲存的搜尋內容全部寄回。</span><span class="sxs-lookup"><span data-stu-id="54767-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="54767-107">如果您指定已儲存的搜尋識別碼，則對應至該識別碼的已儲存搜尋會隨即返回。</span><span class="sxs-lookup"><span data-stu-id="54767-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="54767-108">例子</span><span class="sxs-lookup"><span data-stu-id="54767-108">EXAMPLES</span></span>

### <span data-ttu-id="54767-109">範例 1：取得工作區的所有已儲存搜尋</span><span class="sxs-lookup"><span data-stu-id="54767-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="54767-110">此命令會獲得所有與工作區相關聯的已儲存資源。</span><span class="sxs-lookup"><span data-stu-id="54767-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="54767-111">範例 2：取得特定的已儲存搜尋識別碼</span><span class="sxs-lookup"><span data-stu-id="54767-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="54767-112">此命令會以其識別碼獲得特定的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="54767-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="54767-113">參數</span><span class="sxs-lookup"><span data-stu-id="54767-113">PARAMETERS</span></span>

### <span data-ttu-id="54767-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54767-114">-DefaultProfile</span></span>
<span data-ttu-id="54767-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="54767-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54767-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54767-116">-ResourceGroupName</span></span>
<span data-ttu-id="54767-117">指定包含工作區的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="54767-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="54767-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="54767-118">-SavedSearchId</span></span>
<span data-ttu-id="54767-119">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="54767-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="54767-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54767-120">-WorkspaceName</span></span>
<span data-ttu-id="54767-121">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="54767-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="54767-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54767-122">CommonParameters</span></span>
<span data-ttu-id="54767-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54767-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54767-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="54767-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54767-125">輸入</span><span class="sxs-lookup"><span data-stu-id="54767-125">INPUTS</span></span>

### <span data-ttu-id="54767-126">System.String</span><span class="sxs-lookup"><span data-stu-id="54767-126">System.String</span></span>

## <span data-ttu-id="54767-127">輸出</span><span class="sxs-lookup"><span data-stu-id="54767-127">OUTPUTS</span></span>

### <span data-ttu-id="54767-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="54767-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="54767-129">Microsoft.Azure.Commands.OperationalInsights.models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="54767-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="54767-130">筆記</span><span class="sxs-lookup"><span data-stu-id="54767-130">NOTES</span></span>

## <span data-ttu-id="54767-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="54767-131">RELATED LINKS</span></span>

[<span data-ttu-id="54767-132">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54767-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


