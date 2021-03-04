---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 30e361d77f3c3b738703e1dde075ccbabc38b0b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908885"
---
# <span data-ttu-id="d6157-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d6157-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="d6157-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6157-102">SYNOPSIS</span></span>
<span data-ttu-id="d6157-103">獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d6157-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="d6157-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6157-104">SYNTAX</span></span>

### <span data-ttu-id="d6157-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="d6157-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d6157-106">獲取</span><span class="sxs-lookup"><span data-stu-id="d6157-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="d6157-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d6157-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="d6157-108">描述</span><span class="sxs-lookup"><span data-stu-id="d6157-108">DESCRIPTION</span></span>
<span data-ttu-id="d6157-109">獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d6157-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="d6157-110">例子</span><span class="sxs-lookup"><span data-stu-id="d6157-110">EXAMPLES</span></span>

### <span data-ttu-id="d6157-111">範例 1：列出指定 MySql 伺服器中所有的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="d6157-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="d6157-112">此 Cmdlet 會列出指定的 MySql 伺服器中所有的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d6157-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="d6157-113">範例 2：依名稱取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="d6157-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="d6157-114">此 Cmdlet 會依名稱獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d6157-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="d6157-115">範例 3：依身分識別取得虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="d6157-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="d6157-116">此 Cmdlet 會依身分識別獲得虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="d6157-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="d6157-117">參數</span><span class="sxs-lookup"><span data-stu-id="d6157-117">PARAMETERS</span></span>

### <span data-ttu-id="d6157-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6157-118">-DefaultProfile</span></span>
<span data-ttu-id="d6157-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6157-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6157-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6157-120">-InputObject</span></span>
<span data-ttu-id="d6157-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d6157-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6157-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6157-122">-Name</span></span>
<span data-ttu-id="d6157-123">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d6157-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6157-124">-PassThru</span></span>
<span data-ttu-id="d6157-125">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="d6157-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d6157-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6157-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6157-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-127">The name of the resource group.</span></span>
<span data-ttu-id="d6157-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d6157-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d6157-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d6157-129">-ServerName</span></span>
<span data-ttu-id="d6157-130">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-130">The name of the server.</span></span>

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

### <span data-ttu-id="d6157-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6157-131">-SubscriptionId</span></span>
<span data-ttu-id="d6157-132">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6157-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d6157-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6157-133">CommonParameters</span></span>
<span data-ttu-id="d6157-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6157-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6157-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6157-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6157-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d6157-136">INPUTS</span></span>

### <span data-ttu-id="d6157-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d6157-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d6157-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d6157-138">OUTPUTS</span></span>

### <span data-ttu-id="d6157-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d6157-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="d6157-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d6157-140">NOTES</span></span>

<span data-ttu-id="d6157-141">別名</span><span class="sxs-lookup"><span data-stu-id="d6157-141">ALIASES</span></span>

<span data-ttu-id="d6157-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d6157-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6157-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d6157-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6157-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d6157-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6157-145">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d6157-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d6157-146">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d6157-147">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d6157-148">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d6157-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="d6157-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d6157-150">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d6157-151">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d6157-152">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d6157-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d6157-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="d6157-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d6157-155">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d6157-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6157-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d6157-157">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6157-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d6157-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6157-158">RELATED LINKS</span></span>

