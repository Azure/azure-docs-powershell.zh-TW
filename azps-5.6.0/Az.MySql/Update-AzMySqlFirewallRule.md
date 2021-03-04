---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 314d8016f96d76546e0f2afee163bb5cb911ff0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906126"
---
# <span data-ttu-id="d1a1b-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1a1b-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="d1a1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a1b-103">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d1a1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1a1b-104">SYNTAX</span></span>

### <span data-ttu-id="d1a1b-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="d1a1b-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1a1b-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1a1b-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1a1b-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1a1b-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1a1b-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1a1b-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1a1b-109">描述</span><span class="sxs-lookup"><span data-stu-id="d1a1b-109">DESCRIPTION</span></span>
<span data-ttu-id="d1a1b-110">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="d1a1b-111">例子</span><span class="sxs-lookup"><span data-stu-id="d1a1b-111">EXAMPLES</span></span>

### <span data-ttu-id="d1a1b-112">範例 1：依名稱更新 MySql 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="d1a1b-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d1a1b-113">此 Cmdlet 會依名稱更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="d1a1b-114">範例 2：依身分識別更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="d1a1b-115">這些 Cmdlet 會依身分識別更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="d1a1b-116">範例 3：更新 MySql 防火牆規則 by -ClientIPAddress。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="d1a1b-117">這些 Cmdlet 會依 -ClientIPAddress 更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="d1a1b-118">參數</span><span class="sxs-lookup"><span data-stu-id="d1a1b-118">PARAMETERS</span></span>

### <span data-ttu-id="d1a1b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1a1b-119">-AsJob</span></span>
<span data-ttu-id="d1a1b-120">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="d1a1b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d1a1b-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1a1b-121">-ClientIPAddress</span></span>
<span data-ttu-id="d1a1b-122">用戶端指定的伺服器防火牆規則之單一 IP。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="d1a1b-123">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-123">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, ClientIPAddressViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a1b-124">-DefaultProfile</span></span>
<span data-ttu-id="d1a1b-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1a1b-126">-EndIPAddress</span></span>
<span data-ttu-id="d1a1b-127">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="d1a1b-128">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-128">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1a1b-129">-InputObject</span></span>
<span data-ttu-id="d1a1b-130">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="d1a1b-131">-Name</span></span>
<span data-ttu-id="d1a1b-132">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-132">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d1a1b-133">-NoWait</span></span>
<span data-ttu-id="d1a1b-134">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="d1a1b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1a1b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a1b-135">-ResourceGroupName</span></span>
<span data-ttu-id="d1a1b-136">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-136">The name of the resource group.</span></span>
<span data-ttu-id="d1a1b-137">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-137">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1a1b-138">-ServerName</span></span>
<span data-ttu-id="d1a1b-139">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-139">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1a1b-140">-StartIPAddress</span></span>
<span data-ttu-id="d1a1b-141">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="d1a1b-142">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-142">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1a1b-143">-SubscriptionId</span></span>
<span data-ttu-id="d1a1b-144">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-144">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1a1b-145">-確認</span><span class="sxs-lookup"><span data-stu-id="d1a1b-145">-Confirm</span></span>
<span data-ttu-id="d1a1b-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a1b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a1b-147">-WhatIf</span></span>
<span data-ttu-id="d1a1b-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a1b-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a1b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a1b-150">CommonParameters</span></span>
<span data-ttu-id="d1a1b-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a1b-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1a1b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a1b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="d1a1b-153">INPUTS</span></span>

### <span data-ttu-id="d1a1b-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d1a1b-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d1a1b-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d1a1b-155">OUTPUTS</span></span>

### <span data-ttu-id="d1a1b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1a1b-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d1a1b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="d1a1b-157">NOTES</span></span>

<span data-ttu-id="d1a1b-158">別名</span><span class="sxs-lookup"><span data-stu-id="d1a1b-158">ALIASES</span></span>

<span data-ttu-id="d1a1b-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d1a1b-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1a1b-160">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1a1b-161">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1a1b-162">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d1a1b-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1a1b-163">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d1a1b-164">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d1a1b-165">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d1a1b-166">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="d1a1b-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1a1b-167">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-167">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d1a1b-168">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-168">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d1a1b-169">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d1a1b-170">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-170">The name is case insensitive.</span></span>
  - <span data-ttu-id="d1a1b-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-171">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d1a1b-172">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-172">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d1a1b-173">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d1a1b-174">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1a1b-174">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d1a1b-175">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1a1b-175">RELATED LINKS</span></span>

