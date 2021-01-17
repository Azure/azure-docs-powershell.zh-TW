---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449028"
---
# <span data-ttu-id="24b63-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="24b63-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="24b63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24b63-102">SYNOPSIS</span></span>
<span data-ttu-id="24b63-103">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24b63-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="24b63-104">句法</span><span class="sxs-lookup"><span data-stu-id="24b63-104">SYNTAX</span></span>

### <span data-ttu-id="24b63-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="24b63-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24b63-106">獲取</span><span class="sxs-lookup"><span data-stu-id="24b63-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24b63-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24b63-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="24b63-108">說明</span><span class="sxs-lookup"><span data-stu-id="24b63-108">DESCRIPTION</span></span>
<span data-ttu-id="24b63-109">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="24b63-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="24b63-110">示例</span><span class="sxs-lookup"><span data-stu-id="24b63-110">EXAMPLES</span></span>

### <span data-ttu-id="24b63-111">範例1：依名稱取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="24b63-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="24b63-112">這個 Cmdlet 會依名稱取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="24b63-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="24b63-113">範例2：依身分識別來取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="24b63-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="24b63-114">這個 Cmdlet 會依身分識別來取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="24b63-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="24b63-115">範例3：列出指定 MySql 伺服器中的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="24b63-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="24b63-116">這個 Cmdlet 會列出指定 MySql 伺服器中的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="24b63-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="24b63-117">參數</span><span class="sxs-lookup"><span data-stu-id="24b63-117">PARAMETERS</span></span>

### <span data-ttu-id="24b63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b63-118">-DefaultProfile</span></span>
<span data-ttu-id="24b63-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24b63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24b63-120">-InputObject</span></span>
<span data-ttu-id="24b63-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="24b63-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24b63-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="24b63-122">-Name</span></span>
<span data-ttu-id="24b63-123">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="24b63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b63-124">-ResourceGroupName</span></span>
<span data-ttu-id="24b63-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-125">The name of the resource group.</span></span>
<span data-ttu-id="24b63-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="24b63-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="24b63-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24b63-127">-ServerName</span></span>
<span data-ttu-id="24b63-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-128">The name of the server.</span></span>

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

### <span data-ttu-id="24b63-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24b63-129">-SubscriptionId</span></span>
<span data-ttu-id="24b63-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="24b63-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="24b63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b63-131">CommonParameters</span></span>
<span data-ttu-id="24b63-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24b63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b63-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="24b63-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b63-134">輸入</span><span class="sxs-lookup"><span data-stu-id="24b63-134">INPUTS</span></span>

### <span data-ttu-id="24b63-135">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="24b63-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="24b63-136">輸出</span><span class="sxs-lookup"><span data-stu-id="24b63-136">OUTPUTS</span></span>

### <span data-ttu-id="24b63-137">IFirewallRule 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="24b63-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="24b63-138">筆記</span><span class="sxs-lookup"><span data-stu-id="24b63-138">NOTES</span></span>

<span data-ttu-id="24b63-139">別名</span><span class="sxs-lookup"><span data-stu-id="24b63-139">ALIASES</span></span>

<span data-ttu-id="24b63-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="24b63-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24b63-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="24b63-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24b63-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="24b63-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24b63-143">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="24b63-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24b63-144">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="24b63-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="24b63-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="24b63-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="24b63-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24b63-148">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="24b63-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="24b63-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="24b63-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="24b63-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="24b63-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="24b63-153">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="24b63-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="24b63-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="24b63-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="24b63-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="24b63-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="24b63-156">RELATED LINKS</span></span>

