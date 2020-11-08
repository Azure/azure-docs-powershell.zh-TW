---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137947"
---
# <span data-ttu-id="59e27-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="59e27-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="59e27-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59e27-102">SYNOPSIS</span></span>
<span data-ttu-id="59e27-103">取得有關工作區中資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="59e27-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="59e27-104">句法</span><span class="sxs-lookup"><span data-stu-id="59e27-104">SYNTAX</span></span>

### <span data-ttu-id="59e27-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="59e27-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59e27-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="59e27-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e27-107">說明</span><span class="sxs-lookup"><span data-stu-id="59e27-107">DESCRIPTION</span></span>
<span data-ttu-id="59e27-108">**AzSynapseDataFlow** Cmdlet 會取得有關工作區中資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="59e27-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="59e27-109">如果您指定資料流程程的名稱，此 Cmdlet 會取得該資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="59e27-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="59e27-110">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有資料流程的資訊。</span><span class="sxs-lookup"><span data-stu-id="59e27-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="59e27-111">示例</span><span class="sxs-lookup"><span data-stu-id="59e27-111">EXAMPLES</span></span>

### <span data-ttu-id="59e27-112">範例1</span><span class="sxs-lookup"><span data-stu-id="59e27-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="59e27-113">這個命令會取得名為 ContosoWorkspace 的工作區中所有資料資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="59e27-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="59e27-114">範例2</span><span class="sxs-lookup"><span data-stu-id="59e27-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="59e27-115">這個命令會在名為 ContosoWorkspace 的工作區中，取得名為 ContosoDataFlow 的資料流程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="59e27-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="59e27-116">參數</span><span class="sxs-lookup"><span data-stu-id="59e27-116">PARAMETERS</span></span>

### <span data-ttu-id="59e27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e27-117">-DefaultProfile</span></span>
<span data-ttu-id="59e27-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59e27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59e27-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="59e27-119">-Name</span></span>
<span data-ttu-id="59e27-120">資料流程程名稱。</span><span class="sxs-lookup"><span data-stu-id="59e27-120">The data flow name.</span></span>

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

### <span data-ttu-id="59e27-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="59e27-121">-WorkspaceName</span></span>
<span data-ttu-id="59e27-122">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="59e27-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="59e27-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="59e27-123">-WorkspaceObject</span></span>
<span data-ttu-id="59e27-124">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="59e27-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="59e27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e27-125">CommonParameters</span></span>
<span data-ttu-id="59e27-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59e27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e27-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="59e27-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e27-128">輸入</span><span class="sxs-lookup"><span data-stu-id="59e27-128">INPUTS</span></span>

### <span data-ttu-id="59e27-129">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="59e27-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="59e27-130">輸出</span><span class="sxs-lookup"><span data-stu-id="59e27-130">OUTPUTS</span></span>

### <span data-ttu-id="59e27-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="59e27-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="59e27-132">筆記</span><span class="sxs-lookup"><span data-stu-id="59e27-132">NOTES</span></span>

## <span data-ttu-id="59e27-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="59e27-133">RELATED LINKS</span></span>