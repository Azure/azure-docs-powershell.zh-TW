---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6df0e33ff94be7bf5e060b929206c09180d830f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904194"
---
# <span data-ttu-id="de768-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="de768-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="de768-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de768-102">SYNOPSIS</span></span>
<span data-ttu-id="de768-103">刪除 Synapse Analytics 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="de768-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="de768-104">語法</span><span class="sxs-lookup"><span data-stu-id="de768-104">SYNTAX</span></span>

### <span data-ttu-id="de768-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="de768-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de768-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de768-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de768-107">描述</span><span class="sxs-lookup"><span data-stu-id="de768-107">DESCRIPTION</span></span>
<span data-ttu-id="de768-108">**Remove-AzSynapseFirewallRule** Cmdlet 會永久刪除 Azure Synapse Analytics 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="de768-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="de768-109">例子</span><span class="sxs-lookup"><span data-stu-id="de768-109">EXAMPLES</span></span>

### <span data-ttu-id="de768-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="de768-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="de768-111">此命令會刪除工作區 ContosoWorkspace 下名為 ContosoFirewallRule 與名稱 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="de768-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="de768-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="de768-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="de768-113">此命令會透過管線刪除工作區下名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="de768-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="de768-114">參數</span><span class="sxs-lookup"><span data-stu-id="de768-114">PARAMETERS</span></span>

### <span data-ttu-id="de768-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de768-115">-AsJob</span></span>
<span data-ttu-id="de768-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="de768-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de768-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de768-117">-DefaultProfile</span></span>
<span data-ttu-id="de768-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de768-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de768-119">-強制</span><span class="sxs-lookup"><span data-stu-id="de768-119">-Force</span></span>
<span data-ttu-id="de768-120">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="de768-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="de768-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="de768-121">-Name</span></span>
<span data-ttu-id="de768-122">工作區的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="de768-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de768-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de768-123">-PassThru</span></span>
<span data-ttu-id="de768-124">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="de768-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="de768-125">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="de768-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="de768-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de768-126">-ResourceGroupName</span></span>
<span data-ttu-id="de768-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="de768-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de768-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="de768-128">-WorkspaceName</span></span>
<span data-ttu-id="de768-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="de768-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de768-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="de768-130">-WorkspaceObject</span></span>
<span data-ttu-id="de768-131">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="de768-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de768-132">-確認</span><span class="sxs-lookup"><span data-stu-id="de768-132">-Confirm</span></span>
<span data-ttu-id="de768-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de768-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de768-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de768-134">-WhatIf</span></span>
<span data-ttu-id="de768-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de768-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de768-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de768-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de768-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de768-137">CommonParameters</span></span>
<span data-ttu-id="de768-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de768-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de768-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de768-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de768-140">輸入</span><span class="sxs-lookup"><span data-stu-id="de768-140">INPUTS</span></span>

### <span data-ttu-id="de768-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="de768-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="de768-142">輸出</span><span class="sxs-lookup"><span data-stu-id="de768-142">OUTPUTS</span></span>

### <span data-ttu-id="de768-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de768-143">System.Boolean</span></span>

## <span data-ttu-id="de768-144">筆記</span><span class="sxs-lookup"><span data-stu-id="de768-144">NOTES</span></span>

## <span data-ttu-id="de768-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="de768-145">RELATED LINKS</span></span>
