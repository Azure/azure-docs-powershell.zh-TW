---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451780"
---
# <span data-ttu-id="4cc2b-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="4cc2b-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="4cc2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cc2b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc2b-103">針對 Azure 搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cc2b-104">SYNTAX</span></span>

### <span data-ttu-id="4cc2b-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4cc2b-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc2b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc2b-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc2b-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc2b-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc2b-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cc2b-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc2b-109">**新的-AzureRmSearchQueryKey** Cmdlet 會針對 Azure 搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="4cc2b-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cc2b-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc2b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4cc2b-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="4cc2b-112">這個範例會為 Azure 搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="4cc2b-113">參數</span><span class="sxs-lookup"><span data-stu-id="4cc2b-113">PARAMETERS</span></span>

### <span data-ttu-id="4cc2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc2b-114">-DefaultProfile</span></span>
<span data-ttu-id="4cc2b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cc2b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cc2b-116">-Name</span></span>
<span data-ttu-id="4cc2b-117">搜尋服務查詢的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-117">Search Service query key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4cc2b-118">-ParentObject</span></span>
<span data-ttu-id="4cc2b-119">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4cc2b-120">-ParentResourceId</span></span>
<span data-ttu-id="4cc2b-121">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-121">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4cc2b-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4cc2b-124">-ServiceName</span></span>
<span data-ttu-id="4cc2b-125">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-125">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4cc2b-126">-Confirm</span></span>
<span data-ttu-id="4cc2b-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc2b-128">-WhatIf</span></span>
<span data-ttu-id="4cc2b-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cc2b-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc2b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc2b-131">CommonParameters</span></span>
<span data-ttu-id="4cc2b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc2b-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc2b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4cc2b-134">INPUTS</span></span>

### <span data-ttu-id="4cc2b-135">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="4cc2b-136">參數： ParentObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4cc2b-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="4cc2b-137">System.object</span><span class="sxs-lookup"><span data-stu-id="4cc2b-137">System.String</span></span>

## <span data-ttu-id="4cc2b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4cc2b-138">OUTPUTS</span></span>

### <span data-ttu-id="4cc2b-139">[PSSearchQueryKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="4cc2b-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="4cc2b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4cc2b-140">NOTES</span></span>

## <span data-ttu-id="4cc2b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cc2b-141">RELATED LINKS</span></span>

[<span data-ttu-id="4cc2b-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="4cc2b-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="4cc2b-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="4cc2b-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
