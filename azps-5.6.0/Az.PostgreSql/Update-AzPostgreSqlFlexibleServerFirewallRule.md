---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 26f6da2cdbf7d12e4d4927fd14ffc6b58b539bef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907585"
---
# <span data-ttu-id="0ac7a-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ac7a-101">Update-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="0ac7a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ac7a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac7a-103">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0ac7a-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ac7a-104">SYNTAX</span></span>

### <span data-ttu-id="0ac7a-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="0ac7a-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ac7a-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ac7a-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ac7a-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ac7a-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ac7a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0ac7a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0ac7a-109">描述</span><span class="sxs-lookup"><span data-stu-id="0ac7a-109">DESCRIPTION</span></span>
<span data-ttu-id="0ac7a-110">建立新防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="0ac7a-111">例子</span><span class="sxs-lookup"><span data-stu-id="0ac7a-111">EXAMPLES</span></span>

### <span data-ttu-id="0ac7a-112">範例 1：依名稱更新 PostgreSql 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="0ac7a-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="0ac7a-113">此 Cmdlet 會依名稱更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="0ac7a-114">範例 2：依身分識別更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="0ac7a-115">這些 Cmdlet 會依身分識別更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="0ac7a-116">參數</span><span class="sxs-lookup"><span data-stu-id="0ac7a-116">PARAMETERS</span></span>

### <span data-ttu-id="0ac7a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ac7a-117">-AsJob</span></span>
<span data-ttu-id="0ac7a-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="0ac7a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="0ac7a-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ac7a-119">-ClientIPAddress</span></span>
<span data-ttu-id="0ac7a-120">用戶端指定的伺服器防火牆規則之單一 IP。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="0ac7a-121">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0ac7a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac7a-122">-DefaultProfile</span></span>
<span data-ttu-id="0ac7a-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac7a-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ac7a-124">-EndIPAddress</span></span>
<span data-ttu-id="0ac7a-125">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="0ac7a-126">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0ac7a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ac7a-127">-InputObject</span></span>
<span data-ttu-id="0ac7a-128">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac7a-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ac7a-129">-Name</span></span>
<span data-ttu-id="0ac7a-130">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0ac7a-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0ac7a-131">-NoWait</span></span>
<span data-ttu-id="0ac7a-132">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="0ac7a-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ac7a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ac7a-133">-ResourceGroupName</span></span>
<span data-ttu-id="0ac7a-134">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-134">The name of the resource group.</span></span>
<span data-ttu-id="0ac7a-135">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0ac7a-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0ac7a-136">-ServerName</span></span>
<span data-ttu-id="0ac7a-137">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-137">The name of the server.</span></span>

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

### <span data-ttu-id="0ac7a-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ac7a-138">-StartIPAddress</span></span>
<span data-ttu-id="0ac7a-139">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="0ac7a-140">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0ac7a-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ac7a-141">-SubscriptionId</span></span>
<span data-ttu-id="0ac7a-142">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0ac7a-143">-確認</span><span class="sxs-lookup"><span data-stu-id="0ac7a-143">-Confirm</span></span>
<span data-ttu-id="0ac7a-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac7a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac7a-145">-WhatIf</span></span>
<span data-ttu-id="0ac7a-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ac7a-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac7a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac7a-148">CommonParameters</span></span>
<span data-ttu-id="0ac7a-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac7a-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ac7a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac7a-151">輸入</span><span class="sxs-lookup"><span data-stu-id="0ac7a-151">INPUTS</span></span>

### <span data-ttu-id="0ac7a-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0ac7a-152">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0ac7a-153">輸出</span><span class="sxs-lookup"><span data-stu-id="0ac7a-153">OUTPUTS</span></span>

### <span data-ttu-id="0ac7a-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0ac7a-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="0ac7a-155">筆記</span><span class="sxs-lookup"><span data-stu-id="0ac7a-155">NOTES</span></span>

<span data-ttu-id="0ac7a-156">別名</span><span class="sxs-lookup"><span data-stu-id="0ac7a-156">ALIASES</span></span>

<span data-ttu-id="0ac7a-157">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0ac7a-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ac7a-158">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ac7a-159">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ac7a-160">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0ac7a-160">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ac7a-161">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0ac7a-162">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0ac7a-163">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0ac7a-164">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="0ac7a-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ac7a-165">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-165">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0ac7a-166">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-166">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0ac7a-167">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-167">The name is case insensitive.</span></span>
  - <span data-ttu-id="0ac7a-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-168">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0ac7a-169">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-169">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0ac7a-170">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0ac7a-171">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ac7a-171">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0ac7a-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ac7a-172">RELATED LINKS</span></span>

