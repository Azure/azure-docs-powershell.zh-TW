---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902166"
---
# <span data-ttu-id="3a895-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="3a895-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="3a895-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a895-102">SYNOPSIS</span></span>
<span data-ttu-id="3a895-103">在工作區中建立或更新資料流程。</span><span class="sxs-lookup"><span data-stu-id="3a895-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="3a895-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a895-104">SYNTAX</span></span>

### <span data-ttu-id="3a895-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3a895-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a895-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="3a895-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a895-107">描述</span><span class="sxs-lookup"><span data-stu-id="3a895-107">DESCRIPTION</span></span>
<span data-ttu-id="3a895-108">**Set-AzSynapseDataFlow** Cmdlet 會建立資料流程或更新工作區中現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3a895-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="3a895-109">例子</span><span class="sxs-lookup"><span data-stu-id="3a895-109">EXAMPLES</span></span>

### <span data-ttu-id="3a895-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3a895-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="3a895-111">此命令在名為 ContosoWorkspace 的工作區中建立名為 ContosoDataFlow 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3a895-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="3a895-112">命令以檔案中資料DataFlow.js的基礎。</span><span class="sxs-lookup"><span data-stu-id="3a895-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="3a895-113">參數</span><span class="sxs-lookup"><span data-stu-id="3a895-113">PARAMETERS</span></span>

### <span data-ttu-id="3a895-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a895-114">-AsJob</span></span>
<span data-ttu-id="3a895-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3a895-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a895-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a895-116">-DefaultProfile</span></span>
<span data-ttu-id="3a895-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a895-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a895-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3a895-118">-DefinitionFile</span></span>
<span data-ttu-id="3a895-119">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3a895-119">The JSON file path.</span></span>

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

### <span data-ttu-id="3a895-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a895-120">-Name</span></span>
<span data-ttu-id="3a895-121">資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="3a895-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a895-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a895-122">-WorkspaceName</span></span>
<span data-ttu-id="3a895-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a895-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a895-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a895-124">-WorkspaceObject</span></span>
<span data-ttu-id="3a895-125">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="3a895-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a895-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3a895-126">-Confirm</span></span>
<span data-ttu-id="3a895-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3a895-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a895-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a895-128">-WhatIf</span></span>
<span data-ttu-id="3a895-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a895-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a895-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a895-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a895-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a895-131">CommonParameters</span></span>
<span data-ttu-id="3a895-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a895-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a895-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a895-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a895-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3a895-134">INPUTS</span></span>

### <span data-ttu-id="3a895-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a895-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3a895-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3a895-136">OUTPUTS</span></span>

### <span data-ttu-id="3a895-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="3a895-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="3a895-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3a895-138">NOTES</span></span>

## <span data-ttu-id="3a895-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a895-139">RELATED LINKS</span></span>
