---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 43cf2d06c45d545b1d311cea474a8ec69fd49021
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275608"
---
# <span data-ttu-id="f75a4-101">Update-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f75a4-101">Update-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="f75a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f75a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f75a4-103">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f75a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f75a4-104">SYNTAX</span></span>

### <span data-ttu-id="f75a4-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f75a4-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f75a4-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f75a4-106">ClientIPAddress</span></span>
```
Update-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f75a4-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f75a4-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f75a4-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f75a4-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f75a4-109">說明</span><span class="sxs-lookup"><span data-stu-id="f75a4-109">DESCRIPTION</span></span>
<span data-ttu-id="f75a4-110">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="f75a4-111">示例</span><span class="sxs-lookup"><span data-stu-id="f75a4-111">EXAMPLES</span></span>

### <span data-ttu-id="f75a4-112">範例1：依名稱更新 PostgreSql 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="f75a4-112">Example 1: Update PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="f75a4-113">這個 Cmdlet 會依名稱更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-113">This cmdlet updates PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="f75a4-114">範例2：依身分識別來更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-114">Example 2: Update PostgreSql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.1 -StartIPAddress 0.0.0.0

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="f75a4-115">這些 Cmdlet 會依身分識別來更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-115">These cmdlets update PostgreSql Firewall Rule by identity.</span></span>

### <span data-ttu-id="f75a4-116">範例3：以-ClientIPAddress 更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-116">Example 3: Update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Update-AzPostgreSqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="f75a4-117">這些 Cmdlet 會透過-ClientIPAddress 來更新 PostgreSql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f75a4-117">These cmdlets update PostgreSql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="f75a4-118">參數</span><span class="sxs-lookup"><span data-stu-id="f75a4-118">PARAMETERS</span></span>

### <span data-ttu-id="f75a4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f75a4-119">-AsJob</span></span>
<span data-ttu-id="f75a4-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f75a4-120">Run the command as a job</span></span>

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

### <span data-ttu-id="f75a4-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="f75a4-121">-ClientIPAddress</span></span>
<span data-ttu-id="f75a4-122">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="f75a4-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="f75a4-123">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="f75a4-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f75a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75a4-124">-DefaultProfile</span></span>
<span data-ttu-id="f75a4-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f75a4-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="f75a4-126">-EndIPAddress</span></span>
<span data-ttu-id="f75a4-127">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f75a4-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="f75a4-128">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="f75a4-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f75a4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f75a4-129">-InputObject</span></span>
<span data-ttu-id="f75a4-130">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f75a4-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f75a4-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="f75a4-131">-Name</span></span>
<span data-ttu-id="f75a4-132">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="f75a4-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f75a4-133">-NoWait</span></span>
<span data-ttu-id="f75a4-134">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f75a4-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f75a4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75a4-135">-ResourceGroupName</span></span>
<span data-ttu-id="f75a4-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-136">The name of the resource group.</span></span>
<span data-ttu-id="f75a4-137">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f75a4-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f75a4-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f75a4-138">-ServerName</span></span>
<span data-ttu-id="f75a4-139">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-139">The name of the server.</span></span>

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

### <span data-ttu-id="f75a4-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="f75a4-140">-StartIPAddress</span></span>
<span data-ttu-id="f75a4-141">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f75a4-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="f75a4-142">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="f75a4-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="f75a4-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f75a4-143">-SubscriptionId</span></span>
<span data-ttu-id="f75a4-144">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="f75a4-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f75a4-145">-確認</span><span class="sxs-lookup"><span data-stu-id="f75a4-145">-Confirm</span></span>
<span data-ttu-id="f75a4-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f75a4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75a4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75a4-147">-WhatIf</span></span>
<span data-ttu-id="f75a4-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f75a4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f75a4-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f75a4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75a4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75a4-150">CommonParameters</span></span>
<span data-ttu-id="f75a4-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f75a4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75a4-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f75a4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75a4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f75a4-153">INPUTS</span></span>

### <span data-ttu-id="f75a4-154">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="f75a4-154">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="f75a4-155">輸出</span><span class="sxs-lookup"><span data-stu-id="f75a4-155">OUTPUTS</span></span>

### <span data-ttu-id="f75a4-156">IFirewallRule （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="f75a4-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="f75a4-157">筆記</span><span class="sxs-lookup"><span data-stu-id="f75a4-157">NOTES</span></span>

<span data-ttu-id="f75a4-158">別名</span><span class="sxs-lookup"><span data-stu-id="f75a4-158">ALIASES</span></span>

<span data-ttu-id="f75a4-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f75a4-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f75a4-160">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f75a4-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f75a4-161">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f75a4-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f75a4-162">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f75a4-162">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f75a4-163">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f75a4-164">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f75a4-165">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f75a4-166">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f75a4-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f75a4-167">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f75a4-168">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f75a4-169">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f75a4-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="f75a4-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f75a4-171">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f75a4-172">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f75a4-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f75a4-173">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f75a4-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f75a4-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="f75a4-174">RELATED LINKS</span></span>

