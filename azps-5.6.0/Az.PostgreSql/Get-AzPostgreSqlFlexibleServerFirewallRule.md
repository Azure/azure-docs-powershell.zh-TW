---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerFirewallRule.md
ms.openlocfilehash: c6197ff97191c50f7f85acbee0a8ce51b54d8211
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902845"
---
# <span data-ttu-id="15a0c-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="15a0c-101">Get-AzPostgreSqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="15a0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="15a0c-103">列出給定伺服器中所有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="15a0c-103">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="15a0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="15a0c-104">SYNTAX</span></span>

### <span data-ttu-id="15a0c-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="15a0c-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15a0c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="15a0c-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15a0c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15a0c-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="15a0c-108">描述</span><span class="sxs-lookup"><span data-stu-id="15a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="15a0c-109">列出給定伺服器中所有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="15a0c-109">List all the firewall rules in a given server.</span></span>

## <span data-ttu-id="15a0c-110">例子</span><span class="sxs-lookup"><span data-stu-id="15a0c-110">EXAMPLES</span></span>

### <span data-ttu-id="15a0c-111">範例 1：根據名稱取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="15a0c-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="15a0c-112">此 Cmdlet 會按名稱獲得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="15a0c-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="15a0c-113">範例 2：根據身分識別取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="15a0c-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/servers/postgresql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="15a0c-114">此 Cmdlet 會以身分識別獲得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="15a0c-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="15a0c-115">範例 3：列出指定 PostgreSql 伺服器中所有的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="15a0c-115">Example 3: Lists all the firewall rules in the specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerFirewallRule -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="15a0c-116">此 Cmdlet 會列出指定 PostgreSql 伺服器中所有的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="15a0c-116">This cmdlet lists all the firewall rule in specified PostgreSql server.</span></span>

## <span data-ttu-id="15a0c-117">參數</span><span class="sxs-lookup"><span data-stu-id="15a0c-117">PARAMETERS</span></span>

### <span data-ttu-id="15a0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a0c-118">-DefaultProfile</span></span>
<span data-ttu-id="15a0c-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a0c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a0c-120">-InputObject</span></span>
<span data-ttu-id="15a0c-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="15a0c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="15a0c-122">-Name</span></span>
<span data-ttu-id="15a0c-123">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a0c-124">-ResourceGroupName</span></span>
<span data-ttu-id="15a0c-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-125">The name of the resource group.</span></span>
<span data-ttu-id="15a0c-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="15a0c-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="15a0c-127">-ServerName</span></span>
<span data-ttu-id="15a0c-128">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15a0c-129">-SubscriptionId</span></span>
<span data-ttu-id="15a0c-130">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="15a0c-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a0c-131">CommonParameters</span></span>
<span data-ttu-id="15a0c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15a0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a0c-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15a0c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a0c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="15a0c-134">INPUTS</span></span>

### <span data-ttu-id="15a0c-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="15a0c-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="15a0c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="15a0c-136">OUTPUTS</span></span>

### <span data-ttu-id="15a0c-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="15a0c-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="15a0c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="15a0c-138">NOTES</span></span>

<span data-ttu-id="15a0c-139">別名</span><span class="sxs-lookup"><span data-stu-id="15a0c-139">ALIASES</span></span>

<span data-ttu-id="15a0c-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="15a0c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15a0c-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="15a0c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15a0c-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="15a0c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15a0c-143">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="15a0c-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15a0c-144">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="15a0c-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="15a0c-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="15a0c-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="15a0c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15a0c-148">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="15a0c-149">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15a0c-150">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="15a0c-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="15a0c-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="15a0c-152">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="15a0c-153">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="15a0c-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15a0c-154">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="15a0c-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="15a0c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="15a0c-155">RELATED LINKS</span></span>

