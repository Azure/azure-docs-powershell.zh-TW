---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 143238bfcc8dffc209150a675af0a982d20663bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907942"
---
# <span data-ttu-id="9eb10-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="9eb10-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="9eb10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9eb10-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb10-103">重新產生自我託管的整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="9eb10-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="9eb10-104">語法</span><span class="sxs-lookup"><span data-stu-id="9eb10-104">SYNTAX</span></span>

### <span data-ttu-id="9eb10-105">NewByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9eb10-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eb10-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eb10-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eb10-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eb10-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eb10-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eb10-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eb10-109">描述</span><span class="sxs-lookup"><span data-stu-id="9eb10-109">DESCRIPTION</span></span>
<span data-ttu-id="9eb10-110">Cmdlet **New-AzSynapse RuntimeRuntimeKey** 會以 KeyName' 參數指定的金鑰名稱重新產生整合執行時間金鑰。</span><span class="sxs-lookup"><span data-stu-id="9eb10-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="9eb10-111">上一個按鍵無效。</span><span class="sxs-lookup"><span data-stu-id="9eb10-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="9eb10-112">例子</span><span class="sxs-lookup"><span data-stu-id="9eb10-112">EXAMPLES</span></span>

### <span data-ttu-id="9eb10-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="9eb10-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="9eb10-114">Cmdlet 會針對名為'test-selfhost-ir'的整合執行時間重新產生 Key 'authKey2'。</span><span class="sxs-lookup"><span data-stu-id="9eb10-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9eb10-115">參數</span><span class="sxs-lookup"><span data-stu-id="9eb10-115">PARAMETERS</span></span>

### <span data-ttu-id="9eb10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb10-116">-DefaultProfile</span></span>
<span data-ttu-id="9eb10-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eb10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eb10-118">-強制</span><span class="sxs-lookup"><span data-stu-id="9eb10-118">-Force</span></span>
<span data-ttu-id="9eb10-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="9eb10-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9eb10-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eb10-120">-InputObject</span></span>
<span data-ttu-id="9eb10-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="9eb10-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="9eb10-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9eb10-122">-KeyName</span></span>
<span data-ttu-id="9eb10-123">自我託管整合執行時間的驗證金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb10-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9eb10-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="9eb10-124">-Name</span></span>
<span data-ttu-id="9eb10-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb10-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="9eb10-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb10-126">-ResourceGroupName</span></span>
<span data-ttu-id="9eb10-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9eb10-127">Resource group name.</span></span>

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

### <span data-ttu-id="9eb10-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eb10-128">-ResourceId</span></span>
<span data-ttu-id="9eb10-129">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9eb10-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="9eb10-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9eb10-130">-WorkspaceName</span></span>
<span data-ttu-id="9eb10-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eb10-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9eb10-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9eb10-132">-WorkspaceObject</span></span>
<span data-ttu-id="9eb10-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="9eb10-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9eb10-134">-確認</span><span class="sxs-lookup"><span data-stu-id="9eb10-134">-Confirm</span></span>
<span data-ttu-id="9eb10-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9eb10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb10-136">-WhatIf</span></span>
<span data-ttu-id="9eb10-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9eb10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb10-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb10-139">CommonParameters</span></span>
<span data-ttu-id="9eb10-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9eb10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb10-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eb10-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb10-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9eb10-142">INPUTS</span></span>

### <span data-ttu-id="9eb10-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9eb10-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9eb10-144">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="9eb10-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9eb10-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9eb10-145">OUTPUTS</span></span>

### <span data-ttu-id="9eb10-146">Microsoft.Azure.Commands.Synapse.Models.PS方格RuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="9eb10-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="9eb10-147">筆記</span><span class="sxs-lookup"><span data-stu-id="9eb10-147">NOTES</span></span>

## <span data-ttu-id="9eb10-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eb10-148">RELATED LINKS</span></span>
