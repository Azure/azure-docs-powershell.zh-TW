---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: 7b1ed42777dcd24460dabb91cf67160dac709aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910450"
---
# <span data-ttu-id="a7e78-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7e78-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="a7e78-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7e78-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e78-103">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="a7e78-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a7e78-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7e78-104">SYNTAX</span></span>

### <span data-ttu-id="a7e78-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="a7e78-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7e78-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a7e78-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a7e78-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e78-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a7e78-108">描述</span><span class="sxs-lookup"><span data-stu-id="a7e78-108">DESCRIPTION</span></span>
<span data-ttu-id="a7e78-109">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="a7e78-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a7e78-110">例子</span><span class="sxs-lookup"><span data-stu-id="a7e78-110">EXAMPLES</span></span>

### <span data-ttu-id="a7e78-111">範例 1：列出指定 MySql 伺服器的所有組配置</span><span class="sxs-lookup"><span data-stu-id="a7e78-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="a7e78-112">此 Cmdlet 會列出指定 MySql 伺服器的所有組配置。</span><span class="sxs-lookup"><span data-stu-id="a7e78-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="a7e78-113">範例 2：根據名稱取得指定的 MySql 組配置</span><span class="sxs-lookup"><span data-stu-id="a7e78-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="a7e78-114">此 Cmdlet 會以名稱指定 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="a7e78-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="a7e78-115">參數</span><span class="sxs-lookup"><span data-stu-id="a7e78-115">PARAMETERS</span></span>

### <span data-ttu-id="a7e78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e78-116">-DefaultProfile</span></span>
<span data-ttu-id="a7e78-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7e78-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e78-118">-InputObject</span></span>
<span data-ttu-id="a7e78-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a7e78-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7e78-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7e78-120">-Name</span></span>
<span data-ttu-id="a7e78-121">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="a7e78-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e78-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e78-122">-ResourceGroupName</span></span>
<span data-ttu-id="a7e78-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-123">The name of the resource group.</span></span>
<span data-ttu-id="a7e78-124">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a7e78-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a7e78-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7e78-125">-ServerName</span></span>
<span data-ttu-id="a7e78-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-126">The name of the server.</span></span>

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

### <span data-ttu-id="a7e78-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7e78-127">-SubscriptionId</span></span>
<span data-ttu-id="a7e78-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7e78-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a7e78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e78-129">CommonParameters</span></span>
<span data-ttu-id="a7e78-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7e78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e78-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7e78-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e78-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a7e78-132">INPUTS</span></span>

### <span data-ttu-id="a7e78-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a7e78-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a7e78-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a7e78-134">OUTPUTS</span></span>

### <span data-ttu-id="a7e78-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7e78-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="a7e78-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a7e78-136">NOTES</span></span>

<span data-ttu-id="a7e78-137">別名</span><span class="sxs-lookup"><span data-stu-id="a7e78-137">ALIASES</span></span>

<span data-ttu-id="a7e78-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a7e78-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7e78-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a7e78-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7e78-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a7e78-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7e78-141">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a7e78-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7e78-142">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a7e78-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a7e78-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a7e78-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a7e78-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7e78-146">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a7e78-147">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a7e78-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a7e78-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a7e78-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a7e78-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a7e78-151">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a7e78-152">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7e78-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a7e78-153">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e78-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a7e78-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7e78-154">RELATED LINKS</span></span>

