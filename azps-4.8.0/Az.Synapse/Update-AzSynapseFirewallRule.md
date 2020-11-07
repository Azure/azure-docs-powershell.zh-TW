---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968904"
---
# <span data-ttu-id="2be93-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2be93-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="2be93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2be93-102">SYNOPSIS</span></span>
<span data-ttu-id="2be93-103">更新 Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2be93-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="2be93-104">句法</span><span class="sxs-lookup"><span data-stu-id="2be93-104">SYNTAX</span></span>

### <span data-ttu-id="2be93-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2be93-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2be93-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2be93-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2be93-107">說明</span><span class="sxs-lookup"><span data-stu-id="2be93-107">DESCRIPTION</span></span>
<span data-ttu-id="2be93-108">**AzSynapseFirewallRule** Cmdlet Modifys Azure Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2be93-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="2be93-109">示例</span><span class="sxs-lookup"><span data-stu-id="2be93-109">EXAMPLES</span></span>

### <span data-ttu-id="2be93-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2be93-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="2be93-111">這個命令會在 [工作區 ContosoWorkspace] 下更新名為 [ContosoFirewallRule] 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2be93-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="2be93-112">範例2</span><span class="sxs-lookup"><span data-stu-id="2be93-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="2be93-113">這個命令會透過管線在工作區下更新名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2be93-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="2be93-114">參數</span><span class="sxs-lookup"><span data-stu-id="2be93-114">PARAMETERS</span></span>

### <span data-ttu-id="2be93-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2be93-115">-AsJob</span></span>
<span data-ttu-id="2be93-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2be93-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2be93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be93-117">-DefaultProfile</span></span>
<span data-ttu-id="2be93-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2be93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be93-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="2be93-119">-EndIpAddress</span></span>
<span data-ttu-id="2be93-120">防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2be93-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="2be93-121">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="2be93-121">Must be IPv4 format.</span></span>
<span data-ttu-id="2be93-122">必須大於或等於 startIpAddress。</span><span class="sxs-lookup"><span data-stu-id="2be93-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="2be93-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2be93-123">-Name</span></span>
<span data-ttu-id="2be93-124">工作區的 firerwall 規則名稱。</span><span class="sxs-lookup"><span data-stu-id="2be93-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="2be93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be93-125">-ResourceGroupName</span></span>
<span data-ttu-id="2be93-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2be93-126">Resource group name.</span></span>

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

### <span data-ttu-id="2be93-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="2be93-127">-StartIpAddress</span></span>
<span data-ttu-id="2be93-128">防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="2be93-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="2be93-129">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="2be93-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="2be93-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2be93-130">-WorkspaceName</span></span>
<span data-ttu-id="2be93-131">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="2be93-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2be93-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2be93-132">-WorkspaceObject</span></span>
<span data-ttu-id="2be93-133">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="2be93-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2be93-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2be93-134">-Confirm</span></span>
<span data-ttu-id="2be93-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2be93-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be93-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be93-136">-WhatIf</span></span>
<span data-ttu-id="2be93-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2be93-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be93-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2be93-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be93-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be93-139">CommonParameters</span></span>
<span data-ttu-id="2be93-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2be93-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be93-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2be93-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be93-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2be93-142">INPUTS</span></span>

### <span data-ttu-id="2be93-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="2be93-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2be93-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2be93-144">OUTPUTS</span></span>

### <span data-ttu-id="2be93-145">PSSynapseIpFirewallRule 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="2be93-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="2be93-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2be93-146">NOTES</span></span>

## <span data-ttu-id="2be93-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2be93-147">RELATED LINKS</span></span>
