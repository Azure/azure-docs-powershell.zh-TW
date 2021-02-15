---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138195"
---
# <span data-ttu-id="5c89f-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5c89f-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="5c89f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c89f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c89f-103">刪除 Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5c89f-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="5c89f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c89f-104">SYNTAX</span></span>

### <span data-ttu-id="5c89f-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5c89f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c89f-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c89f-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c89f-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c89f-107">DESCRIPTION</span></span>
<span data-ttu-id="5c89f-108">**AzSynapseFirewallRule** Cmdlet 會永久刪除 Azure Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5c89f-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="5c89f-109">示例</span><span class="sxs-lookup"><span data-stu-id="5c89f-109">EXAMPLES</span></span>

### <span data-ttu-id="5c89f-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5c89f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="5c89f-111">這個命令會在 [工作區 ContosoWorkspace] 下刪除名為 [ContosoFirewallRule] 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5c89f-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="5c89f-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5c89f-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="5c89f-113">這個命令會在工作區透過管線中刪除名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="5c89f-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="5c89f-114">參數</span><span class="sxs-lookup"><span data-stu-id="5c89f-114">PARAMETERS</span></span>

### <span data-ttu-id="5c89f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c89f-115">-AsJob</span></span>
<span data-ttu-id="5c89f-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5c89f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c89f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c89f-117">-DefaultProfile</span></span>
<span data-ttu-id="5c89f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c89f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c89f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5c89f-119">-Force</span></span>
<span data-ttu-id="5c89f-120">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="5c89f-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5c89f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c89f-121">-Name</span></span>
<span data-ttu-id="5c89f-122">工作區的 firerwall 規則名稱。</span><span class="sxs-lookup"><span data-stu-id="5c89f-122">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="5c89f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c89f-123">-PassThru</span></span>
<span data-ttu-id="5c89f-124">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="5c89f-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5c89f-125">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="5c89f-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5c89f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c89f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5c89f-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5c89f-127">Resource group name.</span></span>

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

### <span data-ttu-id="5c89f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5c89f-128">-WorkspaceName</span></span>
<span data-ttu-id="5c89f-129">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c89f-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5c89f-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5c89f-130">-WorkspaceObject</span></span>
<span data-ttu-id="5c89f-131">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="5c89f-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5c89f-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5c89f-132">-Confirm</span></span>
<span data-ttu-id="5c89f-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c89f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c89f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c89f-134">-WhatIf</span></span>
<span data-ttu-id="5c89f-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c89f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c89f-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c89f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c89f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c89f-137">CommonParameters</span></span>
<span data-ttu-id="5c89f-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c89f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c89f-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c89f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c89f-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5c89f-140">INPUTS</span></span>

### <span data-ttu-id="5c89f-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="5c89f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5c89f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5c89f-142">OUTPUTS</span></span>

### <span data-ttu-id="5c89f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="5c89f-143">System.Boolean</span></span>

## <span data-ttu-id="5c89f-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5c89f-144">NOTES</span></span>

## <span data-ttu-id="5c89f-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c89f-145">RELATED LINKS</span></span>
