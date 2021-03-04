---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: e630bdba87f345229ffe18e4cf2011f82f78dc73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907945"
---
# <span data-ttu-id="6a895-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6a895-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="6a895-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a895-102">SYNOPSIS</span></span>
<span data-ttu-id="6a895-103">建立 Synapse Analytics 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6a895-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="6a895-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a895-104">SYNTAX</span></span>

### <span data-ttu-id="6a895-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6a895-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a895-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a895-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a895-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a895-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a895-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a895-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a895-109">描述</span><span class="sxs-lookup"><span data-stu-id="6a895-109">DESCRIPTION</span></span>
<span data-ttu-id="6a895-110">**New-AzSynapseFirewallRule** Cmdlet 會建立 Azure Synapse Analytics Firewall Rule。</span><span class="sxs-lookup"><span data-stu-id="6a895-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="6a895-111">例子</span><span class="sxs-lookup"><span data-stu-id="6a895-111">EXAMPLES</span></span>

### <span data-ttu-id="6a895-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6a895-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="6a895-113">此命令在工作區 ContosoWorkspace 下建立名為 ContosoFirewallRule 的防火牆規則，並命名為 ContosoFirewallRule。</span><span class="sxs-lookup"><span data-stu-id="6a895-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="6a895-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="6a895-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="6a895-115">此命令會透過管線在工作區下建立名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6a895-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="6a895-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="6a895-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="6a895-117">此命令會建立允許工作區下所有 azure ip 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6a895-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="6a895-118">參數</span><span class="sxs-lookup"><span data-stu-id="6a895-118">PARAMETERS</span></span>

### <span data-ttu-id="6a895-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="6a895-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="6a895-120">建立允許所有 Azure IP 存取的特殊防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6a895-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a895-121">-AsJob</span></span>
<span data-ttu-id="6a895-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6a895-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a895-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a895-123">-DefaultProfile</span></span>
<span data-ttu-id="6a895-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a895-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a895-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a895-125">-EndIpAddress</span></span>
<span data-ttu-id="6a895-126">防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6a895-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="6a895-127">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="6a895-127">Must be IPv4 format.</span></span>
<span data-ttu-id="6a895-128">必須大於或等於 startIpAddress。</span><span class="sxs-lookup"><span data-stu-id="6a895-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a895-129">-Name</span></span>
<span data-ttu-id="6a895-130">工作區的防火牆規則名稱。</span><span class="sxs-lookup"><span data-stu-id="6a895-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a895-131">-ResourceGroupName</span></span>
<span data-ttu-id="6a895-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6a895-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="6a895-133">-StartIpAddress</span></span>
<span data-ttu-id="6a895-134">防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6a895-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="6a895-135">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="6a895-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a895-136">-WorkspaceName</span></span>
<span data-ttu-id="6a895-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a895-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a895-138">-WorkspaceObject</span></span>
<span data-ttu-id="6a895-139">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="6a895-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a895-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6a895-140">-Confirm</span></span>
<span data-ttu-id="6a895-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6a895-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a895-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a895-142">-WhatIf</span></span>
<span data-ttu-id="6a895-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6a895-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a895-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a895-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a895-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a895-145">CommonParameters</span></span>
<span data-ttu-id="6a895-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a895-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a895-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a895-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a895-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6a895-148">INPUTS</span></span>

### <span data-ttu-id="6a895-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a895-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6a895-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6a895-150">OUTPUTS</span></span>

### <span data-ttu-id="6a895-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6a895-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="6a895-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6a895-152">NOTES</span></span>

## <span data-ttu-id="6a895-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a895-153">RELATED LINKS</span></span>
