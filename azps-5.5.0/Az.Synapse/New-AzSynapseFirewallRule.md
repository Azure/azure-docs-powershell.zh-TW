---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137686"
---
# <span data-ttu-id="ca544-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca544-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="ca544-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca544-102">SYNOPSIS</span></span>
<span data-ttu-id="ca544-103">建立 Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ca544-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ca544-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca544-104">SYNTAX</span></span>

### <span data-ttu-id="ca544-105">CreateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ca544-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca544-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca544-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca544-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca544-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca544-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca544-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca544-109">說明</span><span class="sxs-lookup"><span data-stu-id="ca544-109">DESCRIPTION</span></span>
<span data-ttu-id="ca544-110">**新的-AzSynapseFirewallRule** Cmdlet 會建立 Azure Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ca544-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ca544-111">示例</span><span class="sxs-lookup"><span data-stu-id="ca544-111">EXAMPLES</span></span>

### <span data-ttu-id="ca544-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ca544-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="ca544-113">這個命令會在 [工作區 ContosoWorkspace] 下建立名為 [ContosoFirewallRule] 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ca544-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="ca544-114">範例2</span><span class="sxs-lookup"><span data-stu-id="ca544-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="ca544-115">這個命令會透過管線在工作區下建立名為 ContosoFirewallRule 的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ca544-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="ca544-116">範例3</span><span class="sxs-lookup"><span data-stu-id="ca544-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="ca544-117">這個命令會建立允許所有 azure ip 在工作區下方的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ca544-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="ca544-118">參數</span><span class="sxs-lookup"><span data-stu-id="ca544-118">PARAMETERS</span></span>

### <span data-ttu-id="ca544-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="ca544-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="ca544-120">建立特殊的防火牆規則，以允許所有 Azure Ip 都能存取。</span><span class="sxs-lookup"><span data-stu-id="ca544-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="ca544-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca544-121">-AsJob</span></span>
<span data-ttu-id="ca544-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca544-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca544-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca544-123">-DefaultProfile</span></span>
<span data-ttu-id="ca544-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca544-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca544-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca544-125">-EndIpAddress</span></span>
<span data-ttu-id="ca544-126">防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ca544-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="ca544-127">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="ca544-127">Must be IPv4 format.</span></span>
<span data-ttu-id="ca544-128">必須大於或等於 startIpAddress。</span><span class="sxs-lookup"><span data-stu-id="ca544-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="ca544-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca544-129">-Name</span></span>
<span data-ttu-id="ca544-130">工作區的 firerwall 規則名稱。</span><span class="sxs-lookup"><span data-stu-id="ca544-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="ca544-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca544-131">-ResourceGroupName</span></span>
<span data-ttu-id="ca544-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ca544-132">Resource group name.</span></span>

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

### <span data-ttu-id="ca544-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca544-133">-StartIpAddress</span></span>
<span data-ttu-id="ca544-134">防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ca544-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="ca544-135">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="ca544-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="ca544-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ca544-136">-WorkspaceName</span></span>
<span data-ttu-id="ca544-137">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca544-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ca544-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ca544-138">-WorkspaceObject</span></span>
<span data-ttu-id="ca544-139">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="ca544-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ca544-140">-確認</span><span class="sxs-lookup"><span data-stu-id="ca544-140">-Confirm</span></span>
<span data-ttu-id="ca544-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca544-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca544-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca544-142">-WhatIf</span></span>
<span data-ttu-id="ca544-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca544-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca544-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca544-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca544-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca544-145">CommonParameters</span></span>
<span data-ttu-id="ca544-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca544-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca544-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca544-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca544-148">輸入</span><span class="sxs-lookup"><span data-stu-id="ca544-148">INPUTS</span></span>

### <span data-ttu-id="ca544-149">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ca544-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ca544-150">輸出</span><span class="sxs-lookup"><span data-stu-id="ca544-150">OUTPUTS</span></span>

### <span data-ttu-id="ca544-151">PSSynapseIpFirewallRule 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ca544-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="ca544-152">筆記</span><span class="sxs-lookup"><span data-stu-id="ca544-152">NOTES</span></span>

## <span data-ttu-id="ca544-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca544-153">RELATED LINKS</span></span>
