---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 158d4a54cdbeec0dd8cf756a3c685aede97f5bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912978"
---
# <span data-ttu-id="2c110-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="2c110-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="2c110-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c110-102">SYNOPSIS</span></span>
<span data-ttu-id="2c110-103">獲得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="2c110-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="2c110-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c110-104">SYNTAX</span></span>

### <span data-ttu-id="2c110-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2c110-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c110-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c110-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c110-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c110-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c110-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c110-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c110-109">描述</span><span class="sxs-lookup"><span data-stu-id="2c110-109">DESCRIPTION</span></span>
<span data-ttu-id="2c110-110">**Get-AzSynapse RuntimeRuntimeMetric** Cmdlet 會取得工作區中整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="2c110-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="2c110-111">例子</span><span class="sxs-lookup"><span data-stu-id="2c110-111">EXAMPLES</span></span>

### <span data-ttu-id="2c110-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c110-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="2c110-113">此命令會在名為 ContosoWorkspace 的工作區中顯示名為"test-selfhost-ir"的整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="2c110-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2c110-114">參數</span><span class="sxs-lookup"><span data-stu-id="2c110-114">PARAMETERS</span></span>

### <span data-ttu-id="2c110-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c110-115">-DefaultProfile</span></span>
<span data-ttu-id="2c110-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c110-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c110-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c110-117">-InputObject</span></span>
<span data-ttu-id="2c110-118">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="2c110-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="2c110-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c110-119">-Name</span></span>
<span data-ttu-id="2c110-120">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="2c110-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="2c110-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c110-121">-ResourceGroupName</span></span>
<span data-ttu-id="2c110-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2c110-122">Resource group name.</span></span>

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

### <span data-ttu-id="2c110-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c110-123">-ResourceId</span></span>
<span data-ttu-id="2c110-124">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c110-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="2c110-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c110-125">-WorkspaceName</span></span>
<span data-ttu-id="2c110-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c110-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2c110-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2c110-127">-WorkspaceObject</span></span>
<span data-ttu-id="2c110-128">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="2c110-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2c110-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c110-129">CommonParameters</span></span>
<span data-ttu-id="2c110-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c110-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c110-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c110-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c110-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2c110-132">INPUTS</span></span>

### <span data-ttu-id="2c110-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c110-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2c110-134">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="2c110-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2c110-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2c110-135">OUTPUTS</span></span>

### <span data-ttu-id="2c110-136">Microsoft.Azure.Commands.Synapse.models.PSMetricRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="2c110-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="2c110-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2c110-137">NOTES</span></span>

## <span data-ttu-id="2c110-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c110-138">RELATED LINKS</span></span>
