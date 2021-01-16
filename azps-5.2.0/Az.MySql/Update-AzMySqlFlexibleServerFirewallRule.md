---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 5df722564e899d46a1f68bf8e88ecdaa2b792121
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281801"
---
# <span data-ttu-id="04c68-101">Update-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04c68-101">Update-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="04c68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04c68-102">SYNOPSIS</span></span>
<span data-ttu-id="04c68-103">更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="04c68-103">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="04c68-104">句法</span><span class="sxs-lookup"><span data-stu-id="04c68-104">SYNTAX</span></span>

### <span data-ttu-id="04c68-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="04c68-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04c68-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="04c68-106">ClientIPAddress</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04c68-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="04c68-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04c68-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="04c68-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> -EndIPAddress <String>
 -StartIPAddress <String> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="04c68-109">說明</span><span class="sxs-lookup"><span data-stu-id="04c68-109">DESCRIPTION</span></span>
<span data-ttu-id="04c68-110">更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="04c68-110">Updates an existing firewall rule.</span></span>

## <span data-ttu-id="04c68-111">示例</span><span class="sxs-lookup"><span data-stu-id="04c68-111">EXAMPLES</span></span>

### <span data-ttu-id="04c68-112">範例1：依名稱更新 MySql 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="04c68-112">Example 1: Update MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="04c68-113">這個 Cmdlet 會依名稱更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="04c68-113">This cmdlet updates MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="04c68-114">範例2：依身分識別更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="04c68-114">Example 2: Update MySql Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/firewallRules/rule"
PS C:\> Update-AzMySqlFlexibleServerFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.2        0.0.0.3
```

<span data-ttu-id="04c68-115">這些 Cmdlet 會依身分識別來更新 MySql 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="04c68-115">These cmdlets update MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="04c68-116">參數</span><span class="sxs-lookup"><span data-stu-id="04c68-116">PARAMETERS</span></span>

### <span data-ttu-id="04c68-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04c68-117">-AsJob</span></span>
<span data-ttu-id="04c68-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="04c68-118">Run the command as a job</span></span>

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

### <span data-ttu-id="04c68-119">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="04c68-119">-ClientIPAddress</span></span>
<span data-ttu-id="04c68-120">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="04c68-120">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="04c68-121">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="04c68-121">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="04c68-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c68-122">-DefaultProfile</span></span>
<span data-ttu-id="04c68-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04c68-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04c68-124">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="04c68-124">-EndIPAddress</span></span>
<span data-ttu-id="04c68-125">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04c68-125">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="04c68-126">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="04c68-126">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="04c68-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04c68-127">-InputObject</span></span>
<span data-ttu-id="04c68-128">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="04c68-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04c68-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="04c68-129">-Name</span></span>
<span data-ttu-id="04c68-130">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-130">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="04c68-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04c68-131">-NoWait</span></span>
<span data-ttu-id="04c68-132">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="04c68-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04c68-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04c68-133">-ResourceGroupName</span></span>
<span data-ttu-id="04c68-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-134">The name of the resource group.</span></span>
<span data-ttu-id="04c68-135">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="04c68-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="04c68-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04c68-136">-ServerName</span></span>
<span data-ttu-id="04c68-137">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-137">The name of the server.</span></span>

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

### <span data-ttu-id="04c68-138">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="04c68-138">-StartIPAddress</span></span>
<span data-ttu-id="04c68-139">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="04c68-139">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="04c68-140">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="04c68-140">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="04c68-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04c68-141">-SubscriptionId</span></span>
<span data-ttu-id="04c68-142">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="04c68-142">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="04c68-143">-確認</span><span class="sxs-lookup"><span data-stu-id="04c68-143">-Confirm</span></span>
<span data-ttu-id="04c68-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04c68-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c68-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c68-145">-WhatIf</span></span>
<span data-ttu-id="04c68-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04c68-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04c68-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04c68-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c68-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c68-148">CommonParameters</span></span>
<span data-ttu-id="04c68-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04c68-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c68-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04c68-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c68-151">輸入</span><span class="sxs-lookup"><span data-stu-id="04c68-151">INPUTS</span></span>

### <span data-ttu-id="04c68-152">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="04c68-152">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="04c68-153">輸出</span><span class="sxs-lookup"><span data-stu-id="04c68-153">OUTPUTS</span></span>

### <span data-ttu-id="04c68-154">IFirewallRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="04c68-154">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="04c68-155">筆記</span><span class="sxs-lookup"><span data-stu-id="04c68-155">NOTES</span></span>

<span data-ttu-id="04c68-156">別名</span><span class="sxs-lookup"><span data-stu-id="04c68-156">ALIASES</span></span>

<span data-ttu-id="04c68-157">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="04c68-157">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04c68-158">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="04c68-158">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04c68-159">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="04c68-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04c68-160">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="04c68-160">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04c68-161">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-161">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="04c68-162">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-162">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="04c68-163">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-163">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="04c68-164">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="04c68-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04c68-165">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-165">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="04c68-166">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-166">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="04c68-167">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="04c68-168">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="04c68-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="04c68-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-169">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="04c68-170">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-170">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="04c68-171">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="04c68-171">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="04c68-172">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04c68-172">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="04c68-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="04c68-173">RELATED LINKS</span></span>

