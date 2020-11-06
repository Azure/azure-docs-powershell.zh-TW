---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 4836a7c016a86ad5fcbb1c926bc27f43215a44f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620722"
---
# <span data-ttu-id="ca6bd-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="ca6bd-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="ca6bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6bd-103">針對 Azure 搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="ca6bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca6bd-104">SYNTAX</span></span>

### <span data-ttu-id="ca6bd-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ca6bd-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca6bd-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca6bd-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca6bd-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca6bd-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca6bd-108">說明</span><span class="sxs-lookup"><span data-stu-id="ca6bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ca6bd-109">**新的-AzSearchQueryKey** Cmdlet 會針對 Azure 搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="ca6bd-110">示例</span><span class="sxs-lookup"><span data-stu-id="ca6bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ca6bd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ca6bd-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="ca6bd-112">這個範例會為 Azure 搜尋服務建立新的查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="ca6bd-113">參數</span><span class="sxs-lookup"><span data-stu-id="ca6bd-113">PARAMETERS</span></span>

### <span data-ttu-id="ca6bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6bd-114">-DefaultProfile</span></span>
<span data-ttu-id="ca6bd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca6bd-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca6bd-116">-Name</span></span>
<span data-ttu-id="ca6bd-117">搜尋服務查詢的索引鍵名。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="ca6bd-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca6bd-118">-ParentObject</span></span>
<span data-ttu-id="ca6bd-119">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="ca6bd-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca6bd-120">-ParentResourceId</span></span>
<span data-ttu-id="ca6bd-121">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="ca6bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca6bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca6bd-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-123">Resource Group name.</span></span>

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

### <span data-ttu-id="ca6bd-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ca6bd-124">-ServiceName</span></span>
<span data-ttu-id="ca6bd-125">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-125">Search Service name.</span></span>

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

### <span data-ttu-id="ca6bd-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ca6bd-126">-Confirm</span></span>
<span data-ttu-id="ca6bd-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca6bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca6bd-128">-WhatIf</span></span>
<span data-ttu-id="ca6bd-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca6bd-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca6bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6bd-131">CommonParameters</span></span>
<span data-ttu-id="ca6bd-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6bd-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6bd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ca6bd-134">INPUTS</span></span>

### <span data-ttu-id="ca6bd-135">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="ca6bd-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ca6bd-136">System.String</span></span>

## <span data-ttu-id="ca6bd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ca6bd-137">OUTPUTS</span></span>

### <span data-ttu-id="ca6bd-138">[PSSearchQueryKey]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="ca6bd-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="ca6bd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ca6bd-139">NOTES</span></span>

## <span data-ttu-id="ca6bd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca6bd-140">RELATED LINKS</span></span>

[<span data-ttu-id="ca6bd-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="ca6bd-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="ca6bd-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="ca6bd-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
