---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912977"
---
# <span data-ttu-id="a2285-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a2285-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a2285-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2285-102">SYNOPSIS</span></span>
<span data-ttu-id="a2285-103">獲得整合執行時間節點資訊。</span><span class="sxs-lookup"><span data-stu-id="a2285-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="a2285-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2285-104">SYNTAX</span></span>

### <span data-ttu-id="a2285-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2285-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2285-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2285-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2285-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2285-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2285-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2285-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2285-109">描述</span><span class="sxs-lookup"><span data-stu-id="a2285-109">DESCRIPTION</span></span>
<span data-ttu-id="a2285-110">**Get-AzSynapse RuntimeRuntimeNode** Cmdlet 會取得整合執行時間節點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a2285-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="a2285-111">例子</span><span class="sxs-lookup"><span data-stu-id="a2285-111">EXAMPLES</span></span>

### <span data-ttu-id="a2285-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a2285-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="a2285-113">Cmdlet 會從工作區 ContosoWorkspace 的自行託管整合執行時間 "test-selfhost-ir" 中，獲得名為 "Node_1" 的節點資訊。</span><span class="sxs-lookup"><span data-stu-id="a2285-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a2285-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="a2285-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="a2285-115">Cmdlet 會獲得工作區'test-df-eu2'中自我託管整合執行時間'test-selfhost-ir'中名為 "Node_1" 的節點資訊，包括 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a2285-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="a2285-116">參數</span><span class="sxs-lookup"><span data-stu-id="a2285-116">PARAMETERS</span></span>

### <span data-ttu-id="a2285-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2285-117">-DefaultProfile</span></span>
<span data-ttu-id="a2285-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2285-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2285-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2285-119">-InputObject</span></span>
<span data-ttu-id="a2285-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="a2285-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="a2285-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a2285-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a2285-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="a2285-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2285-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a2285-123">-IpAddress</span></span>
<span data-ttu-id="a2285-124">整合執行時間節點的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a2285-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="a2285-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2285-125">-Name</span></span>
<span data-ttu-id="a2285-126">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="a2285-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2285-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2285-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2285-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a2285-128">Resource group name.</span></span>

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

### <span data-ttu-id="a2285-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2285-129">-ResourceId</span></span>
<span data-ttu-id="a2285-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2285-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="a2285-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a2285-131">-WorkspaceName</span></span>
<span data-ttu-id="a2285-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2285-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2285-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2285-133">-WorkspaceObject</span></span>
<span data-ttu-id="a2285-134">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="a2285-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2285-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2285-135">CommonParameters</span></span>
<span data-ttu-id="a2285-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2285-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2285-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2285-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2285-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a2285-138">INPUTS</span></span>

### <span data-ttu-id="a2285-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2285-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a2285-140">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="a2285-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a2285-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a2285-141">OUTPUTS</span></span>

### <span data-ttu-id="a2285-142">Microsoft.Azure.Commands.Synapse.Models.PSManaged方格RuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a2285-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="a2285-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHosted方格RuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a2285-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a2285-144">筆記</span><span class="sxs-lookup"><span data-stu-id="a2285-144">NOTES</span></span>

## <span data-ttu-id="a2285-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2285-145">RELATED LINKS</span></span>
