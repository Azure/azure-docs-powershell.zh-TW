---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126299"
---
# <span data-ttu-id="dfc34-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dfc34-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="dfc34-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dfc34-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc34-103">取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="dfc34-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="dfc34-104">句法</span><span class="sxs-lookup"><span data-stu-id="dfc34-104">SYNTAX</span></span>

### <span data-ttu-id="dfc34-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="dfc34-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dfc34-106">獲取</span><span class="sxs-lookup"><span data-stu-id="dfc34-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dfc34-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dfc34-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc34-108">說明</span><span class="sxs-lookup"><span data-stu-id="dfc34-108">DESCRIPTION</span></span>
<span data-ttu-id="dfc34-109">取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="dfc34-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="dfc34-110">示例</span><span class="sxs-lookup"><span data-stu-id="dfc34-110">EXAMPLES</span></span>

### <span data-ttu-id="dfc34-111">範例1：列出指定 PostgreSql 伺服器中的所有虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="dfc34-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="dfc34-112">這個 Cmdlet 會列出指定 PostgreSql 伺服器中的所有虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="dfc34-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="dfc34-113">範例2：依名稱取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="dfc34-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="dfc34-114">這個 Cmdlet 會依名稱取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="dfc34-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="dfc34-115">範例3：依身分識別取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="dfc34-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="dfc34-116">這個 Cmdlet 透過身分識別來取得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="dfc34-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="dfc34-117">參數</span><span class="sxs-lookup"><span data-stu-id="dfc34-117">PARAMETERS</span></span>

### <span data-ttu-id="dfc34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc34-118">-DefaultProfile</span></span>
<span data-ttu-id="dfc34-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc34-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfc34-120">-InputObject</span></span>
<span data-ttu-id="dfc34-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dfc34-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dfc34-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="dfc34-122">-Name</span></span>
<span data-ttu-id="dfc34-123">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc34-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfc34-124">-PassThru</span></span>
<span data-ttu-id="dfc34-125">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="dfc34-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dfc34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc34-126">-ResourceGroupName</span></span>
<span data-ttu-id="dfc34-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-127">The name of the resource group.</span></span>
<span data-ttu-id="dfc34-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dfc34-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dfc34-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dfc34-129">-ServerName</span></span>
<span data-ttu-id="dfc34-130">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-130">The name of the server.</span></span>

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

### <span data-ttu-id="dfc34-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfc34-131">-SubscriptionId</span></span>
<span data-ttu-id="dfc34-132">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="dfc34-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dfc34-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc34-133">CommonParameters</span></span>
<span data-ttu-id="dfc34-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dfc34-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc34-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dfc34-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc34-136">輸入</span><span class="sxs-lookup"><span data-stu-id="dfc34-136">INPUTS</span></span>

### <span data-ttu-id="dfc34-137">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="dfc34-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="dfc34-138">輸出</span><span class="sxs-lookup"><span data-stu-id="dfc34-138">OUTPUTS</span></span>

### <span data-ttu-id="dfc34-139">IVirtualNetworkRule （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="dfc34-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="dfc34-140">筆記</span><span class="sxs-lookup"><span data-stu-id="dfc34-140">NOTES</span></span>

<span data-ttu-id="dfc34-141">別名</span><span class="sxs-lookup"><span data-stu-id="dfc34-141">ALIASES</span></span>

<span data-ttu-id="dfc34-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dfc34-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfc34-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dfc34-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfc34-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dfc34-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfc34-145">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dfc34-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfc34-146">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dfc34-147">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dfc34-148">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dfc34-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="dfc34-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfc34-150">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dfc34-151">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dfc34-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dfc34-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="dfc34-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dfc34-154">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dfc34-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfc34-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dfc34-156">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfc34-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dfc34-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="dfc34-157">RELATED LINKS</span></span>

