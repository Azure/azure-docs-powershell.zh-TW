---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141200"
---
# <span data-ttu-id="725cb-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="725cb-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="725cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="725cb-102">SYNOPSIS</span></span>
<span data-ttu-id="725cb-103">建立或更新工作區中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="725cb-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="725cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="725cb-104">SYNTAX</span></span>

### <span data-ttu-id="725cb-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="725cb-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="725cb-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="725cb-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="725cb-107">說明</span><span class="sxs-lookup"><span data-stu-id="725cb-107">DESCRIPTION</span></span>
<span data-ttu-id="725cb-108">**AzSynapseDataFlow** Cmdlet 會建立資料流程程或更新工作區中現有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="725cb-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="725cb-109">示例</span><span class="sxs-lookup"><span data-stu-id="725cb-109">EXAMPLES</span></span>

### <span data-ttu-id="725cb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="725cb-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="725cb-111">這個命令會在名為 [ContosoWorkspace] 的工作區中建立名為 ContosoDataFlow 的資料流程。</span><span class="sxs-lookup"><span data-stu-id="725cb-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="725cb-112">此命令會根據檔案中 DataFlow.js的資訊來控制資料流程。</span><span class="sxs-lookup"><span data-stu-id="725cb-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="725cb-113">參數</span><span class="sxs-lookup"><span data-stu-id="725cb-113">PARAMETERS</span></span>

### <span data-ttu-id="725cb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="725cb-114">-AsJob</span></span>
<span data-ttu-id="725cb-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="725cb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="725cb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725cb-116">-DefaultProfile</span></span>
<span data-ttu-id="725cb-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="725cb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="725cb-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="725cb-118">-DefinitionFile</span></span>
<span data-ttu-id="725cb-119">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="725cb-119">The JSON file path.</span></span>

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

### <span data-ttu-id="725cb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="725cb-120">-Name</span></span>
<span data-ttu-id="725cb-121">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="725cb-121">The data flow name.</span></span>

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

### <span data-ttu-id="725cb-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="725cb-122">-WorkspaceName</span></span>
<span data-ttu-id="725cb-123">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="725cb-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="725cb-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="725cb-124">-WorkspaceObject</span></span>
<span data-ttu-id="725cb-125">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="725cb-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="725cb-126">-確認</span><span class="sxs-lookup"><span data-stu-id="725cb-126">-Confirm</span></span>
<span data-ttu-id="725cb-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="725cb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="725cb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="725cb-128">-WhatIf</span></span>
<span data-ttu-id="725cb-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="725cb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="725cb-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="725cb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="725cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725cb-131">CommonParameters</span></span>
<span data-ttu-id="725cb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="725cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725cb-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="725cb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725cb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="725cb-134">INPUTS</span></span>

### <span data-ttu-id="725cb-135">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="725cb-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="725cb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="725cb-136">OUTPUTS</span></span>

### <span data-ttu-id="725cb-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="725cb-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="725cb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="725cb-138">NOTES</span></span>

## <span data-ttu-id="725cb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="725cb-139">RELATED LINKS</span></span>
