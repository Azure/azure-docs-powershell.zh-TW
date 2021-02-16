---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128474"
---
# <span data-ttu-id="c56cd-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="c56cd-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="c56cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c56cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c56cd-103">匯出範本規格至本機 filesystem</span><span class="sxs-lookup"><span data-stu-id="c56cd-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="c56cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="c56cd-104">SYNTAX</span></span>

### <span data-ttu-id="c56cd-105">ExportByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c56cd-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56cd-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c56cd-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56cd-107">說明</span><span class="sxs-lookup"><span data-stu-id="c56cd-107">DESCRIPTION</span></span>
<span data-ttu-id="c56cd-108">將特定的範本規格版本匯出到本機 filesystem。</span><span class="sxs-lookup"><span data-stu-id="c56cd-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="c56cd-109">示例</span><span class="sxs-lookup"><span data-stu-id="c56cd-109">EXAMPLES</span></span>

### <span data-ttu-id="c56cd-110">範例1：依名稱匯出</span><span class="sxs-lookup"><span data-stu-id="c56cd-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="c56cd-111">將資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格的版本 ' v 1.0」匯出到本機輸出檔案夾 "v1"。</span><span class="sxs-lookup"><span data-stu-id="c56cd-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="c56cd-112">範例2：依資源識別碼匯出</span><span class="sxs-lookup"><span data-stu-id="c56cd-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="c56cd-113">將 [訂閱 subId] 資源群組 "myRG" 中名為 "MyTemplateSpec" 的範本規格的版本 ' v 1.0」匯出 \{ \} 到本機輸出檔案夾 "v1"。</span><span class="sxs-lookup"><span data-stu-id="c56cd-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="c56cd-114">參數</span><span class="sxs-lookup"><span data-stu-id="c56cd-114">PARAMETERS</span></span>

### <span data-ttu-id="c56cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56cd-115">-DefaultProfile</span></span>
<span data-ttu-id="c56cd-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c56cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c56cd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c56cd-117">-Name</span></span>
<span data-ttu-id="c56cd-118">範本規格的名稱。</span><span class="sxs-lookup"><span data-stu-id="c56cd-118">The name of the template spec.</span></span>

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

### <span data-ttu-id="c56cd-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c56cd-119">-OutputFolder</span></span>
<span data-ttu-id="c56cd-120">要將範本規格版本輸出至其中的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="c56cd-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="c56cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="c56cd-122">範本規格之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c56cd-122">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="c56cd-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c56cd-123">-ResourceId</span></span>
<span data-ttu-id="c56cd-124">範本規格的完全限定資源識別碼。範例：/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="c56cd-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="c56cd-125">-版本</span><span class="sxs-lookup"><span data-stu-id="c56cd-125">-Version</span></span>
<span data-ttu-id="c56cd-126">要匯出的範本規格版本。</span><span class="sxs-lookup"><span data-stu-id="c56cd-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="c56cd-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c56cd-127">-Confirm</span></span>
<span data-ttu-id="c56cd-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c56cd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56cd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56cd-129">-WhatIf</span></span>
<span data-ttu-id="c56cd-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c56cd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c56cd-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c56cd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56cd-132">CommonParameters</span></span>
<span data-ttu-id="c56cd-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c56cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56cd-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c56cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56cd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c56cd-135">INPUTS</span></span>

### <span data-ttu-id="c56cd-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c56cd-136">System.String</span></span>

## <span data-ttu-id="c56cd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c56cd-137">OUTPUTS</span></span>

### <span data-ttu-id="c56cd-138">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="c56cd-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c56cd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c56cd-139">NOTES</span></span>

## <span data-ttu-id="c56cd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c56cd-140">RELATED LINKS</span></span>
