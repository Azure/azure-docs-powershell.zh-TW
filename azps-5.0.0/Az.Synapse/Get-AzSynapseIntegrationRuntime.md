---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139410"
---
# <span data-ttu-id="9d35b-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9d35b-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="9d35b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d35b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d35b-103">取得有關整合執行時間資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="9d35b-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="9d35b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d35b-104">SYNTAX</span></span>

### <span data-ttu-id="9d35b-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9d35b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d35b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d35b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d35b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d35b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d35b-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d35b-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d35b-109">說明</span><span class="sxs-lookup"><span data-stu-id="9d35b-109">DESCRIPTION</span></span>
<span data-ttu-id="9d35b-110">**AzSynapseIntegrationRuntime** Cmdlet 會取得有關工作區中集成執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d35b-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="9d35b-111">如果您指定整合執行時間的名稱，此 Cmdlet 會取得該整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d35b-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="9d35b-112">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有整合執行時間的資訊。</span><span class="sxs-lookup"><span data-stu-id="9d35b-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="9d35b-113">示例</span><span class="sxs-lookup"><span data-stu-id="9d35b-113">EXAMPLES</span></span>

### <span data-ttu-id="9d35b-114">範例1</span><span class="sxs-lookup"><span data-stu-id="9d35b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="9d35b-115">在名為 ContosoWorkspace 的工作區中列出所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="9d35b-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9d35b-116">範例2</span><span class="sxs-lookup"><span data-stu-id="9d35b-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="9d35b-117">這個命令會在名為 ContosoWorkspace 的工作區中，顯示名為「test-selfhost-ir」的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d35b-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="9d35b-118">範例3</span><span class="sxs-lookup"><span data-stu-id="9d35b-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="9d35b-119">這個命令會在名為 ContosoWorkspace 的工作區中，顯示名為「test-selfhost-ir」之整合執行時間的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="9d35b-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="9d35b-120">參數</span><span class="sxs-lookup"><span data-stu-id="9d35b-120">PARAMETERS</span></span>

### <span data-ttu-id="9d35b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d35b-121">-DefaultProfile</span></span>
<span data-ttu-id="9d35b-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d35b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d35b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d35b-123">-InputObject</span></span>
<span data-ttu-id="9d35b-124">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="9d35b-124">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d35b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d35b-125">-Name</span></span>
<span data-ttu-id="9d35b-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="9d35b-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d35b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d35b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d35b-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9d35b-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d35b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d35b-129">-ResourceId</span></span>
<span data-ttu-id="9d35b-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d35b-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d35b-131">-狀態</span><span class="sxs-lookup"><span data-stu-id="9d35b-131">-Status</span></span>
<span data-ttu-id="9d35b-132">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="9d35b-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="9d35b-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9d35b-133">-WorkspaceName</span></span>
<span data-ttu-id="9d35b-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d35b-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d35b-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9d35b-135">-WorkspaceObject</span></span>
<span data-ttu-id="9d35b-136">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="9d35b-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d35b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d35b-137">CommonParameters</span></span>
<span data-ttu-id="9d35b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d35b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d35b-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9d35b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d35b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="9d35b-140">INPUTS</span></span>

### <span data-ttu-id="9d35b-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9d35b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9d35b-142">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9d35b-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9d35b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="9d35b-143">OUTPUTS</span></span>

### <span data-ttu-id="9d35b-144">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="9d35b-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9d35b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="9d35b-145">NOTES</span></span>

## <span data-ttu-id="9d35b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d35b-146">RELATED LINKS</span></span>