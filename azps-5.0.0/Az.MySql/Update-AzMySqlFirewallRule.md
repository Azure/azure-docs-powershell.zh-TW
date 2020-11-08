---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFirewallRule.md
ms.openlocfilehash: 979fc45bb7bdfe36133404a88a646a871cb33301
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140834"
---
# <span data-ttu-id="10093-101">Update-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10093-101">Update-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="10093-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10093-102">SYNOPSIS</span></span>
<span data-ttu-id="10093-103">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="10093-104">句法</span><span class="sxs-lookup"><span data-stu-id="10093-104">SYNTAX</span></span>

### <span data-ttu-id="10093-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="10093-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10093-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="10093-106">ClientIPAddress</span></span>
```
Update-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10093-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="10093-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="10093-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="10093-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="10093-109">說明</span><span class="sxs-lookup"><span data-stu-id="10093-109">DESCRIPTION</span></span>
<span data-ttu-id="10093-110">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="10093-111">示例</span><span class="sxs-lookup"><span data-stu-id="10093-111">EXAMPLES</span></span>

### <span data-ttu-id="10093-112">範例1：依名稱更新 MySql 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="10093-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="10093-113">這個 Cmdlet 會依名稱更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="10093-114">範例2：依身分識別更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="10093-115">這些 Cmdlet 會依身分識別來更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

### <span data-ttu-id="10093-116">範例3：依 ClientIPAddress 更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-116">Example 3: Update MySql Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.2
```

<span data-ttu-id="10093-117">這些 Cmdlet 會依 ClientIPAddress 更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="10093-117">These cmdlets update MySql Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="10093-118">參數</span><span class="sxs-lookup"><span data-stu-id="10093-118">PARAMETERS</span></span>

### <span data-ttu-id="10093-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10093-119">-AsJob</span></span>
<span data-ttu-id="10093-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="10093-120">Run the command as a job</span></span>

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

### <span data-ttu-id="10093-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="10093-121">-ClientIPAddress</span></span>
<span data-ttu-id="10093-122">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="10093-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="10093-123">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="10093-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="10093-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10093-124">-DefaultProfile</span></span>
<span data-ttu-id="10093-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10093-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10093-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="10093-126">-EndIPAddress</span></span>
<span data-ttu-id="10093-127">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="10093-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="10093-128">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="10093-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="10093-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10093-129">-InputObject</span></span>
<span data-ttu-id="10093-130">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="10093-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="10093-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="10093-131">-Name</span></span>
<span data-ttu-id="10093-132">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="10093-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="10093-133">-NoWait</span></span>
<span data-ttu-id="10093-134">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="10093-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="10093-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10093-135">-ResourceGroupName</span></span>
<span data-ttu-id="10093-136">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-136">The name of the resource group.</span></span>
<span data-ttu-id="10093-137">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="10093-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="10093-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10093-138">-ServerName</span></span>
<span data-ttu-id="10093-139">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-139">The name of the server.</span></span>

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

### <span data-ttu-id="10093-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="10093-140">-StartIPAddress</span></span>
<span data-ttu-id="10093-141">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="10093-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="10093-142">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="10093-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="10093-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10093-143">-SubscriptionId</span></span>
<span data-ttu-id="10093-144">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="10093-144">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="10093-145">-確認</span><span class="sxs-lookup"><span data-stu-id="10093-145">-Confirm</span></span>
<span data-ttu-id="10093-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10093-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10093-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10093-147">-WhatIf</span></span>
<span data-ttu-id="10093-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10093-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10093-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10093-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10093-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10093-150">CommonParameters</span></span>
<span data-ttu-id="10093-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10093-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10093-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="10093-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10093-153">輸入</span><span class="sxs-lookup"><span data-stu-id="10093-153">INPUTS</span></span>

### <span data-ttu-id="10093-154">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="10093-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="10093-155">輸出</span><span class="sxs-lookup"><span data-stu-id="10093-155">OUTPUTS</span></span>

### <span data-ttu-id="10093-156">IFirewallRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="10093-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="10093-157">筆記</span><span class="sxs-lookup"><span data-stu-id="10093-157">NOTES</span></span>

<span data-ttu-id="10093-158">別名</span><span class="sxs-lookup"><span data-stu-id="10093-158">ALIASES</span></span>

<span data-ttu-id="10093-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="10093-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="10093-160">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="10093-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="10093-161">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="10093-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="10093-162">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="10093-162">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="10093-163">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="10093-164">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="10093-165">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="10093-166">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="10093-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="10093-167">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="10093-168">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-168">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="10093-169">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="10093-169">The name is case insensitive.</span></span>
  - <span data-ttu-id="10093-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="10093-171">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="10093-172">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10093-172">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="10093-173">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="10093-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="10093-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="10093-174">RELATED LINKS</span></span>
