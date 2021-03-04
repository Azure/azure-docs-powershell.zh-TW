---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 48f2ea831470482a91e9ff78dc8b70472e2f556a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916821"
---
# <span data-ttu-id="2dc19-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2dc19-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="2dc19-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2dc19-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc19-103">更新 Synapse Analytics 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2dc19-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="2dc19-104">語法</span><span class="sxs-lookup"><span data-stu-id="2dc19-104">SYNTAX</span></span>

### <span data-ttu-id="2dc19-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2dc19-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dc19-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dc19-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dc19-107">描述</span><span class="sxs-lookup"><span data-stu-id="2dc19-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc19-108">**Update-AzSynapseFirewallRule** Cmdlet 會修改 Azure Synapse Analytics 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2dc19-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="2dc19-109">例子</span><span class="sxs-lookup"><span data-stu-id="2dc19-109">EXAMPLES</span></span>

### <span data-ttu-id="2dc19-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2dc19-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="2dc19-111">此命令會更新工作區 ContosoWorkspace 下名為 ContosoFirewallRule 的防火牆規則，並命名為 ContosoFirewallRule。</span><span class="sxs-lookup"><span data-stu-id="2dc19-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="2dc19-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="2dc19-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="2dc19-113">此命令會透過管線更新工作區下名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2dc19-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="2dc19-114">參數</span><span class="sxs-lookup"><span data-stu-id="2dc19-114">PARAMETERS</span></span>

### <span data-ttu-id="2dc19-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dc19-115">-AsJob</span></span>
<span data-ttu-id="2dc19-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2dc19-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dc19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc19-117">-DefaultProfile</span></span>
<span data-ttu-id="2dc19-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2dc19-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dc19-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2dc19-119">-EndIpAddress</span></span>
<span data-ttu-id="2dc19-120">防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2dc19-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="2dc19-121">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="2dc19-121">Must be IPv4 format.</span></span>
<span data-ttu-id="2dc19-122">必須大於或等於 startIpAddress。</span><span class="sxs-lookup"><span data-stu-id="2dc19-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc19-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2dc19-123">-Name</span></span>
<span data-ttu-id="2dc19-124">工作區的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="2dc19-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="2dc19-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc19-125">-ResourceGroupName</span></span>
<span data-ttu-id="2dc19-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2dc19-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc19-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2dc19-127">-StartIpAddress</span></span>
<span data-ttu-id="2dc19-128">防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2dc19-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="2dc19-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="2dc19-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc19-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2dc19-130">-WorkspaceName</span></span>
<span data-ttu-id="2dc19-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2dc19-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dc19-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2dc19-132">-WorkspaceObject</span></span>
<span data-ttu-id="2dc19-133">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="2dc19-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dc19-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2dc19-134">-Confirm</span></span>
<span data-ttu-id="2dc19-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2dc19-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc19-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc19-136">-WhatIf</span></span>
<span data-ttu-id="2dc19-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2dc19-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc19-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2dc19-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc19-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc19-139">CommonParameters</span></span>
<span data-ttu-id="2dc19-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2dc19-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc19-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dc19-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc19-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2dc19-142">INPUTS</span></span>

### <span data-ttu-id="2dc19-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2dc19-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2dc19-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2dc19-144">OUTPUTS</span></span>

### <span data-ttu-id="2dc19-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2dc19-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="2dc19-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2dc19-146">NOTES</span></span>

## <span data-ttu-id="2dc19-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dc19-147">RELATED LINKS</span></span>
