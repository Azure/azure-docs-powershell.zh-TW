---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 0fa0069686a34fbd1ee60d31df96386a5d7959d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909385"
---
# <span data-ttu-id="58d87-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="58d87-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="58d87-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58d87-102">SYNOPSIS</span></span>
<span data-ttu-id="58d87-103">在工作區中獲取資料流程相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58d87-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="58d87-104">語法</span><span class="sxs-lookup"><span data-stu-id="58d87-104">SYNTAX</span></span>

### <span data-ttu-id="58d87-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="58d87-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58d87-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="58d87-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58d87-107">描述</span><span class="sxs-lookup"><span data-stu-id="58d87-107">DESCRIPTION</span></span>
<span data-ttu-id="58d87-108">**Get-AzSynapseDataFlow** Cmdlet 會取得工作區中資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="58d87-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="58d87-109">如果您指定資料流程的名稱，此 Cmdlet 會獲得該資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="58d87-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="58d87-110">如果您未指定名稱，此 Cmdlet 會獲得工作區中所有資料流量的資訊。</span><span class="sxs-lookup"><span data-stu-id="58d87-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="58d87-111">例子</span><span class="sxs-lookup"><span data-stu-id="58d87-111">EXAMPLES</span></span>

### <span data-ttu-id="58d87-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="58d87-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="58d87-113">此命令會獲得名為 ContosoWorkspace 工作區中所有資料流程程的資訊。</span><span class="sxs-lookup"><span data-stu-id="58d87-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="58d87-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="58d87-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="58d87-115">此命令會從名為 ContosoWorkspace 的工作區中，獲得名為 ContosoDataFlow 的資料流程相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58d87-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="58d87-116">參數</span><span class="sxs-lookup"><span data-stu-id="58d87-116">PARAMETERS</span></span>

### <span data-ttu-id="58d87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d87-117">-DefaultProfile</span></span>
<span data-ttu-id="58d87-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58d87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58d87-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="58d87-119">-Name</span></span>
<span data-ttu-id="58d87-120">資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="58d87-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d87-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="58d87-121">-WorkspaceName</span></span>
<span data-ttu-id="58d87-122">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="58d87-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d87-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="58d87-123">-WorkspaceObject</span></span>
<span data-ttu-id="58d87-124">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="58d87-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d87-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d87-125">CommonParameters</span></span>
<span data-ttu-id="58d87-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58d87-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d87-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58d87-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d87-128">輸入</span><span class="sxs-lookup"><span data-stu-id="58d87-128">INPUTS</span></span>

### <span data-ttu-id="58d87-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="58d87-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="58d87-130">輸出</span><span class="sxs-lookup"><span data-stu-id="58d87-130">OUTPUTS</span></span>

### <span data-ttu-id="58d87-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="58d87-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="58d87-132">筆記</span><span class="sxs-lookup"><span data-stu-id="58d87-132">NOTES</span></span>

## <span data-ttu-id="58d87-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="58d87-133">RELATED LINKS</span></span>
