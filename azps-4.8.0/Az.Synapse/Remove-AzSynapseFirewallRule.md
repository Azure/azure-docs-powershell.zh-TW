---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971360"
---
# <span data-ttu-id="167b8-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="167b8-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="167b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="167b8-102">SYNOPSIS</span></span>
<span data-ttu-id="167b8-103">刪除 Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="167b8-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="167b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="167b8-104">SYNTAX</span></span>

### <span data-ttu-id="167b8-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="167b8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="167b8-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="167b8-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="167b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="167b8-107">DESCRIPTION</span></span>
<span data-ttu-id="167b8-108">**AzSynapseFirewallRule** Cmdlet 會永久刪除 Azure Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="167b8-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="167b8-109">示例</span><span class="sxs-lookup"><span data-stu-id="167b8-109">EXAMPLES</span></span>

### <span data-ttu-id="167b8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="167b8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="167b8-111">這個命令會在 [工作區 ContosoWorkspace] 下刪除名為 [ContosoFirewallRule] 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="167b8-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="167b8-112">範例2</span><span class="sxs-lookup"><span data-stu-id="167b8-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="167b8-113">這個命令會在工作區透過管線中刪除名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="167b8-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="167b8-114">參數</span><span class="sxs-lookup"><span data-stu-id="167b8-114">PARAMETERS</span></span>

### <span data-ttu-id="167b8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="167b8-115">-AsJob</span></span>
<span data-ttu-id="167b8-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="167b8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="167b8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167b8-117">-DefaultProfile</span></span>
<span data-ttu-id="167b8-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="167b8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="167b8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="167b8-119">-Name</span></span>
<span data-ttu-id="167b8-120">工作區的 firerwall 規則名稱。</span><span class="sxs-lookup"><span data-stu-id="167b8-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="167b8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="167b8-121">-PassThru</span></span>
<span data-ttu-id="167b8-122">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="167b8-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="167b8-123">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="167b8-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="167b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="167b8-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="167b8-125">Resource group name.</span></span>

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

### <span data-ttu-id="167b8-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="167b8-126">-WorkspaceName</span></span>
<span data-ttu-id="167b8-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="167b8-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="167b8-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="167b8-128">-WorkspaceObject</span></span>
<span data-ttu-id="167b8-129">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="167b8-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="167b8-130">-確認</span><span class="sxs-lookup"><span data-stu-id="167b8-130">-Confirm</span></span>
<span data-ttu-id="167b8-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="167b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="167b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="167b8-132">-WhatIf</span></span>
<span data-ttu-id="167b8-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="167b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="167b8-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="167b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="167b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="167b8-135">CommonParameters</span></span>
<span data-ttu-id="167b8-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="167b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="167b8-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="167b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="167b8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="167b8-138">INPUTS</span></span>

### <span data-ttu-id="167b8-139">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="167b8-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="167b8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="167b8-140">OUTPUTS</span></span>

### <span data-ttu-id="167b8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="167b8-141">System.Boolean</span></span>

## <span data-ttu-id="167b8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="167b8-142">NOTES</span></span>

## <span data-ttu-id="167b8-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="167b8-143">RELATED LINKS</span></span>