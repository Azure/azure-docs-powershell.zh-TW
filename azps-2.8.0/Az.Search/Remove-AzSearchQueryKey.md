---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: ae781b4c53e373cdbd8338f4db75d6913c863bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791121"
---
# <span data-ttu-id="0b83c-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="0b83c-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="0b83c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b83c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b83c-103">從 Azure 搜尋服務移除查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="0b83c-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="0b83c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b83c-104">SYNTAX</span></span>

### <span data-ttu-id="0b83c-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b83c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b83c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b83c-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b83c-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b83c-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b83c-108">說明</span><span class="sxs-lookup"><span data-stu-id="0b83c-108">DESCRIPTION</span></span>
<span data-ttu-id="0b83c-109">**AzSearchQueryKey** Cmdlet 會從 Azure 搜尋服務中移除查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="0b83c-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="0b83c-110">示例</span><span class="sxs-lookup"><span data-stu-id="0b83c-110">EXAMPLES</span></span>

### <span data-ttu-id="0b83c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0b83c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="0b83c-112">此範例會從 Azure 搜尋服務移除查詢鍵。</span><span class="sxs-lookup"><span data-stu-id="0b83c-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="0b83c-113">參數</span><span class="sxs-lookup"><span data-stu-id="0b83c-113">PARAMETERS</span></span>

### <span data-ttu-id="0b83c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b83c-114">-DefaultProfile</span></span>
<span data-ttu-id="0b83c-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b83c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b83c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0b83c-116">-Force</span></span>
<span data-ttu-id="0b83c-117">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0b83c-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b83c-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="0b83c-118">-KeyValue</span></span>
<span data-ttu-id="0b83c-119">搜尋服務查詢項值。</span><span class="sxs-lookup"><span data-stu-id="0b83c-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="0b83c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0b83c-120">-ParentObject</span></span>
<span data-ttu-id="0b83c-121">搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0b83c-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="0b83c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0b83c-122">-ParentResourceId</span></span>
<span data-ttu-id="0b83c-123">搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b83c-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="0b83c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b83c-124">-PassThru</span></span>
<span data-ttu-id="0b83c-125">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="0b83c-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="0b83c-126">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="0b83c-126">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b83c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b83c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0b83c-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0b83c-128">Resource Group name.</span></span>

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

### <span data-ttu-id="0b83c-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0b83c-129">-ServiceName</span></span>
<span data-ttu-id="0b83c-130">搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0b83c-130">Search Service name.</span></span>

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

### <span data-ttu-id="0b83c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0b83c-131">-Confirm</span></span>
<span data-ttu-id="0b83c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b83c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b83c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b83c-133">-WhatIf</span></span>
<span data-ttu-id="0b83c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b83c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b83c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b83c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b83c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b83c-136">CommonParameters</span></span>
<span data-ttu-id="0b83c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b83c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b83c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b83c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b83c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0b83c-139">INPUTS</span></span>

### <span data-ttu-id="0b83c-140">[PSSearchService]，然後按 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0b83c-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="0b83c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="0b83c-141">System.String</span></span>

## <span data-ttu-id="0b83c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0b83c-142">OUTPUTS</span></span>

### <span data-ttu-id="0b83c-143">System.object</span><span class="sxs-lookup"><span data-stu-id="0b83c-143">System.Boolean</span></span>

## <span data-ttu-id="0b83c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0b83c-144">NOTES</span></span>

## <span data-ttu-id="0b83c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b83c-145">RELATED LINKS</span></span>

[<span data-ttu-id="0b83c-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="0b83c-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="0b83c-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="0b83c-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
