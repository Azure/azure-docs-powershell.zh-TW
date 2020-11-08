---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140355"
---
# <span data-ttu-id="2bfe2-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2bfe2-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="2bfe2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bfe2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfe2-103">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="2bfe2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bfe2-104">SYNTAX</span></span>

### <span data-ttu-id="2bfe2-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="2bfe2-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2bfe2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2bfe2-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2bfe2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2bfe2-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2bfe2-108">說明</span><span class="sxs-lookup"><span data-stu-id="2bfe2-108">DESCRIPTION</span></span>
<span data-ttu-id="2bfe2-109">取得伺服器防火牆規則的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="2bfe2-110">示例</span><span class="sxs-lookup"><span data-stu-id="2bfe2-110">EXAMPLES</span></span>

### <span data-ttu-id="2bfe2-111">範例1：列出 MariaDB 下的所有防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2bfe2-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="2bfe2-112">這個命令會列出 MariaDB 下的所有 girewall 規則。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="2bfe2-113">範例2：在 MariaDB 下取得防火牆規則</span><span class="sxs-lookup"><span data-stu-id="2bfe2-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="2bfe2-114">這個命令會在 MariaDB 下取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="2bfe2-115">參數</span><span class="sxs-lookup"><span data-stu-id="2bfe2-115">PARAMETERS</span></span>

### <span data-ttu-id="2bfe2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bfe2-116">-DefaultProfile</span></span>
<span data-ttu-id="2bfe2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bfe2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bfe2-118">-InputObject</span></span>
<span data-ttu-id="2bfe2-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2bfe2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2bfe2-120">-Name</span></span>
<span data-ttu-id="2bfe2-121">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="2bfe2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bfe2-122">-ResourceGroupName</span></span>
<span data-ttu-id="2bfe2-123">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2bfe2-124">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2bfe2-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2bfe2-125">-ServerName</span></span>
<span data-ttu-id="2bfe2-126">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-126">The name of the server.</span></span>

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

### <span data-ttu-id="2bfe2-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2bfe2-127">-SubscriptionId</span></span>
<span data-ttu-id="2bfe2-128">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2bfe2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfe2-129">CommonParameters</span></span>
<span data-ttu-id="2bfe2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfe2-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfe2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2bfe2-132">INPUTS</span></span>

### <span data-ttu-id="2bfe2-133">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="2bfe2-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="2bfe2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2bfe2-134">OUTPUTS</span></span>

### <span data-ttu-id="2bfe2-135">IFirewallRule （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="2bfe2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2bfe2-136">NOTES</span></span>

<span data-ttu-id="2bfe2-137">別名</span><span class="sxs-lookup"><span data-stu-id="2bfe2-137">ALIASES</span></span>

<span data-ttu-id="2bfe2-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2bfe2-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2bfe2-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2bfe2-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2bfe2-141">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2bfe2-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2bfe2-142">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2bfe2-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2bfe2-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2bfe2-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2bfe2-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2bfe2-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2bfe2-147">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2bfe2-148">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2bfe2-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2bfe2-150">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2bfe2-151">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="2bfe2-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="2bfe2-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2bfe2-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bfe2-153">RELATED LINKS</span></span>

