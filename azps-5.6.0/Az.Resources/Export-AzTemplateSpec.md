---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: eb6311dacd05f539cf508657e52637524ea98ea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907542"
---
# <span data-ttu-id="eb5ce-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="eb5ce-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="eb5ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eb5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5ce-103">將範本規格匯出至本地檔案系統</span><span class="sxs-lookup"><span data-stu-id="eb5ce-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="eb5ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="eb5ce-104">SYNTAX</span></span>

### <span data-ttu-id="eb5ce-105">ExportByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eb5ce-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb5ce-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb5ce-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb5ce-107">描述</span><span class="sxs-lookup"><span data-stu-id="eb5ce-107">DESCRIPTION</span></span>
<span data-ttu-id="eb5ce-108">將特定的範本規格版本匯出至本地檔案系統。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="eb5ce-109">例子</span><span class="sxs-lookup"><span data-stu-id="eb5ce-109">EXAMPLES</span></span>

### <span data-ttu-id="eb5ce-110">範例 1：按名稱匯出</span><span class="sxs-lookup"><span data-stu-id="eb5ce-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="eb5ce-111">將資源群組 「myRG」中名為「MyTemplateSpec」的範本規格「v1.0」匯出至本地輸出檔案夾「v1」。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="eb5ce-112">範例 2：根據資源識別碼匯出</span><span class="sxs-lookup"><span data-stu-id="eb5ce-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="eb5ce-113">將訂閱子Id 資源群組「myRG」中名為「MyTemplateSpec」的範本規格「v1.0」匯出至本地 \{ \} 輸出檔案夾「v1」。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="eb5ce-114">參數</span><span class="sxs-lookup"><span data-stu-id="eb5ce-114">PARAMETERS</span></span>

### <span data-ttu-id="eb5ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ce-115">-DefaultProfile</span></span>
<span data-ttu-id="eb5ce-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb5ce-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb5ce-117">-Name</span></span>
<span data-ttu-id="eb5ce-118">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ce-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="eb5ce-119">-OutputFolder</span></span>
<span data-ttu-id="eb5ce-120">將輸出範本規格版本的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-120">The path to the folder where the template spec version will be output to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb5ce-122">範本規格資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ce-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb5ce-123">-ResourceId</span></span>
<span data-ttu-id="eb5ce-124">範本規格的完全合格的資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="eb5ce-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ce-125">-版本</span><span class="sxs-lookup"><span data-stu-id="eb5ce-125">-Version</span></span>
<span data-ttu-id="eb5ce-126">要匯出的範本規格版本。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-126">The version of the template spec to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb5ce-127">-確認</span><span class="sxs-lookup"><span data-stu-id="eb5ce-127">-Confirm</span></span>
<span data-ttu-id="eb5ce-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb5ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5ce-129">-WhatIf</span></span>
<span data-ttu-id="eb5ce-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb5ce-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb5ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5ce-132">CommonParameters</span></span>
<span data-ttu-id="eb5ce-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eb5ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5ce-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb5ce-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5ce-135">輸入</span><span class="sxs-lookup"><span data-stu-id="eb5ce-135">INPUTS</span></span>

### <span data-ttu-id="eb5ce-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eb5ce-136">System.String</span></span>

## <span data-ttu-id="eb5ce-137">輸出</span><span class="sxs-lookup"><span data-stu-id="eb5ce-137">OUTPUTS</span></span>

### <span data-ttu-id="eb5ce-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="eb5ce-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eb5ce-139">筆記</span><span class="sxs-lookup"><span data-stu-id="eb5ce-139">NOTES</span></span>

## <span data-ttu-id="eb5ce-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb5ce-140">RELATED LINKS</span></span>
