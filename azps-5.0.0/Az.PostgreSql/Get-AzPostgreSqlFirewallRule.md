---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139672"
---
# <span data-ttu-id="77462-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="77462-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="77462-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77462-102">SYNOPSIS</span></span>
<span data-ttu-id="77462-103">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="77462-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="77462-104">句法</span><span class="sxs-lookup"><span data-stu-id="77462-104">SYNTAX</span></span>

### <span data-ttu-id="77462-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="77462-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77462-106">獲取</span><span class="sxs-lookup"><span data-stu-id="77462-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77462-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="77462-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="77462-108">說明</span><span class="sxs-lookup"><span data-stu-id="77462-108">DESCRIPTION</span></span>
<span data-ttu-id="77462-109">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="77462-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="77462-110">示例</span><span class="sxs-lookup"><span data-stu-id="77462-110">EXAMPLES</span></span>

### <span data-ttu-id="77462-111">範例1：列出指定 PostgreSql 伺服器中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="77462-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="77462-112">這個 Cmdlet 會列出指定 PostgreSql 伺服器中的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="77462-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="77462-113">範例2：依名稱取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="77462-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="77462-114">這個 Cmdlet 會依名稱取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="77462-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="77462-115">範例3：依身分識別取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="77462-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="77462-116">這個 Cmdlet 會依身分識別來取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="77462-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="77462-117">參數</span><span class="sxs-lookup"><span data-stu-id="77462-117">PARAMETERS</span></span>

### <span data-ttu-id="77462-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77462-118">-DefaultProfile</span></span>
<span data-ttu-id="77462-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77462-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77462-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77462-120">-InputObject</span></span>
<span data-ttu-id="77462-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="77462-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="77462-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="77462-122">-Name</span></span>
<span data-ttu-id="77462-123">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="77462-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77462-124">-ResourceGroupName</span></span>
<span data-ttu-id="77462-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-125">The name of the resource group.</span></span>
<span data-ttu-id="77462-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="77462-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="77462-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="77462-127">-ServerName</span></span>
<span data-ttu-id="77462-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-128">The name of the server.</span></span>

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

### <span data-ttu-id="77462-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77462-129">-SubscriptionId</span></span>
<span data-ttu-id="77462-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="77462-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="77462-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77462-131">CommonParameters</span></span>
<span data-ttu-id="77462-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77462-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77462-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="77462-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77462-134">輸入</span><span class="sxs-lookup"><span data-stu-id="77462-134">INPUTS</span></span>

### <span data-ttu-id="77462-135">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="77462-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="77462-136">輸出</span><span class="sxs-lookup"><span data-stu-id="77462-136">OUTPUTS</span></span>

### <span data-ttu-id="77462-137">IFirewallRule （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="77462-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="77462-138">筆記</span><span class="sxs-lookup"><span data-stu-id="77462-138">NOTES</span></span>

<span data-ttu-id="77462-139">別名</span><span class="sxs-lookup"><span data-stu-id="77462-139">ALIASES</span></span>

<span data-ttu-id="77462-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="77462-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="77462-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="77462-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="77462-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="77462-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="77462-143">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="77462-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="77462-144">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="77462-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="77462-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="77462-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="77462-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="77462-148">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="77462-149">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="77462-150">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="77462-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="77462-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="77462-152">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="77462-153">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="77462-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="77462-154">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="77462-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="77462-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="77462-155">RELATED LINKS</span></span>

