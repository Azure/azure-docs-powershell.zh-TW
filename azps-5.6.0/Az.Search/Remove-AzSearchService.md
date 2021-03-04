---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 0e1011fb8e2aaec7a77f735c961fa6ec2ede9dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916369"
---
# <span data-ttu-id="8ab76-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8ab76-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="8ab76-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ab76-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab76-103">移除 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="8ab76-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8ab76-104">語法</span><span class="sxs-lookup"><span data-stu-id="8ab76-104">SYNTAX</span></span>

### <span data-ttu-id="8ab76-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8ab76-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab76-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ab76-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ab76-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ab76-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab76-108">描述</span><span class="sxs-lookup"><span data-stu-id="8ab76-108">DESCRIPTION</span></span>
<span data-ttu-id="8ab76-109">**Remove-AzSearchService** Cmdlet 會移除具有指定參數的 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="8ab76-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="8ab76-110">例子</span><span class="sxs-lookup"><span data-stu-id="8ab76-110">EXAMPLES</span></span>

### <span data-ttu-id="8ab76-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8ab76-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="8ab76-112">此範例會移除 Azure 認知搜尋服務。</span><span class="sxs-lookup"><span data-stu-id="8ab76-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="8ab76-113">參數</span><span class="sxs-lookup"><span data-stu-id="8ab76-113">PARAMETERS</span></span>

### <span data-ttu-id="8ab76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab76-114">-DefaultProfile</span></span>
<span data-ttu-id="8ab76-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ab76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ab76-116">-強制</span><span class="sxs-lookup"><span data-stu-id="8ab76-116">-Force</span></span>
<span data-ttu-id="8ab76-117">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="8ab76-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8ab76-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ab76-118">-InputObject</span></span>
<span data-ttu-id="8ab76-119">Azure 認知搜尋服務輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8ab76-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab76-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ab76-120">-Name</span></span>
<span data-ttu-id="8ab76-121">Azure 認知搜尋服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8ab76-121">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="8ab76-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ab76-122">-PassThru</span></span>
<span data-ttu-id="8ab76-123">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="8ab76-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8ab76-124">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="8ab76-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8ab76-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab76-125">-ResourceGroupName</span></span>
<span data-ttu-id="8ab76-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="8ab76-126">Resource Group name.</span></span>

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

### <span data-ttu-id="8ab76-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ab76-127">-ResourceId</span></span>
<span data-ttu-id="8ab76-128">Azure 認知搜尋服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ab76-128">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab76-129">-確認</span><span class="sxs-lookup"><span data-stu-id="8ab76-129">-Confirm</span></span>
<span data-ttu-id="8ab76-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8ab76-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ab76-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab76-131">-WhatIf</span></span>
<span data-ttu-id="8ab76-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ab76-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab76-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ab76-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ab76-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab76-134">CommonParameters</span></span>
<span data-ttu-id="8ab76-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ab76-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab76-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ab76-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab76-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8ab76-137">INPUTS</span></span>

### <span data-ttu-id="8ab76-138">Microsoft.Azure.Commands.management.Search.models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8ab76-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8ab76-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8ab76-139">System.String</span></span>

## <span data-ttu-id="8ab76-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8ab76-140">OUTPUTS</span></span>

### <span data-ttu-id="8ab76-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ab76-141">System.Boolean</span></span>

## <span data-ttu-id="8ab76-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8ab76-142">NOTES</span></span>

## <span data-ttu-id="8ab76-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ab76-143">RELATED LINKS</span></span>

[<span data-ttu-id="8ab76-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8ab76-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="8ab76-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8ab76-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="8ab76-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="8ab76-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
