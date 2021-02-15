---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130415"
---
# <span data-ttu-id="c232c-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="c232c-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="c232c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c232c-102">SYNOPSIS</span></span>
<span data-ttu-id="c232c-103">取得自託管整合執行時間的鍵。</span><span class="sxs-lookup"><span data-stu-id="c232c-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="c232c-104">句法</span><span class="sxs-lookup"><span data-stu-id="c232c-104">SYNTAX</span></span>

### <span data-ttu-id="c232c-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c232c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c232c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c232c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c232c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c232c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c232c-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c232c-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c232c-109">說明</span><span class="sxs-lookup"><span data-stu-id="c232c-109">DESCRIPTION</span></span>
<span data-ttu-id="c232c-110">**AzSynapseIntegrationRuntimeKey** Cmdlet 會取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c232c-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="c232c-111">金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="c232c-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="c232c-112">示例</span><span class="sxs-lookup"><span data-stu-id="c232c-112">EXAMPLES</span></span>

### <span data-ttu-id="c232c-113">範例1</span><span class="sxs-lookup"><span data-stu-id="c232c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="c232c-114">這個 Cmdlet 會檢索名為「test-selfhost-ir」的整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c232c-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c232c-115">參數</span><span class="sxs-lookup"><span data-stu-id="c232c-115">PARAMETERS</span></span>

### <span data-ttu-id="c232c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c232c-116">-DefaultProfile</span></span>
<span data-ttu-id="c232c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c232c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c232c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c232c-118">-InputObject</span></span>
<span data-ttu-id="c232c-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="c232c-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="c232c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="c232c-120">-Name</span></span>
<span data-ttu-id="c232c-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="c232c-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="c232c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c232c-122">-ResourceGroupName</span></span>
<span data-ttu-id="c232c-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c232c-123">Resource group name.</span></span>

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

### <span data-ttu-id="c232c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c232c-124">-ResourceId</span></span>
<span data-ttu-id="c232c-125">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c232c-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="c232c-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c232c-126">-WorkspaceName</span></span>
<span data-ttu-id="c232c-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c232c-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c232c-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c232c-128">-WorkspaceObject</span></span>
<span data-ttu-id="c232c-129">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="c232c-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c232c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c232c-130">CommonParameters</span></span>
<span data-ttu-id="c232c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c232c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c232c-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c232c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c232c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c232c-133">INPUTS</span></span>

### <span data-ttu-id="c232c-134">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c232c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c232c-135">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c232c-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c232c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c232c-136">OUTPUTS</span></span>

### <span data-ttu-id="c232c-137">PSIntegrationRuntimeKeys 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="c232c-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="c232c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c232c-138">NOTES</span></span>

## <span data-ttu-id="c232c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c232c-139">RELATED LINKS</span></span>
