---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: f750718c4bd380b579dff0897b53a68ae4f45b95
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281630"
---
# <span data-ttu-id="c55c4-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c55c4-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="c55c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c55c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c55c4-103">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c55c4-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="c55c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="c55c4-104">SYNTAX</span></span>

### <span data-ttu-id="c55c4-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c55c4-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c55c4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c55c4-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c55c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c55c4-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c55c4-108">說明</span><span class="sxs-lookup"><span data-stu-id="c55c4-108">DESCRIPTION</span></span>
<span data-ttu-id="c55c4-109">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c55c4-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="c55c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="c55c4-110">EXAMPLES</span></span>

### <span data-ttu-id="c55c4-111">範例1：列出指定 MySql 伺服器中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="c55c4-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="c55c4-112">這個 Cmdlet 會列出指定 MySql 伺服器中的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c55c4-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="c55c4-113">範例2：依名稱取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="c55c4-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="c55c4-114">這個 Cmdlet 會依名稱取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c55c4-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="c55c4-115">範例3：依身分識別取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="c55c4-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="c55c4-116">這個 Cmdlet 會依身分識別來取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="c55c4-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="c55c4-117">參數</span><span class="sxs-lookup"><span data-stu-id="c55c4-117">PARAMETERS</span></span>

### <span data-ttu-id="c55c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55c4-118">-DefaultProfile</span></span>
<span data-ttu-id="c55c4-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c55c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c55c4-120">-InputObject</span></span>
<span data-ttu-id="c55c4-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c55c4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55c4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c55c4-122">-Name</span></span>
<span data-ttu-id="c55c4-123">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="c55c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="c55c4-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-125">The name of the resource group.</span></span>
<span data-ttu-id="c55c4-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c55c4-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c55c4-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c55c4-127">-ServerName</span></span>
<span data-ttu-id="c55c4-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-128">The name of the server.</span></span>

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

### <span data-ttu-id="c55c4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c55c4-129">-SubscriptionId</span></span>
<span data-ttu-id="c55c4-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="c55c4-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c55c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55c4-131">CommonParameters</span></span>
<span data-ttu-id="c55c4-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c55c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55c4-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c55c4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55c4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c55c4-134">INPUTS</span></span>

### <span data-ttu-id="c55c4-135">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c55c4-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c55c4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c55c4-136">OUTPUTS</span></span>

### <span data-ttu-id="c55c4-137">IFirewallRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="c55c4-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="c55c4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c55c4-138">NOTES</span></span>

<span data-ttu-id="c55c4-139">別名</span><span class="sxs-lookup"><span data-stu-id="c55c4-139">ALIASES</span></span>

<span data-ttu-id="c55c4-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c55c4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c55c4-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c55c4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c55c4-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c55c4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c55c4-143">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c55c4-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c55c4-144">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c55c4-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c55c4-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c55c4-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c55c4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c55c4-148">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c55c4-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c55c4-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c55c4-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c55c4-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="c55c4-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c55c4-153">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c55c4-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c55c4-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c55c4-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c55c4-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c55c4-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c55c4-156">RELATED LINKS</span></span>

