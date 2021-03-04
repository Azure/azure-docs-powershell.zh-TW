---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: 1001aa2f282ab59e6ddc9e3e1ecc654950d8e30e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902165"
---
# <span data-ttu-id="622c6-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="622c6-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="622c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="622c6-102">SYNOPSIS</span></span>
<span data-ttu-id="622c6-103">在工作區中建立或更新資料集。</span><span class="sxs-lookup"><span data-stu-id="622c6-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="622c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="622c6-104">SYNTAX</span></span>

### <span data-ttu-id="622c6-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="622c6-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="622c6-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="622c6-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="622c6-107">描述</span><span class="sxs-lookup"><span data-stu-id="622c6-107">DESCRIPTION</span></span>
<span data-ttu-id="622c6-108">**Set-AzSynapseDataset** Cmdlet 會建立資料集或更新工作區中現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="622c6-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="622c6-109">例子</span><span class="sxs-lookup"><span data-stu-id="622c6-109">EXAMPLES</span></span>

### <span data-ttu-id="622c6-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="622c6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="622c6-111">此命令在名為 ContosoWorkspace 的工作區中建立名為 ContosoDataset 的資料集。</span><span class="sxs-lookup"><span data-stu-id="622c6-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="622c6-112">命令以檔案中資料Dataset.js基礎。</span><span class="sxs-lookup"><span data-stu-id="622c6-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="622c6-113">參數</span><span class="sxs-lookup"><span data-stu-id="622c6-113">PARAMETERS</span></span>

### <span data-ttu-id="622c6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="622c6-114">-AsJob</span></span>
<span data-ttu-id="622c6-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="622c6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="622c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622c6-116">-DefaultProfile</span></span>
<span data-ttu-id="622c6-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="622c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="622c6-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="622c6-118">-DefinitionFile</span></span>
<span data-ttu-id="622c6-119">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="622c6-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c6-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="622c6-120">-Name</span></span>
<span data-ttu-id="622c6-121">資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="622c6-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c6-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="622c6-122">-WorkspaceName</span></span>
<span data-ttu-id="622c6-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="622c6-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="622c6-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="622c6-124">-WorkspaceObject</span></span>
<span data-ttu-id="622c6-125">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="622c6-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="622c6-126">-確認</span><span class="sxs-lookup"><span data-stu-id="622c6-126">-Confirm</span></span>
<span data-ttu-id="622c6-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="622c6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="622c6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="622c6-128">-WhatIf</span></span>
<span data-ttu-id="622c6-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="622c6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="622c6-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="622c6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="622c6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622c6-131">CommonParameters</span></span>
<span data-ttu-id="622c6-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="622c6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622c6-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="622c6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622c6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="622c6-134">INPUTS</span></span>

### <span data-ttu-id="622c6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="622c6-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="622c6-136">輸出</span><span class="sxs-lookup"><span data-stu-id="622c6-136">OUTPUTS</span></span>

### <span data-ttu-id="622c6-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="622c6-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="622c6-138">筆記</span><span class="sxs-lookup"><span data-stu-id="622c6-138">NOTES</span></span>

## <span data-ttu-id="622c6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="622c6-139">RELATED LINKS</span></span>
