---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 341edce877666d56a78064f1e13dc7b7af9b26a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141822"
---
# <span data-ttu-id="a0ffc-101">Remove-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a0ffc-101">Remove-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="a0ffc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ffc-103">從 Azure 認知搜尋服務移除專用端點連線。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-103">Remove the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a0ffc-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0ffc-104">SYNTAX</span></span>

### <span data-ttu-id="a0ffc-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a0ffc-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ffc-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ffc-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ffc-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ffc-107">InputObjectParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection -InputObject <PSPrivateEndpointConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ffc-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0ffc-108">ResourceIdParameterSet</span></span>
```
Remove-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0ffc-109">說明</span><span class="sxs-lookup"><span data-stu-id="a0ffc-109">DESCRIPTION</span></span>
<span data-ttu-id="a0ffc-110">[ **移除-AzSearchPrivateEndpointConnection** ] 會從 Azure 認知搜尋服務移除專用端點連線。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-110">The **Remove-AzSearchPrivateEndpointConnection** removes the private endpoint connection from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a0ffc-111">示例</span><span class="sxs-lookup"><span data-stu-id="a0ffc-111">EXAMPLES</span></span>

### <span data-ttu-id="a0ffc-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a0ffc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="a0ffc-113">這個範例會依名稱從搜尋服務移除私人端點連線。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-113">This example removes a private endpoint connection from the search service by name.</span></span>

## <span data-ttu-id="a0ffc-114">參數</span><span class="sxs-lookup"><span data-stu-id="a0ffc-114">PARAMETERS</span></span>

### <span data-ttu-id="a0ffc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ffc-115">-DefaultProfile</span></span>
<span data-ttu-id="a0ffc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ffc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a0ffc-117">-Force</span></span>
<span data-ttu-id="a0ffc-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0ffc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0ffc-119">-InputObject</span></span>
<span data-ttu-id="a0ffc-120">私人端點連接輸入物件</span><span class="sxs-lookup"><span data-stu-id="a0ffc-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="a0ffc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0ffc-121">-Name</span></span>
<span data-ttu-id="a0ffc-122">Azure 認知搜尋服務私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="a0ffc-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="a0ffc-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a0ffc-123">-ParentObject</span></span>
<span data-ttu-id="a0ffc-124">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="a0ffc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0ffc-125">-PassThru</span></span>
<span data-ttu-id="a0ffc-126">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a0ffc-127">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a0ffc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ffc-128">-ResourceGroupName</span></span>
<span data-ttu-id="a0ffc-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-129">Resource Group name.</span></span>

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

### <span data-ttu-id="a0ffc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ffc-130">-ResourceId</span></span>
<span data-ttu-id="a0ffc-131">私人連結服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a0ffc-131">Private link service resource id</span></span>

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

### <span data-ttu-id="a0ffc-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a0ffc-132">-ServiceName</span></span>
<span data-ttu-id="a0ffc-133">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-133">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="a0ffc-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a0ffc-134">-Confirm</span></span>
<span data-ttu-id="a0ffc-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ffc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ffc-136">-WhatIf</span></span>
<span data-ttu-id="a0ffc-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0ffc-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ffc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ffc-139">CommonParameters</span></span>
<span data-ttu-id="a0ffc-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ffc-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0ffc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ffc-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a0ffc-142">INPUTS</span></span>

### <span data-ttu-id="a0ffc-143">所有</span><span class="sxs-lookup"><span data-stu-id="a0ffc-143">None</span></span>

## <span data-ttu-id="a0ffc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a0ffc-144">OUTPUTS</span></span>

### <span data-ttu-id="a0ffc-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a0ffc-145">System.Boolean</span></span>

## <span data-ttu-id="a0ffc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a0ffc-146">NOTES</span></span>

## <span data-ttu-id="a0ffc-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0ffc-147">RELATED LINKS</span></span>

[<span data-ttu-id="a0ffc-148">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="a0ffc-148">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="a0ffc-149">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="a0ffc-149">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)