---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 168a19c6e3900b395841aabbc19359d9fa4858f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909374"
---
# <span data-ttu-id="f002f-101">Get-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f002f-101">Get-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="f002f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f002f-102">SYNOPSIS</span></span>
<span data-ttu-id="f002f-103">獲得整合執行時間資源相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f002f-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="f002f-104">語法</span><span class="sxs-lookup"><span data-stu-id="f002f-104">SYNTAX</span></span>

### <span data-ttu-id="f002f-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f002f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f002f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f002f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime [-Name <String>] -WorkspaceObject <PSSynapseWorkspace> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f002f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f002f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -ResourceId <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f002f-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f002f-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f002f-109">描述</span><span class="sxs-lookup"><span data-stu-id="f002f-109">DESCRIPTION</span></span>
<span data-ttu-id="f002f-110">**Get-AzSynapse WorkspaceRuntime** Cmdlet 會取得工作區中整合執行時間的資訊。</span><span class="sxs-lookup"><span data-stu-id="f002f-110">The **Get-AzSynapseIntegrationRuntime** cmdlet gets information about integration runtimes in a workspace.</span></span>
<span data-ttu-id="f002f-111">如果您指定整合執行時間的名稱，此 Cmdlet 會獲得該整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f002f-111">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="f002f-112">如果您未指定名稱，此 Cmdlet 會獲得工作區中所有整合執行時間的資訊。</span><span class="sxs-lookup"><span data-stu-id="f002f-112">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a workspace.</span></span>

## <span data-ttu-id="f002f-113">例子</span><span class="sxs-lookup"><span data-stu-id="f002f-113">EXAMPLES</span></span>

### <span data-ttu-id="f002f-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="f002f-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f002f-115">在名為 ContosoWorkspace 的工作區中列出所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="f002f-115">List all integration runtimes in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f002f-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="f002f-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="f002f-117">此命令會在名為 ContosoWorkspace 的工作區中顯示名為"test-selfhost-ir"的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f002f-117">This command displays information about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f002f-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="f002f-118">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Status
```

<span data-ttu-id="f002f-119">此命令會在名為 ContosoWorkspace 的工作區中顯示名為"test-selfhost-ir"之整合執行時間的詳細狀態。</span><span class="sxs-lookup"><span data-stu-id="f002f-119">This command displays detail status about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f002f-120">參數</span><span class="sxs-lookup"><span data-stu-id="f002f-120">PARAMETERS</span></span>

### <span data-ttu-id="f002f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f002f-121">-DefaultProfile</span></span>
<span data-ttu-id="f002f-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f002f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f002f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f002f-123">-InputObject</span></span>
<span data-ttu-id="f002f-124">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="f002f-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="f002f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f002f-125">-Name</span></span>
<span data-ttu-id="f002f-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="f002f-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="f002f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f002f-127">-ResourceGroupName</span></span>
<span data-ttu-id="f002f-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f002f-128">Resource group name.</span></span>

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

### <span data-ttu-id="f002f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f002f-129">-ResourceId</span></span>
<span data-ttu-id="f002f-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f002f-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="f002f-131">-狀態</span><span class="sxs-lookup"><span data-stu-id="f002f-131">-Status</span></span>
<span data-ttu-id="f002f-132">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="f002f-132">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="f002f-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f002f-133">-WorkspaceName</span></span>
<span data-ttu-id="f002f-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f002f-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f002f-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f002f-135">-WorkspaceObject</span></span>
<span data-ttu-id="f002f-136">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="f002f-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f002f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f002f-137">CommonParameters</span></span>
<span data-ttu-id="f002f-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f002f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f002f-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f002f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f002f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f002f-140">INPUTS</span></span>

### <span data-ttu-id="f002f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f002f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f002f-142">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="f002f-142">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f002f-143">輸出</span><span class="sxs-lookup"><span data-stu-id="f002f-143">OUTPUTS</span></span>

### <span data-ttu-id="f002f-144">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="f002f-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f002f-145">筆記</span><span class="sxs-lookup"><span data-stu-id="f002f-145">NOTES</span></span>

## <span data-ttu-id="f002f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f002f-146">RELATED LINKS</span></span>
