---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141270"
---
# <span data-ttu-id="2443e-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2443e-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="2443e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2443e-102">SYNOPSIS</span></span>
<span data-ttu-id="2443e-103">移除範本規格</span><span class="sxs-lookup"><span data-stu-id="2443e-103">Removes a Template Spec</span></span>

## <span data-ttu-id="2443e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2443e-104">SYNTAX</span></span>

### <span data-ttu-id="2443e-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2443e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2443e-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2443e-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2443e-107">說明</span><span class="sxs-lookup"><span data-stu-id="2443e-107">DESCRIPTION</span></span>
<span data-ttu-id="2443e-108">移除指定的範本規格。如果 **提供 version 版本參數，** 則只會移除指定的版本。</span><span class="sxs-lookup"><span data-stu-id="2443e-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="2443e-109">如果未提供特定版本，則會移除範本規格及其所有版本。</span><span class="sxs-lookup"><span data-stu-id="2443e-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="2443e-110">如果有 **-Force** 標誌存在，就不會提示您要移除的資訊。</span><span class="sxs-lookup"><span data-stu-id="2443e-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="2443e-111">示例</span><span class="sxs-lookup"><span data-stu-id="2443e-111">EXAMPLES</span></span>

### <span data-ttu-id="2443e-112">範例1：依名稱移除特定版本</span><span class="sxs-lookup"><span data-stu-id="2443e-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="2443e-113">移除資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格版本 ' v 1.0」。</span><span class="sxs-lookup"><span data-stu-id="2443e-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="2443e-114">範例2：依資源識別碼移除特定版本</span><span class="sxs-lookup"><span data-stu-id="2443e-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="2443e-115">移除訂閱 subId 之資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格的版本 ' v 1.0 \{ 」 \} 。</span><span class="sxs-lookup"><span data-stu-id="2443e-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="2443e-116">範例3：依名稱移除範本規格與所有版本</span><span class="sxs-lookup"><span data-stu-id="2443e-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="2443e-117">移除名為「MyTemplateSpec」的範本規格，以及其在資源群組 ' myRG」中的所有版本。</span><span class="sxs-lookup"><span data-stu-id="2443e-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="2443e-118">範例3：依資源識別碼移除範本規格與所有版本</span><span class="sxs-lookup"><span data-stu-id="2443e-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="2443e-119">移除 [訂閱 subId] 資源群組 "myRG" 中名為「MyTemplateSpec」及其所有版本的 Template 規格 \{ \} 。</span><span class="sxs-lookup"><span data-stu-id="2443e-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="2443e-120">參數</span><span class="sxs-lookup"><span data-stu-id="2443e-120">PARAMETERS</span></span>

### <span data-ttu-id="2443e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2443e-121">-DefaultProfile</span></span>
<span data-ttu-id="2443e-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2443e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2443e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2443e-123">-Force</span></span>
<span data-ttu-id="2443e-124">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="2443e-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2443e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2443e-125">-Name</span></span>
<span data-ttu-id="2443e-126">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="2443e-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="2443e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2443e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2443e-128">範本規格之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2443e-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="2443e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2443e-129">-ResourceId</span></span>
<span data-ttu-id="2443e-130">範本規格的完全限定資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="2443e-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="2443e-131">-版本</span><span class="sxs-lookup"><span data-stu-id="2443e-131">-Version</span></span>
<span data-ttu-id="2443e-132">要刪除的範本規格版本。</span><span class="sxs-lookup"><span data-stu-id="2443e-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="2443e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="2443e-133">-Confirm</span></span>
<span data-ttu-id="2443e-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2443e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2443e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2443e-135">-WhatIf</span></span>
<span data-ttu-id="2443e-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2443e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2443e-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2443e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2443e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2443e-138">CommonParameters</span></span>
<span data-ttu-id="2443e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2443e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2443e-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2443e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2443e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="2443e-141">INPUTS</span></span>

### <span data-ttu-id="2443e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="2443e-142">System.String</span></span>

## <span data-ttu-id="2443e-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2443e-143">OUTPUTS</span></span>

### <span data-ttu-id="2443e-144">System.object</span><span class="sxs-lookup"><span data-stu-id="2443e-144">System.Boolean</span></span>

## <span data-ttu-id="2443e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2443e-145">NOTES</span></span>

## <span data-ttu-id="2443e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2443e-146">RELATED LINKS</span></span>
