---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 922989583a071384de98343e12d48ce68cc32db8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141811"
---
# <span data-ttu-id="0fb2c-101">Remove-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0fb2c-101">Remove-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="0fb2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0fb2c-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb2c-103">從 Azure 認知搜尋服務移除共用的私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-103">Remove the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0fb2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0fb2c-104">SYNTAX</span></span>

### <span data-ttu-id="0fb2c-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0fb2c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fb2c-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb2c-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb2c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb2c-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb2c-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fb2c-108">InputObjectParameterSet</span></span>
```
Remove-AzSearchSharedPrivateLinkResource -InputObject <PSSharedPrivateLinkResource> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb2c-109">說明</span><span class="sxs-lookup"><span data-stu-id="0fb2c-109">DESCRIPTION</span></span>
<span data-ttu-id="0fb2c-110">**AzSearchSharedPrivateLinkResource** Cmdlet 會從 Azure 認知搜尋服務移除共用的私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-110">The **Remove-AzSearchSharedPrivateLinkResource** cmdlet removes the shared private link resource from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0fb2c-111">示例</span><span class="sxs-lookup"><span data-stu-id="0fb2c-111">EXAMPLES</span></span>

### <span data-ttu-id="0fb2c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="0fb2c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe

Confirm
Remove Shared Private Link Resource 'blob-pe'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="0fb2c-113">這個範例會依 Azure 認知搜尋服務的名稱來刪除共用的私人連結資源。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-113">This example deletes a shared private link resource by name of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="0fb2c-114">參數</span><span class="sxs-lookup"><span data-stu-id="0fb2c-114">PARAMETERS</span></span>

### <span data-ttu-id="0fb2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fb2c-115">-AsJob</span></span>
<span data-ttu-id="0fb2c-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0fb2c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fb2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb2c-117">-DefaultProfile</span></span>
<span data-ttu-id="0fb2c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fb2c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0fb2c-119">-Force</span></span>
<span data-ttu-id="0fb2c-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0fb2c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fb2c-121">-InputObject</span></span>
<span data-ttu-id="0fb2c-122">共用私人連結資源輸入物件</span><span class="sxs-lookup"><span data-stu-id="0fb2c-122">Shared private link resource input object</span></span>

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

### <span data-ttu-id="0fb2c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="0fb2c-123">-Name</span></span>
<span data-ttu-id="0fb2c-124">Azure 認知搜尋共用的私人連結資源</span><span class="sxs-lookup"><span data-stu-id="0fb2c-124">Azure Cognitive Search Shared private link resource</span></span>

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

### <span data-ttu-id="0fb2c-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0fb2c-125">-ParentObject</span></span>
<span data-ttu-id="0fb2c-126">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-126">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="0fb2c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fb2c-127">-PassThru</span></span>
<span data-ttu-id="0fb2c-128">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0fb2c-129">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-129">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0fb2c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fb2c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0fb2c-131">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-131">Resource Group name.</span></span>

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

### <span data-ttu-id="0fb2c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fb2c-132">-ResourceId</span></span>
<span data-ttu-id="0fb2c-133">共用私人連結資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0fb2c-133">Shared private link resource id</span></span>

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

### <span data-ttu-id="0fb2c-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0fb2c-134">-ServiceName</span></span>
<span data-ttu-id="0fb2c-135">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-135">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="0fb2c-136">-確認</span><span class="sxs-lookup"><span data-stu-id="0fb2c-136">-Confirm</span></span>
<span data-ttu-id="0fb2c-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb2c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb2c-138">-WhatIf</span></span>
<span data-ttu-id="0fb2c-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fb2c-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb2c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb2c-141">CommonParameters</span></span>
<span data-ttu-id="0fb2c-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb2c-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0fb2c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb2c-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0fb2c-144">INPUTS</span></span>

### <span data-ttu-id="0fb2c-145">所有</span><span class="sxs-lookup"><span data-stu-id="0fb2c-145">None</span></span>

## <span data-ttu-id="0fb2c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="0fb2c-146">OUTPUTS</span></span>

### <span data-ttu-id="0fb2c-147">System.object</span><span class="sxs-lookup"><span data-stu-id="0fb2c-147">System.Boolean</span></span>

## <span data-ttu-id="0fb2c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="0fb2c-148">NOTES</span></span>

## <span data-ttu-id="0fb2c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fb2c-149">RELATED LINKS</span></span>

[<span data-ttu-id="0fb2c-150">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0fb2c-150">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="0fb2c-151">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0fb2c-151">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="0fb2c-152">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="0fb2c-152">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)