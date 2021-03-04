---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: ed5c5bf502e1d19b0ba095e5db68f1f116a71137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902837"
---
# <span data-ttu-id="12666-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="12666-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="12666-102">簡介</span><span class="sxs-lookup"><span data-stu-id="12666-102">SYNOPSIS</span></span>
<span data-ttu-id="12666-103">從 Azure 認知搜尋服務移除共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="12666-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="12666-104">語法</span><span class="sxs-lookup"><span data-stu-id="12666-104">SYNTAX</span></span>

### <span data-ttu-id="12666-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="12666-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12666-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12666-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12666-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12666-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12666-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12666-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12666-109">描述</span><span class="sxs-lookup"><span data-stu-id="12666-109">DESCRIPTION</span></span>
<span data-ttu-id="12666-110">**Remove-AzSearchSharedPrivateLinkResource** Cmdlet 會從 Azure 認知搜尋服務移除共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="12666-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="12666-111">例子</span><span class="sxs-lookup"><span data-stu-id="12666-111">EXAMPLES</span></span>

### <span data-ttu-id="12666-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="12666-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="12666-113">此範例會刪除 Azure 認知搜尋服務名稱的共用私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="12666-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="12666-114">參數</span><span class="sxs-lookup"><span data-stu-id="12666-114">PARAMETERS</span></span>

### <span data-ttu-id="12666-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12666-115">-AsJob</span></span>
<span data-ttu-id="12666-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="12666-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12666-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12666-117">-DefaultProfile</span></span>
<span data-ttu-id="12666-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="12666-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12666-119">-強制</span><span class="sxs-lookup"><span data-stu-id="12666-119">-Force</span></span>
<span data-ttu-id="12666-120">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="12666-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="12666-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12666-121">-InputObject</span></span>
<span data-ttu-id="12666-122">共用私人連結資源輸入物件</span><span class="sxs-lookup"><span data-stu-id="12666-122">Shared private link resource input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12666-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="12666-123">-Name</span></span>
<span data-ttu-id="12666-124">Azure 認知搜尋共用私人連結資源</span><span class="sxs-lookup"><span data-stu-id="12666-124">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12666-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="12666-125">-ParentObject</span></span>
<span data-ttu-id="12666-126">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="12666-126">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12666-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12666-127">-PassThru</span></span>
<span data-ttu-id="12666-128">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="12666-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="12666-129">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="12666-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="12666-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12666-130">-ResourceGroupName</span></span>
<span data-ttu-id="12666-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="12666-131">Resource Group name.</span></span>

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

### <span data-ttu-id="12666-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12666-132">-ResourceId</span></span>
<span data-ttu-id="12666-133">共用私人連結資源識別碼</span><span class="sxs-lookup"><span data-stu-id="12666-133">Shared private link resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12666-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="12666-134">-ServiceName</span></span>
<span data-ttu-id="12666-135">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="12666-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="12666-136">-確認</span><span class="sxs-lookup"><span data-stu-id="12666-136">-Confirm</span></span>
<span data-ttu-id="12666-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="12666-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12666-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12666-138">-WhatIf</span></span>
<span data-ttu-id="12666-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12666-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12666-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12666-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12666-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12666-141">CommonParameters</span></span>
<span data-ttu-id="12666-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="12666-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12666-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12666-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12666-144">輸入</span><span class="sxs-lookup"><span data-stu-id="12666-144">INPUTS</span></span>

### <span data-ttu-id="12666-145">沒有</span><span class="sxs-lookup"><span data-stu-id="12666-145">None</span></span>

## <span data-ttu-id="12666-146">輸出</span><span class="sxs-lookup"><span data-stu-id="12666-146">OUTPUTS</span></span>

### <span data-ttu-id="12666-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="12666-147">System.Boolean</span></span>

## <span data-ttu-id="12666-148">筆記</span><span class="sxs-lookup"><span data-stu-id="12666-148">NOTES</span></span>

## <span data-ttu-id="12666-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="12666-149">RELATED LINKS</span></span>

[<span data-ttu-id="12666-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="12666-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="12666-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="12666-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="12666-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="12666-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)