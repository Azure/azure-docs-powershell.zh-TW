---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7d474000ed8c449c95ae7319a960c5f748d80e66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127569"
---
# <span data-ttu-id="781c3-101">Update-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="781c3-101">Update-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="781c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="781c3-102">SYNOPSIS</span></span>
<span data-ttu-id="781c3-103">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="781c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="781c3-104">SYNTAX</span></span>

### <span data-ttu-id="781c3-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="781c3-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -EndIPAddress <String> -StartIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="781c3-106">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="781c3-106">ClientIPAddress</span></span>
```
Update-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -ClientIPAddress <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="781c3-107">ClientIPAddressViaIdentity</span><span class="sxs-lookup"><span data-stu-id="781c3-107">ClientIPAddressViaIdentity</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -ClientIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="781c3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="781c3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> -EndIPAddress <String> -StartIPAddress <String>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="781c3-109">說明</span><span class="sxs-lookup"><span data-stu-id="781c3-109">DESCRIPTION</span></span>
<span data-ttu-id="781c3-110">建立新的防火牆規則或更新現有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-110">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="781c3-111">示例</span><span class="sxs-lookup"><span data-stu-id="781c3-111">EXAMPLES</span></span>

### <span data-ttu-id="781c3-112">範例1：更新 MariaDB 防火牆規則</span><span class="sxs-lookup"><span data-stu-id="781c3-112">Example 1: Update MariaDB firewall rule</span></span>
```powershell
PS C:\> Update-AzMariaDbFirewallRule -Name fr-cfgl3y -ServerName mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StartIPAddress 0.0.3.1 -EndIPAddress 0.0.3.255

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.3.1        0.0.3.255
```

<span data-ttu-id="781c3-113">這個命令會更新 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-113">This command updates a MariaDB firewall rule.</span></span>

### <span data-ttu-id="781c3-114">範例2：依身分識別來更新 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-114">Example 2: Update MariaDB Firewall Rule by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID -EndIPAddress 0.0.0.3 -StartIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.3
```

<span data-ttu-id="781c3-115">此 Cmdlet 會依身分識別來更新 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-115">The cmdlet updates MariaDB Firewall Rule by identity.</span></span>

### <span data-ttu-id="781c3-116">範例3：以-ClientIPAddress 更新 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-116">Example 3: Update MariaDB Firewall Rule by -ClientIPAddress.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/mariadb-test-qu5ov0/providers/Microsoft.DBforMariaDB/servers/mariadb-test-4rmtig/firewallRules/fr-cfgl3y"
PS C:\> Update-AzMariaDbFirewallRule -InputObject $ID --ClientIPAddress 0.0.0.2

Name      StartIPAddress EndIPAddress
----      -------------- ------------
fr-cfgl3y 0.0.0.2        0.0.0.2
```

<span data-ttu-id="781c3-117">Cmdlet 會透過-ClientIPAddress 更新 MariaDB 防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="781c3-117">The cmdlet updates MariaDB Firewall Rule by -ClientIPAddress.</span></span>

## <span data-ttu-id="781c3-118">參數</span><span class="sxs-lookup"><span data-stu-id="781c3-118">PARAMETERS</span></span>

### <span data-ttu-id="781c3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="781c3-119">-AsJob</span></span>
<span data-ttu-id="781c3-120">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="781c3-120">Run the command as a job</span></span>

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

### <span data-ttu-id="781c3-121">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="781c3-121">-ClientIPAddress</span></span>
<span data-ttu-id="781c3-122">用戶端指定的伺服器防火牆規則單一 IP。</span><span class="sxs-lookup"><span data-stu-id="781c3-122">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="781c3-123">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="781c3-123">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="781c3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="781c3-124">-DefaultProfile</span></span>
<span data-ttu-id="781c3-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="781c3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="781c3-126">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="781c3-126">-EndIPAddress</span></span>
<span data-ttu-id="781c3-127">伺服器防火牆規則的結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="781c3-127">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="781c3-128">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="781c3-128">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="781c3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="781c3-129">-InputObject</span></span>
<span data-ttu-id="781c3-130">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="781c3-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ClientIPAddressViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="781c3-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="781c3-131">-Name</span></span>
<span data-ttu-id="781c3-132">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-132">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="781c3-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="781c3-133">-NoWait</span></span>
<span data-ttu-id="781c3-134">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="781c3-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="781c3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="781c3-135">-ResourceGroupName</span></span>
<span data-ttu-id="781c3-136">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="781c3-137">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="781c3-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="781c3-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="781c3-138">-ServerName</span></span>
<span data-ttu-id="781c3-139">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-139">The name of the server.</span></span>

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

### <span data-ttu-id="781c3-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="781c3-140">-StartIPAddress</span></span>
<span data-ttu-id="781c3-141">伺服器防火牆規則的起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="781c3-141">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="781c3-142">必須是 IPv4 格式。</span><span class="sxs-lookup"><span data-stu-id="781c3-142">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="781c3-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="781c3-143">-SubscriptionId</span></span>
<span data-ttu-id="781c3-144">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="781c3-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="781c3-145">-確認</span><span class="sxs-lookup"><span data-stu-id="781c3-145">-Confirm</span></span>
<span data-ttu-id="781c3-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="781c3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="781c3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="781c3-147">-WhatIf</span></span>
<span data-ttu-id="781c3-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="781c3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="781c3-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="781c3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="781c3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="781c3-150">CommonParameters</span></span>
<span data-ttu-id="781c3-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="781c3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="781c3-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="781c3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="781c3-153">輸入</span><span class="sxs-lookup"><span data-stu-id="781c3-153">INPUTS</span></span>

### <span data-ttu-id="781c3-154">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="781c3-154">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="781c3-155">輸出</span><span class="sxs-lookup"><span data-stu-id="781c3-155">OUTPUTS</span></span>

### <span data-ttu-id="781c3-156">IFirewallRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="781c3-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="781c3-157">筆記</span><span class="sxs-lookup"><span data-stu-id="781c3-157">NOTES</span></span>

<span data-ttu-id="781c3-158">別名</span><span class="sxs-lookup"><span data-stu-id="781c3-158">ALIASES</span></span>

<span data-ttu-id="781c3-159">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="781c3-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="781c3-160">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="781c3-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="781c3-161">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="781c3-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="781c3-162">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="781c3-162">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="781c3-163">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-163">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="781c3-164">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="781c3-165">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-165">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="781c3-166">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="781c3-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="781c3-167">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-167">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="781c3-168">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-168">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="781c3-169">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="781c3-169">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="781c3-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-170">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="781c3-171">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-171">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="781c3-172">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="781c3-172">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="781c3-173">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="781c3-173">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="781c3-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="781c3-174">RELATED LINKS</span></span>

