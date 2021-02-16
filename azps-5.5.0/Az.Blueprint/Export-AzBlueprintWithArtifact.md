---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127959"
---
# <span data-ttu-id="da8d6-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="da8d6-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="da8d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="da8d6-103">將指定的藍圖定義匯出到指定的輸出位置做為 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="da8d6-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="da8d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="da8d6-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da8d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="da8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="da8d6-106">匯出藍圖定義及其工件，並儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="da8d6-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="da8d6-107">這個 Cmdlet 會匯出藍圖 (草稿或發行) 的最新版本。</span><span class="sxs-lookup"><span data-stu-id="da8d6-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="da8d6-108">示例</span><span class="sxs-lookup"><span data-stu-id="da8d6-108">EXAMPLES</span></span>

### <span data-ttu-id="da8d6-109">範例1</span><span class="sxs-lookup"><span data-stu-id="da8d6-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="da8d6-110">匯出藍圖定義及其工件，並儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="da8d6-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="da8d6-111">參數</span><span class="sxs-lookup"><span data-stu-id="da8d6-111">PARAMETERS</span></span>

### <span data-ttu-id="da8d6-112">-藍圖</span><span class="sxs-lookup"><span data-stu-id="da8d6-112">-Blueprint</span></span>
<span data-ttu-id="da8d6-113">要匯出的藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="da8d6-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="da8d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da8d6-114">-DefaultProfile</span></span>
<span data-ttu-id="da8d6-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="da8d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da8d6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="da8d6-116">-Force</span></span>
<span data-ttu-id="da8d6-117">當設定為 true 時，執行將不要求確認。</span><span class="sxs-lookup"><span data-stu-id="da8d6-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="da8d6-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="da8d6-118">-OutputPath</span></span>
<span data-ttu-id="da8d6-119">磁片上檔案的路徑，該檔案中的檔案會以 JSON 格式匯出藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="da8d6-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="da8d6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da8d6-120">-PassThru</span></span>
<span data-ttu-id="da8d6-121">設定之後，Cmdlet 會傳回代表已匯出藍圖定義的物件。</span><span class="sxs-lookup"><span data-stu-id="da8d6-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="da8d6-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="da8d6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da8d6-123">-版本</span><span class="sxs-lookup"><span data-stu-id="da8d6-123">-Version</span></span>
<span data-ttu-id="da8d6-124">已發佈藍圖定義版本。</span><span class="sxs-lookup"><span data-stu-id="da8d6-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="da8d6-125">-確認</span><span class="sxs-lookup"><span data-stu-id="da8d6-125">-Confirm</span></span>
<span data-ttu-id="da8d6-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da8d6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da8d6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da8d6-127">-WhatIf</span></span>
<span data-ttu-id="da8d6-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da8d6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da8d6-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da8d6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da8d6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8d6-130">CommonParameters</span></span>
<span data-ttu-id="da8d6-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da8d6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8d6-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="da8d6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8d6-133">輸入</span><span class="sxs-lookup"><span data-stu-id="da8d6-133">INPUTS</span></span>

### <span data-ttu-id="da8d6-134">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="da8d6-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="da8d6-135">System.object</span><span class="sxs-lookup"><span data-stu-id="da8d6-135">System.String</span></span>

## <span data-ttu-id="da8d6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="da8d6-136">OUTPUTS</span></span>

### <span data-ttu-id="da8d6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="da8d6-137">System.String</span></span>

## <span data-ttu-id="da8d6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="da8d6-138">NOTES</span></span>

## <span data-ttu-id="da8d6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="da8d6-139">RELATED LINKS</span></span>
