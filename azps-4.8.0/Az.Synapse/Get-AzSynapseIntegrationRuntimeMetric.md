---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129108"
---
# <span data-ttu-id="b8a58-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="b8a58-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="b8a58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8a58-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a58-103">取得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="b8a58-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="b8a58-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8a58-104">SYNTAX</span></span>

### <span data-ttu-id="b8a58-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b8a58-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a58-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a58-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8a58-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a58-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8a58-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a58-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a58-109">說明</span><span class="sxs-lookup"><span data-stu-id="b8a58-109">DESCRIPTION</span></span>
<span data-ttu-id="b8a58-110">**AzSynapseIntegrationRuntimeMetric** Cmdlet 會取得有關工作區中集成執行時間的度量資料。</span><span class="sxs-lookup"><span data-stu-id="b8a58-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="b8a58-111">示例</span><span class="sxs-lookup"><span data-stu-id="b8a58-111">EXAMPLES</span></span>

### <span data-ttu-id="b8a58-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b8a58-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="b8a58-113">這個命令會在名為 ContosoWorkspace 的工作區中，顯示名為「test-selfhost-ir」之整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="b8a58-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b8a58-114">參數</span><span class="sxs-lookup"><span data-stu-id="b8a58-114">PARAMETERS</span></span>

### <span data-ttu-id="b8a58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a58-115">-DefaultProfile</span></span>
<span data-ttu-id="b8a58-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8a58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a58-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8a58-117">-InputObject</span></span>
<span data-ttu-id="b8a58-118">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="b8a58-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="b8a58-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8a58-119">-Name</span></span>
<span data-ttu-id="b8a58-120">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a58-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a58-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a58-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8a58-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a58-122">Resource group name.</span></span>

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

### <span data-ttu-id="b8a58-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8a58-123">-ResourceId</span></span>
<span data-ttu-id="b8a58-124">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8a58-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="b8a58-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b8a58-125">-WorkspaceName</span></span>
<span data-ttu-id="b8a58-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a58-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b8a58-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b8a58-127">-WorkspaceObject</span></span>
<span data-ttu-id="b8a58-128">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="b8a58-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b8a58-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a58-129">CommonParameters</span></span>
<span data-ttu-id="b8a58-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8a58-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a58-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b8a58-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a58-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b8a58-132">INPUTS</span></span>

### <span data-ttu-id="b8a58-133">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b8a58-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b8a58-134">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b8a58-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b8a58-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b8a58-135">OUTPUTS</span></span>

### <span data-ttu-id="b8a58-136">PSIntegrationRuntimeMetrics 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b8a58-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="b8a58-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b8a58-137">NOTES</span></span>

## <span data-ttu-id="b8a58-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8a58-138">RELATED LINKS</span></span>
