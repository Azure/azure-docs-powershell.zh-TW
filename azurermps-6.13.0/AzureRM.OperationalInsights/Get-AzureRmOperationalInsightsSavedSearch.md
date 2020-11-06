---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 712fac06a960eebe546f4554731f69286615b0ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447312"
---
# <span data-ttu-id="7609d-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7609d-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="7609d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7609d-102">SYNOPSIS</span></span>
<span data-ttu-id="7609d-103">傳回指定工作區的所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="7609d-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7609d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7609d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7609d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7609d-105">DESCRIPTION</span></span>
<span data-ttu-id="7609d-106">如果您沒有指定已儲存的搜尋識別碼， **AzureRmOperationalInsightsSavedSearch** Cmdlet 會針對指定的資源群組中的指定工作區傳回所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="7609d-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="7609d-107">如果您指定已儲存的搜尋識別碼，則會傳回對應至該識別碼的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="7609d-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="7609d-108">示例</span><span class="sxs-lookup"><span data-stu-id="7609d-108">EXAMPLES</span></span>

### <span data-ttu-id="7609d-109">範例1：取得工作區的所有已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="7609d-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7609d-110">這個命令會取得與工作區關聯的所有已儲存資源。</span><span class="sxs-lookup"><span data-stu-id="7609d-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="7609d-111">範例2：依識別碼取得特定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="7609d-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="7609d-112">這個命令會根據其識別碼來取得特定已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="7609d-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="7609d-113">參數</span><span class="sxs-lookup"><span data-stu-id="7609d-113">PARAMETERS</span></span>

### <span data-ttu-id="7609d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7609d-114">-DefaultProfile</span></span>
<span data-ttu-id="7609d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7609d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7609d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7609d-116">-ResourceGroupName</span></span>
<span data-ttu-id="7609d-117">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7609d-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="7609d-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="7609d-118">-SavedSearchId</span></span>
<span data-ttu-id="7609d-119">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="7609d-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="7609d-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7609d-120">-WorkspaceName</span></span>
<span data-ttu-id="7609d-121">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7609d-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="7609d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7609d-122">CommonParameters</span></span>
<span data-ttu-id="7609d-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7609d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7609d-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7609d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7609d-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7609d-125">INPUTS</span></span>

### <span data-ttu-id="7609d-126">System.object</span><span class="sxs-lookup"><span data-stu-id="7609d-126">System.String</span></span>

## <span data-ttu-id="7609d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7609d-127">OUTPUTS</span></span>

### <span data-ttu-id="7609d-128">PSSearchListSavedSearchResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="7609d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="7609d-129">PSSearchGetSavedSearchResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="7609d-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="7609d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7609d-130">NOTES</span></span>

## <span data-ttu-id="7609d-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7609d-131">RELATED LINKS</span></span>

[<span data-ttu-id="7609d-132">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7609d-132">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


