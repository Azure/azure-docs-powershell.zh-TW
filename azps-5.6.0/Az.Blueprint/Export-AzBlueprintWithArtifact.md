---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 1e4184b847b260d84d8b3609ade5403367046dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917778"
---
# <span data-ttu-id="b1de4-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b1de4-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b1de4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1de4-102">SYNOPSIS</span></span>
<span data-ttu-id="b1de4-103">將指定的藍圖定義匯出至指定的輸出位置作為 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="b1de4-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="b1de4-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1de4-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1de4-105">描述</span><span class="sxs-lookup"><span data-stu-id="b1de4-105">DESCRIPTION</span></span>
<span data-ttu-id="b1de4-106">將藍圖定義及其加工品匯出並儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="b1de4-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="b1de4-107">此 Cmdlet 會匯出藍圖 (或已發佈) 最新版本。</span><span class="sxs-lookup"><span data-stu-id="b1de4-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="b1de4-108">例子</span><span class="sxs-lookup"><span data-stu-id="b1de4-108">EXAMPLES</span></span>

### <span data-ttu-id="b1de4-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="b1de4-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="b1de4-110">將藍圖定義及其加工品匯出並儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="b1de4-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="b1de4-111">參數</span><span class="sxs-lookup"><span data-stu-id="b1de4-111">PARAMETERS</span></span>

### <span data-ttu-id="b1de4-112">-藍圖</span><span class="sxs-lookup"><span data-stu-id="b1de4-112">-Blueprint</span></span>
<span data-ttu-id="b1de4-113">要匯出的藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="b1de4-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1de4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1de4-114">-DefaultProfile</span></span>
<span data-ttu-id="b1de4-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1de4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1de4-116">-強制</span><span class="sxs-lookup"><span data-stu-id="b1de4-116">-Force</span></span>
<span data-ttu-id="b1de4-117">當設定為 True 時，執行不會要求確認。</span><span class="sxs-lookup"><span data-stu-id="b1de4-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b1de4-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b1de4-118">-OutputPath</span></span>
<span data-ttu-id="b1de4-119">磁片中要匯出 JSON 格式藍圖定義之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1de4-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="b1de4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1de4-120">-PassThru</span></span>
<span data-ttu-id="b1de4-121">設定之後，Cmdlet 會返回代表匯出藍圖定義的物件。</span><span class="sxs-lookup"><span data-stu-id="b1de4-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="b1de4-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b1de4-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1de4-123">-版本</span><span class="sxs-lookup"><span data-stu-id="b1de4-123">-Version</span></span>
<span data-ttu-id="b1de4-124">已發佈的藍圖定義版本。</span><span class="sxs-lookup"><span data-stu-id="b1de4-124">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1de4-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b1de4-125">-Confirm</span></span>
<span data-ttu-id="b1de4-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1de4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1de4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1de4-127">-WhatIf</span></span>
<span data-ttu-id="b1de4-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1de4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1de4-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1de4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1de4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1de4-130">CommonParameters</span></span>
<span data-ttu-id="b1de4-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1de4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1de4-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1de4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1de4-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b1de4-133">INPUTS</span></span>

### <span data-ttu-id="b1de4-134">Microsoft.Azure.Commands.藍圖.models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b1de4-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b1de4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b1de4-135">System.String</span></span>

## <span data-ttu-id="b1de4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b1de4-136">OUTPUTS</span></span>

### <span data-ttu-id="b1de4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b1de4-137">System.String</span></span>

## <span data-ttu-id="b1de4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b1de4-138">NOTES</span></span>

## <span data-ttu-id="b1de4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1de4-139">RELATED LINKS</span></span>
