---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 7edca2e338c4972550d44cc6409187dbc53ab40b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135366"
---
# <span data-ttu-id="c7bdb-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="c7bdb-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="c7bdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bdb-103">針對 Azure 認知搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c7bdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7bdb-104">SYNTAX</span></span>

### <span data-ttu-id="c7bdb-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c7bdb-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bdb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7bdb-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7bdb-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7bdb-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bdb-108">說明</span><span class="sxs-lookup"><span data-stu-id="c7bdb-108">DESCRIPTION</span></span>
<span data-ttu-id="c7bdb-109">**新的-AzSearchQueryKey** Cmdlet 會為 Azure 認知搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c7bdb-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7bdb-110">EXAMPLES</span></span>

### <span data-ttu-id="c7bdb-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c7bdb-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="c7bdb-112">這個範例會為 Azure 認知搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c7bdb-113">參數</span><span class="sxs-lookup"><span data-stu-id="c7bdb-113">PARAMETERS</span></span>

### <span data-ttu-id="c7bdb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bdb-114">-DefaultProfile</span></span>
<span data-ttu-id="c7bdb-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7bdb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7bdb-116">-Name</span></span>
<span data-ttu-id="c7bdb-117">Azure 認知搜尋服務查詢金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="c7bdb-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c7bdb-118">-ParentObject</span></span>
<span data-ttu-id="c7bdb-119">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="c7bdb-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c7bdb-120">-ParentResourceId</span></span>
<span data-ttu-id="c7bdb-121">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-121">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c7bdb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7bdb-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7bdb-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-123">Resource Group name.</span></span>

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

### <span data-ttu-id="c7bdb-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7bdb-124">-ServiceName</span></span>
<span data-ttu-id="c7bdb-125">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-125">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="c7bdb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c7bdb-126">-Confirm</span></span>
<span data-ttu-id="c7bdb-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bdb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bdb-128">-WhatIf</span></span>
<span data-ttu-id="c7bdb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7bdb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bdb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bdb-131">CommonParameters</span></span>
<span data-ttu-id="c7bdb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bdb-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bdb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c7bdb-134">INPUTS</span></span>

### <span data-ttu-id="c7bdb-135">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c7bdb-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c7bdb-136">System.String</span></span>

## <span data-ttu-id="c7bdb-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c7bdb-137">OUTPUTS</span></span>

### <span data-ttu-id="c7bdb-138">[PSSearchQueryKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="c7bdb-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="c7bdb-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c7bdb-139">NOTES</span></span>

## <span data-ttu-id="c7bdb-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7bdb-140">RELATED LINKS</span></span>

[<span data-ttu-id="c7bdb-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c7bdb-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="c7bdb-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="c7bdb-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
