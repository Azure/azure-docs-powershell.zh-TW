---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 6383a1fb0a6dbaa20bee50a268d8f78abf59de65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908774"
---
# <span data-ttu-id="6ffe9-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="6ffe9-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="6ffe9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ffe9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffe9-103">移除範本規格</span><span class="sxs-lookup"><span data-stu-id="6ffe9-103">Removes a Template Spec</span></span>

## <span data-ttu-id="6ffe9-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ffe9-104">SYNTAX</span></span>

### <span data-ttu-id="6ffe9-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6ffe9-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffe9-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffe9-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffe9-107">描述</span><span class="sxs-lookup"><span data-stu-id="6ffe9-107">DESCRIPTION</span></span>
<span data-ttu-id="6ffe9-108">移除指定的範本規格。如果提供版本 **-版本** 參數，則只會移除指定的版本。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="6ffe9-109">如果沒有提供特定版本，將會移除範本規格及其所有版本。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="6ffe9-110">如果 **-Force** 旗標存在，則沒有移除的確認提示。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="6ffe9-111">例子</span><span class="sxs-lookup"><span data-stu-id="6ffe9-111">EXAMPLES</span></span>

### <span data-ttu-id="6ffe9-112">範例 1：移除特定版本的名稱</span><span class="sxs-lookup"><span data-stu-id="6ffe9-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="6ffe9-113">移除資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格版本 'v1.0'。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="6ffe9-114">範例 2：根據資源識別碼移除特定版本</span><span class="sxs-lookup"><span data-stu-id="6ffe9-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="6ffe9-115">移除訂閱子Id 之資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格 'v1.0'。 \{ \}</span><span class="sxs-lookup"><span data-stu-id="6ffe9-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="6ffe9-116">範例 3：移除範本規格及所有版本的名稱</span><span class="sxs-lookup"><span data-stu-id="6ffe9-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="6ffe9-117">移除名為 "MyTemplateSpec" 的範本規格，以及資源群組 "myRG" 內的所有版本。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="6ffe9-118">範例 3：移除範本規格，以及根據資源識別碼移除所有版本</span><span class="sxs-lookup"><span data-stu-id="6ffe9-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="6ffe9-119">移除名為 "MyTemplateSpec" 的範本規格及其訂閱子Id 資源群組 "myRG" \{ 內的所有版本 \} 。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="6ffe9-120">參數</span><span class="sxs-lookup"><span data-stu-id="6ffe9-120">PARAMETERS</span></span>

### <span data-ttu-id="6ffe9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffe9-121">-DefaultProfile</span></span>
<span data-ttu-id="6ffe9-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffe9-123">-強制</span><span class="sxs-lookup"><span data-stu-id="6ffe9-123">-Force</span></span>
<span data-ttu-id="6ffe9-124">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6ffe9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ffe9-125">-Name</span></span>
<span data-ttu-id="6ffe9-126">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffe9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffe9-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ffe9-128">範本規格資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffe9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffe9-129">-ResourceId</span></span>
<span data-ttu-id="6ffe9-130">範本規格的完全合格的資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="6ffe9-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffe9-131">-版本</span><span class="sxs-lookup"><span data-stu-id="6ffe9-131">-Version</span></span>
<span data-ttu-id="6ffe9-132">要刪除的範本規格版本。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="6ffe9-133">-確認</span><span class="sxs-lookup"><span data-stu-id="6ffe9-133">-Confirm</span></span>
<span data-ttu-id="6ffe9-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffe9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffe9-135">-WhatIf</span></span>
<span data-ttu-id="6ffe9-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ffe9-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffe9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffe9-138">CommonParameters</span></span>
<span data-ttu-id="6ffe9-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ffe9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffe9-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ffe9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffe9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6ffe9-141">INPUTS</span></span>

### <span data-ttu-id="6ffe9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6ffe9-142">System.String</span></span>

## <span data-ttu-id="6ffe9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6ffe9-143">OUTPUTS</span></span>

### <span data-ttu-id="6ffe9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ffe9-144">System.Boolean</span></span>

## <span data-ttu-id="6ffe9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6ffe9-145">NOTES</span></span>

## <span data-ttu-id="6ffe9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ffe9-146">RELATED LINKS</span></span>
