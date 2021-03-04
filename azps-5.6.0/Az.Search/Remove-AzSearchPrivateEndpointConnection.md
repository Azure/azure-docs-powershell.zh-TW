---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 98b5f30bfe3a829d276c435c9beef71cf8a2f7de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910661"
---
# <span data-ttu-id="e31a0-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e31a0-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="e31a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e31a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e31a0-103">從 Azure 認知搜尋服務移除私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="e31a0-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e31a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="e31a0-104">SYNTAX</span></span>

### <span data-ttu-id="e31a0-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e31a0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e31a0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31a0-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e31a0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31a0-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e31a0-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e31a0-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e31a0-109">描述</span><span class="sxs-lookup"><span data-stu-id="e31a0-109">DESCRIPTION</span></span>
<span data-ttu-id="e31a0-110">**Remove-AzSearchPrivateEndpointConnection** 會從 Azure 認知搜尋服務移除私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="e31a0-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e31a0-111">例子</span><span class="sxs-lookup"><span data-stu-id="e31a0-111">EXAMPLES</span></span>

### <span data-ttu-id="e31a0-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="e31a0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="e31a0-113">此範例會根據名稱從搜尋服務移除私人端點連接。</span><span class="sxs-lookup"><span data-stu-id="e31a0-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="e31a0-114">參數</span><span class="sxs-lookup"><span data-stu-id="e31a0-114">PARAMETERS</span></span>

### <span data-ttu-id="e31a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31a0-115">-DefaultProfile</span></span>
<span data-ttu-id="e31a0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e31a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e31a0-117">-強制</span><span class="sxs-lookup"><span data-stu-id="e31a0-117">-Force</span></span>
<span data-ttu-id="e31a0-118">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="e31a0-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e31a0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e31a0-119">-InputObject</span></span>
<span data-ttu-id="e31a0-120">私人端點連接輸入物件</span><span class="sxs-lookup"><span data-stu-id="e31a0-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e31a0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e31a0-121">-Name</span></span>
<span data-ttu-id="e31a0-122">Azure 認知搜尋服務私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="e31a0-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="e31a0-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e31a0-123">-ParentObject</span></span>
<span data-ttu-id="e31a0-124">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="e31a0-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="e31a0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e31a0-125">-PassThru</span></span>
<span data-ttu-id="e31a0-126">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="e31a0-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e31a0-127">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="e31a0-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e31a0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31a0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e31a0-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e31a0-129">Resource Group name.</span></span>

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

### <span data-ttu-id="e31a0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e31a0-130">-ResourceId</span></span>
<span data-ttu-id="e31a0-131">私人連結服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e31a0-131">Private link service resource id</span></span>

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

### <span data-ttu-id="e31a0-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e31a0-132">-ServiceName</span></span>
<span data-ttu-id="e31a0-133">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="e31a0-133">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="e31a0-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e31a0-134">-Confirm</span></span>
<span data-ttu-id="e31a0-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e31a0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e31a0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e31a0-136">-WhatIf</span></span>
<span data-ttu-id="e31a0-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e31a0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e31a0-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e31a0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e31a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31a0-139">CommonParameters</span></span>
<span data-ttu-id="e31a0-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e31a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31a0-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e31a0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31a0-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e31a0-142">INPUTS</span></span>

### <span data-ttu-id="e31a0-143">沒有</span><span class="sxs-lookup"><span data-stu-id="e31a0-143">None</span></span>

## <span data-ttu-id="e31a0-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e31a0-144">OUTPUTS</span></span>

### <span data-ttu-id="e31a0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e31a0-145">System.Boolean</span></span>

## <span data-ttu-id="e31a0-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e31a0-146">NOTES</span></span>

## <span data-ttu-id="e31a0-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="e31a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="e31a0-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="e31a0-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="e31a0-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="e31a0-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)