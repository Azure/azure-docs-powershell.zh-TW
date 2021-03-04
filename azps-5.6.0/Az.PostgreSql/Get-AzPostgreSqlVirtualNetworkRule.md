---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: e5eb6e239ef49dccf610be866a0f9711245d5ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910685"
---
# <span data-ttu-id="56044-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56044-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="56044-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56044-102">SYNOPSIS</span></span>
<span data-ttu-id="56044-103">獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="56044-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="56044-104">語法</span><span class="sxs-lookup"><span data-stu-id="56044-104">SYNTAX</span></span>

### <span data-ttu-id="56044-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="56044-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="56044-106">獲取</span><span class="sxs-lookup"><span data-stu-id="56044-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="56044-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56044-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="56044-108">描述</span><span class="sxs-lookup"><span data-stu-id="56044-108">DESCRIPTION</span></span>
<span data-ttu-id="56044-109">獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="56044-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="56044-110">例子</span><span class="sxs-lookup"><span data-stu-id="56044-110">EXAMPLES</span></span>

### <span data-ttu-id="56044-111">範例 1：列出指定 PostgreSql 伺服器中所有的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="56044-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="56044-112">此 Cmdlet 會列出指定 PostgreSql 伺服器中所有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="56044-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="56044-113">範例 2：依名稱取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="56044-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="56044-114">此 Cmdlet 會依名稱獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="56044-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="56044-115">範例 3：依身分識別取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="56044-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="56044-116">此 Cmdlet 會依身分識別獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="56044-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="56044-117">參數</span><span class="sxs-lookup"><span data-stu-id="56044-117">PARAMETERS</span></span>

### <span data-ttu-id="56044-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56044-118">-DefaultProfile</span></span>
<span data-ttu-id="56044-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56044-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56044-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56044-120">-InputObject</span></span>
<span data-ttu-id="56044-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="56044-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56044-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="56044-122">-Name</span></span>
<span data-ttu-id="56044-123">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="56044-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56044-124">-PassThru</span></span>
<span data-ttu-id="56044-125">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="56044-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="56044-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56044-126">-ResourceGroupName</span></span>
<span data-ttu-id="56044-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-127">The name of the resource group.</span></span>
<span data-ttu-id="56044-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="56044-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56044-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56044-129">-ServerName</span></span>
<span data-ttu-id="56044-130">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-130">The name of the server.</span></span>

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

### <span data-ttu-id="56044-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56044-131">-SubscriptionId</span></span>
<span data-ttu-id="56044-132">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56044-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56044-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56044-133">CommonParameters</span></span>
<span data-ttu-id="56044-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56044-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56044-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56044-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56044-136">輸入</span><span class="sxs-lookup"><span data-stu-id="56044-136">INPUTS</span></span>

### <span data-ttu-id="56044-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="56044-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="56044-138">輸出</span><span class="sxs-lookup"><span data-stu-id="56044-138">OUTPUTS</span></span>

### <span data-ttu-id="56044-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56044-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="56044-140">筆記</span><span class="sxs-lookup"><span data-stu-id="56044-140">NOTES</span></span>

<span data-ttu-id="56044-141">別名</span><span class="sxs-lookup"><span data-stu-id="56044-141">ALIASES</span></span>

<span data-ttu-id="56044-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="56044-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56044-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="56044-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56044-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="56044-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56044-145">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="56044-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56044-146">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="56044-147">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="56044-148">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="56044-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="56044-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56044-150">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="56044-151">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56044-152">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="56044-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="56044-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="56044-154">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="56044-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="56044-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="56044-156">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="56044-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="56044-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="56044-157">RELATED LINKS</span></span>

