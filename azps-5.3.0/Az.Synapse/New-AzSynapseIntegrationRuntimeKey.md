---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288191"
---
# <span data-ttu-id="09d21-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="09d21-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="09d21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09d21-102">SYNOPSIS</span></span>
<span data-ttu-id="09d21-103">重新產生自託管的整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="09d21-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="09d21-104">句法</span><span class="sxs-lookup"><span data-stu-id="09d21-104">SYNTAX</span></span>

### <span data-ttu-id="09d21-105">NewByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="09d21-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09d21-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d21-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d21-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d21-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d21-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d21-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d21-109">說明</span><span class="sxs-lookup"><span data-stu-id="09d21-109">DESCRIPTION</span></span>
<span data-ttu-id="09d21-110">Cmdlet **AzSynapseIntegrationRuntimeKey** 會再生整合執行時間金鑰，並使用由 "KeyName" 參數指定的金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="09d21-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="09d21-111">前一個金鑰將無效。</span><span class="sxs-lookup"><span data-stu-id="09d21-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="09d21-112">示例</span><span class="sxs-lookup"><span data-stu-id="09d21-112">EXAMPLES</span></span>

### <span data-ttu-id="09d21-113">範例1</span><span class="sxs-lookup"><span data-stu-id="09d21-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="09d21-114">這個 Cmdlet 會為集成執行時間（名為「test-selfhost-ir」）重新產生金鑰 ' authKey2」。</span><span class="sxs-lookup"><span data-stu-id="09d21-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="09d21-115">參數</span><span class="sxs-lookup"><span data-stu-id="09d21-115">PARAMETERS</span></span>

### <span data-ttu-id="09d21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d21-116">-DefaultProfile</span></span>
<span data-ttu-id="09d21-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09d21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09d21-118">-Force</span><span class="sxs-lookup"><span data-stu-id="09d21-118">-Force</span></span>
<span data-ttu-id="09d21-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="09d21-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="09d21-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09d21-120">-InputObject</span></span>
<span data-ttu-id="09d21-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="09d21-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="09d21-122">-KeyName</span></span>
<span data-ttu-id="09d21-123">自託管整合執行時間的驗證金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="09d21-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="09d21-124">-Name</span></span>
<span data-ttu-id="09d21-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="09d21-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d21-126">-ResourceGroupName</span></span>
<span data-ttu-id="09d21-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="09d21-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09d21-128">-ResourceId</span></span>
<span data-ttu-id="09d21-129">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="09d21-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09d21-130">-WorkspaceName</span></span>
<span data-ttu-id="09d21-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="09d21-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09d21-132">-WorkspaceObject</span></span>
<span data-ttu-id="09d21-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="09d21-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-134">-確認</span><span class="sxs-lookup"><span data-stu-id="09d21-134">-Confirm</span></span>
<span data-ttu-id="09d21-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="09d21-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d21-136">-WhatIf</span></span>
<span data-ttu-id="09d21-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09d21-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09d21-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09d21-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d21-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d21-139">CommonParameters</span></span>
<span data-ttu-id="09d21-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09d21-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d21-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09d21-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d21-142">輸入</span><span class="sxs-lookup"><span data-stu-id="09d21-142">INPUTS</span></span>

### <span data-ttu-id="09d21-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="09d21-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="09d21-144">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="09d21-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="09d21-145">輸出</span><span class="sxs-lookup"><span data-stu-id="09d21-145">OUTPUTS</span></span>

### <span data-ttu-id="09d21-146">PSIntegrationRuntimeKeys 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="09d21-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="09d21-147">筆記</span><span class="sxs-lookup"><span data-stu-id="09d21-147">NOTES</span></span>

## <span data-ttu-id="09d21-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="09d21-148">RELATED LINKS</span></span>
