---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 4daf2a86515522c3843d5d0225c133f0ff3686ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452444"
---
# <span data-ttu-id="49117-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="49117-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="49117-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49117-102">SYNOPSIS</span></span>
<span data-ttu-id="49117-103">傳回指定工作區的所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="49117-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49117-104">句法</span><span class="sxs-lookup"><span data-stu-id="49117-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49117-105">說明</span><span class="sxs-lookup"><span data-stu-id="49117-105">DESCRIPTION</span></span>
<span data-ttu-id="49117-106">如果您沒有指定已儲存的搜尋識別碼， **AzureRmOperationalInsightsSavedSearch** Cmdlet 會針對指定的資源群組中的指定工作區傳回所有已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="49117-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="49117-107">如果您指定已儲存的搜尋識別碼，則會傳回對應至該識別碼的已儲存搜尋。</span><span class="sxs-lookup"><span data-stu-id="49117-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="49117-108">示例</span><span class="sxs-lookup"><span data-stu-id="49117-108">EXAMPLES</span></span>

### <span data-ttu-id="49117-109">範例1：取得工作區的所有已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="49117-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="49117-110">這個命令會取得與工作區關聯的所有已儲存資源。</span><span class="sxs-lookup"><span data-stu-id="49117-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="49117-111">範例2：依識別碼取得特定已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="49117-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="49117-112">這個命令會根據其識別碼來取得特定已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="49117-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="49117-113">參數</span><span class="sxs-lookup"><span data-stu-id="49117-113">PARAMETERS</span></span>

### <span data-ttu-id="49117-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49117-114">-ResourceGroupName</span></span>
<span data-ttu-id="49117-115">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49117-115">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="49117-116">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="49117-116">-SavedSearchId</span></span>
<span data-ttu-id="49117-117">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="49117-117">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="49117-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="49117-118">-WorkspaceName</span></span>
<span data-ttu-id="49117-119">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="49117-119">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="49117-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49117-120">-DefaultProfile</span></span>
<span data-ttu-id="49117-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49117-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49117-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49117-122">CommonParameters</span></span>
<span data-ttu-id="49117-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49117-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49117-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49117-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49117-125">輸入</span><span class="sxs-lookup"><span data-stu-id="49117-125">INPUTS</span></span>

## <span data-ttu-id="49117-126">輸出</span><span class="sxs-lookup"><span data-stu-id="49117-126">OUTPUTS</span></span>

### <span data-ttu-id="49117-127">PSSearchListSavedSearchResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="49117-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="49117-128">PSSearchGetSavedSearchResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="49117-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="49117-129">筆記</span><span class="sxs-lookup"><span data-stu-id="49117-129">NOTES</span></span>

## <span data-ttu-id="49117-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="49117-130">RELATED LINKS</span></span>

[<span data-ttu-id="49117-131">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="49117-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


