---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 1c7b3c1f64637554745e960fadfe93cb3d87fa84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912817"
---
# <span data-ttu-id="87e50-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87e50-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="87e50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="87e50-102">SYNOPSIS</span></span>
<span data-ttu-id="87e50-103">獲得伺服器防火牆規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="87e50-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="87e50-104">語法</span><span class="sxs-lookup"><span data-stu-id="87e50-104">SYNTAX</span></span>

### <span data-ttu-id="87e50-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="87e50-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87e50-106">獲取</span><span class="sxs-lookup"><span data-stu-id="87e50-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87e50-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87e50-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="87e50-108">描述</span><span class="sxs-lookup"><span data-stu-id="87e50-108">DESCRIPTION</span></span>
<span data-ttu-id="87e50-109">獲得伺服器防火牆規則的資訊。</span><span class="sxs-lookup"><span data-stu-id="87e50-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="87e50-110">例子</span><span class="sxs-lookup"><span data-stu-id="87e50-110">EXAMPLES</span></span>

### <span data-ttu-id="87e50-111">範例 1：在 MariaDB 下列出所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="87e50-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="87e50-112">此命令會列出 MariaDB 下的所有長牆規則。</span><span class="sxs-lookup"><span data-stu-id="87e50-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="87e50-113">範例 2：在 MariaDB 下取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="87e50-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="87e50-114">此命令在 MariaDB 下會獲得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="87e50-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="87e50-115">參數</span><span class="sxs-lookup"><span data-stu-id="87e50-115">PARAMETERS</span></span>

### <span data-ttu-id="87e50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e50-116">-DefaultProfile</span></span>
<span data-ttu-id="87e50-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="87e50-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e50-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87e50-118">-InputObject</span></span>
<span data-ttu-id="87e50-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="87e50-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87e50-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="87e50-120">-Name</span></span>
<span data-ttu-id="87e50-121">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="87e50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e50-122">-ResourceGroupName</span></span>
<span data-ttu-id="87e50-123">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="87e50-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="87e50-124">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="87e50-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="87e50-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="87e50-125">-ServerName</span></span>
<span data-ttu-id="87e50-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-126">The name of the server.</span></span>

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

### <span data-ttu-id="87e50-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87e50-127">-SubscriptionId</span></span>
<span data-ttu-id="87e50-128">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="87e50-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="87e50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e50-129">CommonParameters</span></span>
<span data-ttu-id="87e50-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="87e50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e50-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87e50-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e50-132">輸入</span><span class="sxs-lookup"><span data-stu-id="87e50-132">INPUTS</span></span>

### <span data-ttu-id="87e50-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="87e50-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="87e50-134">輸出</span><span class="sxs-lookup"><span data-stu-id="87e50-134">OUTPUTS</span></span>

### <span data-ttu-id="87e50-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87e50-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="87e50-136">筆記</span><span class="sxs-lookup"><span data-stu-id="87e50-136">NOTES</span></span>

<span data-ttu-id="87e50-137">別名</span><span class="sxs-lookup"><span data-stu-id="87e50-137">ALIASES</span></span>

<span data-ttu-id="87e50-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="87e50-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87e50-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="87e50-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87e50-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="87e50-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87e50-141">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="87e50-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87e50-142">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="87e50-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="87e50-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="87e50-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="87e50-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87e50-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="87e50-147">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="87e50-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="87e50-148">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="87e50-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="87e50-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="87e50-150">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="87e50-151">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="87e50-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="87e50-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e50-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="87e50-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="87e50-153">RELATED LINKS</span></span>

