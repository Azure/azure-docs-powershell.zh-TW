---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613594"
---
# <span data-ttu-id="a3149-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a3149-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="a3149-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3149-102">SYNOPSIS</span></span>
<span data-ttu-id="a3149-103">將指定的藍圖定義匯出到指定的輸出位置做為 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="a3149-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="a3149-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3149-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3149-105">說明</span><span class="sxs-lookup"><span data-stu-id="a3149-105">DESCRIPTION</span></span>
<span data-ttu-id="a3149-106">匯出藍圖定義及其工件，並儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="a3149-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="a3149-107">這個 Cmdlet 會匯出藍圖 (草稿或發行) 的最新版本。</span><span class="sxs-lookup"><span data-stu-id="a3149-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="a3149-108">示例</span><span class="sxs-lookup"><span data-stu-id="a3149-108">EXAMPLES</span></span>

### <span data-ttu-id="a3149-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a3149-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="a3149-110">匯出藍圖定義及其工件，並儲存到磁片。</span><span class="sxs-lookup"><span data-stu-id="a3149-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="a3149-111">參數</span><span class="sxs-lookup"><span data-stu-id="a3149-111">PARAMETERS</span></span>

### <span data-ttu-id="a3149-112">-藍圖</span><span class="sxs-lookup"><span data-stu-id="a3149-112">-Blueprint</span></span>
<span data-ttu-id="a3149-113">要匯出的藍圖定義物件。</span><span class="sxs-lookup"><span data-stu-id="a3149-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3149-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3149-114">-DefaultProfile</span></span>
<span data-ttu-id="a3149-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3149-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3149-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a3149-116">-Force</span></span>
<span data-ttu-id="a3149-117">當設定為 true 時，執行將不要求確認。</span><span class="sxs-lookup"><span data-stu-id="a3149-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3149-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a3149-118">-OutputPath</span></span>
<span data-ttu-id="a3149-119">磁片上檔案的路徑，該檔案中的檔案會以 JSON 格式匯出藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="a3149-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3149-120">-版本</span><span class="sxs-lookup"><span data-stu-id="a3149-120">-Version</span></span>
<span data-ttu-id="a3149-121">已發佈藍圖定義版本。</span><span class="sxs-lookup"><span data-stu-id="a3149-121">Published blueprint definition version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3149-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3149-122">CommonParameters</span></span>
<span data-ttu-id="a3149-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3149-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a3149-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3149-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3149-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a3149-125">INPUTS</span></span>

### <span data-ttu-id="a3149-126">PSBlueprintBase 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a3149-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a3149-127">System.object</span><span class="sxs-lookup"><span data-stu-id="a3149-127">System.String</span></span>

## <span data-ttu-id="a3149-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a3149-128">OUTPUTS</span></span>

### <span data-ttu-id="a3149-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a3149-129">System.String</span></span>

## <span data-ttu-id="a3149-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a3149-130">NOTES</span></span>

## <span data-ttu-id="a3149-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3149-131">RELATED LINKS</span></span>
