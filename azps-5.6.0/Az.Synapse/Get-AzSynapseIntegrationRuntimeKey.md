---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: d00e4c137e3b46e7721534264c9273cde5a9ad3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906830"
---
# <span data-ttu-id="6c2fb-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="6c2fb-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="6c2fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6c2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2fb-103">獲得自我託管整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="6c2fb-104">語法</span><span class="sxs-lookup"><span data-stu-id="6c2fb-104">SYNTAX</span></span>

### <span data-ttu-id="6c2fb-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c2fb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c2fb-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c2fb-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c2fb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c2fb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c2fb-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c2fb-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c2fb-109">描述</span><span class="sxs-lookup"><span data-stu-id="6c2fb-109">DESCRIPTION</span></span>
<span data-ttu-id="6c2fb-110">**Get-AzSynapse RuntimeRuntimeKey** Cmdlet 會取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="6c2fb-111">這些金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="6c2fb-112">例子</span><span class="sxs-lookup"><span data-stu-id="6c2fb-112">EXAMPLES</span></span>

### <span data-ttu-id="6c2fb-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="6c2fb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="6c2fb-114">Cmdlet 會針對名為"test-selfhost-ir"的整合執行時間來取金鑰。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6c2fb-115">參數</span><span class="sxs-lookup"><span data-stu-id="6c2fb-115">PARAMETERS</span></span>

### <span data-ttu-id="6c2fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2fb-116">-DefaultProfile</span></span>
<span data-ttu-id="6c2fb-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2fb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c2fb-118">-InputObject</span></span>
<span data-ttu-id="6c2fb-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="6c2fb-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c2fb-120">-Name</span></span>
<span data-ttu-id="6c2fb-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="6c2fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c2fb-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-123">Resource group name.</span></span>

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

### <span data-ttu-id="6c2fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c2fb-124">-ResourceId</span></span>
<span data-ttu-id="6c2fb-125">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="6c2fb-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6c2fb-126">-WorkspaceName</span></span>
<span data-ttu-id="6c2fb-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6c2fb-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6c2fb-128">-WorkspaceObject</span></span>
<span data-ttu-id="6c2fb-129">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6c2fb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2fb-130">CommonParameters</span></span>
<span data-ttu-id="6c2fb-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6c2fb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2fb-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c2fb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2fb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6c2fb-133">INPUTS</span></span>

### <span data-ttu-id="6c2fb-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6c2fb-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6c2fb-135">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="6c2fb-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6c2fb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6c2fb-136">OUTPUTS</span></span>

### <span data-ttu-id="6c2fb-137">Microsoft.Azure.Commands.Synapse.Models.PS方格RuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="6c2fb-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="6c2fb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6c2fb-138">NOTES</span></span>

## <span data-ttu-id="6c2fb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c2fb-139">RELATED LINKS</span></span>
