---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141193"
---
# <span data-ttu-id="e2722-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="e2722-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="e2722-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2722-102">SYNOPSIS</span></span>
<span data-ttu-id="e2722-103">在工作區中建立或更新資料集。</span><span class="sxs-lookup"><span data-stu-id="e2722-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="e2722-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2722-104">SYNTAX</span></span>

### <span data-ttu-id="e2722-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e2722-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2722-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="e2722-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2722-107">說明</span><span class="sxs-lookup"><span data-stu-id="e2722-107">DESCRIPTION</span></span>
<span data-ttu-id="e2722-108">**AzSynapseDataset** Cmdlet 會建立資料集或更新工作區中現有的資料集。</span><span class="sxs-lookup"><span data-stu-id="e2722-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="e2722-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2722-109">EXAMPLES</span></span>

### <span data-ttu-id="e2722-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e2722-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="e2722-111">這個命令會在名為 [ContosoWorkspace] 的工作區中建立名為 ContosoDataset 的資料集。</span><span class="sxs-lookup"><span data-stu-id="e2722-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="e2722-112">此命令根據檔案中 Dataset.js的資訊來基礎。</span><span class="sxs-lookup"><span data-stu-id="e2722-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="e2722-113">參數</span><span class="sxs-lookup"><span data-stu-id="e2722-113">PARAMETERS</span></span>

### <span data-ttu-id="e2722-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2722-114">-AsJob</span></span>
<span data-ttu-id="e2722-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2722-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2722-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2722-116">-DefaultProfile</span></span>
<span data-ttu-id="e2722-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2722-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2722-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e2722-118">-DefinitionFile</span></span>
<span data-ttu-id="e2722-119">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="e2722-119">The JSON file path.</span></span>

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

### <span data-ttu-id="e2722-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2722-120">-Name</span></span>
<span data-ttu-id="e2722-121">資料集名稱。</span><span class="sxs-lookup"><span data-stu-id="e2722-121">The dataset name.</span></span>

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

### <span data-ttu-id="e2722-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e2722-122">-WorkspaceName</span></span>
<span data-ttu-id="e2722-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2722-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e2722-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e2722-124">-WorkspaceObject</span></span>
<span data-ttu-id="e2722-125">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="e2722-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e2722-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e2722-126">-Confirm</span></span>
<span data-ttu-id="e2722-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e2722-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2722-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2722-128">-WhatIf</span></span>
<span data-ttu-id="e2722-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e2722-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2722-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2722-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2722-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2722-131">CommonParameters</span></span>
<span data-ttu-id="e2722-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2722-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2722-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e2722-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2722-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e2722-134">INPUTS</span></span>

### <span data-ttu-id="e2722-135">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="e2722-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e2722-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e2722-136">OUTPUTS</span></span>

### <span data-ttu-id="e2722-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="e2722-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="e2722-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e2722-138">NOTES</span></span>

## <span data-ttu-id="e2722-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2722-139">RELATED LINKS</span></span>