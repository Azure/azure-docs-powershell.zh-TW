---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968937"
---
# <span data-ttu-id="286d1-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="286d1-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="286d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="286d1-102">SYNOPSIS</span></span>
<span data-ttu-id="286d1-103">取得自託管整合執行時間的鍵。</span><span class="sxs-lookup"><span data-stu-id="286d1-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="286d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="286d1-104">SYNTAX</span></span>

### <span data-ttu-id="286d1-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="286d1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="286d1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286d1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="286d1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="286d1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="286d1-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="286d1-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="286d1-109">說明</span><span class="sxs-lookup"><span data-stu-id="286d1-109">DESCRIPTION</span></span>
<span data-ttu-id="286d1-110">**AzSynapseIntegrationRuntimeKey** Cmdlet 會取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="286d1-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="286d1-111">金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="286d1-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="286d1-112">示例</span><span class="sxs-lookup"><span data-stu-id="286d1-112">EXAMPLES</span></span>

### <span data-ttu-id="286d1-113">範例1</span><span class="sxs-lookup"><span data-stu-id="286d1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="286d1-114">這個 Cmdlet 會檢索名為「test-selfhost-ir」的整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="286d1-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="286d1-115">參數</span><span class="sxs-lookup"><span data-stu-id="286d1-115">PARAMETERS</span></span>

### <span data-ttu-id="286d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286d1-116">-DefaultProfile</span></span>
<span data-ttu-id="286d1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="286d1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="286d1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="286d1-118">-InputObject</span></span>
<span data-ttu-id="286d1-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="286d1-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="286d1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="286d1-120">-Name</span></span>
<span data-ttu-id="286d1-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="286d1-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="286d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="286d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="286d1-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="286d1-123">Resource group name.</span></span>

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

### <span data-ttu-id="286d1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="286d1-124">-ResourceId</span></span>
<span data-ttu-id="286d1-125">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="286d1-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="286d1-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="286d1-126">-WorkspaceName</span></span>
<span data-ttu-id="286d1-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="286d1-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="286d1-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="286d1-128">-WorkspaceObject</span></span>
<span data-ttu-id="286d1-129">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="286d1-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="286d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286d1-130">CommonParameters</span></span>
<span data-ttu-id="286d1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="286d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286d1-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="286d1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286d1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="286d1-133">INPUTS</span></span>

### <span data-ttu-id="286d1-134">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="286d1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="286d1-135">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="286d1-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="286d1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="286d1-136">OUTPUTS</span></span>

### <span data-ttu-id="286d1-137">PSIntegrationRuntimeKeys 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="286d1-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="286d1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="286d1-138">NOTES</span></span>

## <span data-ttu-id="286d1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="286d1-139">RELATED LINKS</span></span>