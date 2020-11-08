---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971579"
---
# <span data-ttu-id="b48ad-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b48ad-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b48ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b48ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b48ad-103">取得整合執行時間節點資訊。</span><span class="sxs-lookup"><span data-stu-id="b48ad-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="b48ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="b48ad-104">SYNTAX</span></span>

### <span data-ttu-id="b48ad-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b48ad-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b48ad-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b48ad-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b48ad-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b48ad-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b48ad-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b48ad-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b48ad-109">說明</span><span class="sxs-lookup"><span data-stu-id="b48ad-109">DESCRIPTION</span></span>
<span data-ttu-id="b48ad-110">**AzSynapseIntegrationRuntimeNode** Cmdlet 會取得整合執行時間節點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b48ad-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="b48ad-111">示例</span><span class="sxs-lookup"><span data-stu-id="b48ad-111">EXAMPLES</span></span>

### <span data-ttu-id="b48ad-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b48ad-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="b48ad-113">此 Cmdlet 會取得在工作區 ContosoWorkspace 中，在自行託管整合執行時間 "selfhost-ir" 中名為「Node_1 ' 的節點資訊。</span><span class="sxs-lookup"><span data-stu-id="b48ad-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b48ad-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b48ad-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="b48ad-115">此 Cmdlet 會取得在工作區「test-eu2」中，在自託管整合執行時間 "test-selfhost-ir" 中名為「Node_1」的節點資訊，包括 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b48ad-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="b48ad-116">參數</span><span class="sxs-lookup"><span data-stu-id="b48ad-116">PARAMETERS</span></span>

### <span data-ttu-id="b48ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48ad-117">-DefaultProfile</span></span>
<span data-ttu-id="b48ad-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b48ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b48ad-119">-InputObject</span></span>
<span data-ttu-id="b48ad-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="b48ad-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="b48ad-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b48ad-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b48ad-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b48ad-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="b48ad-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="b48ad-123">-IpAddress</span></span>
<span data-ttu-id="b48ad-124">整合執行時間節點的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b48ad-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="b48ad-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b48ad-125">-Name</span></span>
<span data-ttu-id="b48ad-126">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="b48ad-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b48ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="b48ad-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b48ad-128">Resource group name.</span></span>

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

### <span data-ttu-id="b48ad-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b48ad-129">-ResourceId</span></span>
<span data-ttu-id="b48ad-130">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b48ad-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b48ad-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b48ad-131">-WorkspaceName</span></span>
<span data-ttu-id="b48ad-132">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48ad-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b48ad-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b48ad-133">-WorkspaceObject</span></span>
<span data-ttu-id="b48ad-134">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="b48ad-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b48ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48ad-135">CommonParameters</span></span>
<span data-ttu-id="b48ad-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b48ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48ad-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b48ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48ad-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b48ad-138">INPUTS</span></span>

### <span data-ttu-id="b48ad-139">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b48ad-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b48ad-140">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b48ad-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b48ad-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b48ad-141">OUTPUTS</span></span>

### <span data-ttu-id="b48ad-142">PSManagedIntegrationRuntimeNode 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b48ad-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="b48ad-143">PSSelfHostedIntegrationRuntimeNode 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b48ad-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b48ad-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b48ad-144">NOTES</span></span>

## <span data-ttu-id="b48ad-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b48ad-145">RELATED LINKS</span></span>
