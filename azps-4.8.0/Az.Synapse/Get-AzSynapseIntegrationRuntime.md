---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 285c0877441cabf51c723a472208cc002867fa7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129718"
---
# <span data-ttu-id="02804-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="02804-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="02804-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02804-102">SYNOPSIS</span></span>
<span data-ttu-id="02804-103">取得有關整合執行時間資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="02804-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="02804-104">句法</span><span class="sxs-lookup"><span data-stu-id="02804-104">SYNTAX</span></span>

### <span data-ttu-id="02804-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="02804-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02804-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02804-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02804-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02804-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02804-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02804-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02804-109">說明</span><span class="sxs-lookup"><span data-stu-id="02804-109">DESCRIPTION</span></span>
<span data-ttu-id="02804-110">**AzSynapseIntegrationRuntime** Cmdlet 會取得有關工作區中集成執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="02804-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="02804-111">如果您指定整合執行時間的名稱，此 Cmdlet 會取得該整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="02804-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="02804-112">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有整合執行時間的資訊。</span><span class="sxs-lookup"><span data-stu-id="02804-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="02804-113">示例</span><span class="sxs-lookup"><span data-stu-id="02804-113">EXAMPLES</span></span>

### <span data-ttu-id="02804-114">範例1</span><span class="sxs-lookup"><span data-stu-id="02804-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="02804-115">在名為 ContosoWorkspace 的工作區中列出所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="02804-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="02804-116">範例2</span><span class="sxs-lookup"><span data-stu-id="02804-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="02804-117">這個命令會在名為 ContosoWorkspace 的工作區中，顯示名為「test-selfhost-ir」的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="02804-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="02804-118">範例3</span><span class="sxs-lookup"><span data-stu-id="02804-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="02804-119">這個命令會在名為 ContosoWorkspace 的工作區中，顯示名為「test-selfhost-ir」之整合執行時間的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="02804-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="02804-120">參數</span><span class="sxs-lookup"><span data-stu-id="02804-120">PARAMETERS</span></span>

### <span data-ttu-id="02804-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02804-121">-DefaultProfile</span></span>
<span data-ttu-id="02804-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02804-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02804-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02804-123">-InputObject</span></span>
<span data-ttu-id="02804-124">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="02804-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="02804-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="02804-125">-Name</span></span>
<span data-ttu-id="02804-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="02804-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="02804-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02804-127">-ResourceGroupName</span></span>
<span data-ttu-id="02804-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="02804-128">Resource group name.</span></span>

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

### <span data-ttu-id="02804-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02804-129">-ResourceId</span></span>
<span data-ttu-id="02804-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="02804-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="02804-131">-狀態</span><span class="sxs-lookup"><span data-stu-id="02804-131">-Status</span></span>
<span data-ttu-id="02804-132">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="02804-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="02804-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02804-133">-WorkspaceName</span></span>
<span data-ttu-id="02804-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="02804-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="02804-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="02804-135">-WorkspaceObject</span></span>
<span data-ttu-id="02804-136">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="02804-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="02804-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02804-137">CommonParameters</span></span>
<span data-ttu-id="02804-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02804-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02804-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="02804-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02804-140">輸入</span><span class="sxs-lookup"><span data-stu-id="02804-140">INPUTS</span></span>

### <span data-ttu-id="02804-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="02804-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="02804-142">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="02804-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="02804-143">輸出</span><span class="sxs-lookup"><span data-stu-id="02804-143">OUTPUTS</span></span>

### <span data-ttu-id="02804-144">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="02804-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="02804-145">筆記</span><span class="sxs-lookup"><span data-stu-id="02804-145">NOTES</span></span>

## <span data-ttu-id="02804-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="02804-146">RELATED LINKS</span></span>
