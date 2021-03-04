---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 97b16f3930eda94e69c3528432ee54927c3eef7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901694"
---
# <span data-ttu-id="dd292-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd292-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="dd292-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd292-102">SYNOPSIS</span></span>
<span data-ttu-id="dd292-103">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="dd292-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="dd292-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd292-104">SYNTAX</span></span>

### <span data-ttu-id="dd292-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="dd292-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd292-106">獲取</span><span class="sxs-lookup"><span data-stu-id="dd292-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dd292-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd292-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd292-108">描述</span><span class="sxs-lookup"><span data-stu-id="dd292-108">DESCRIPTION</span></span>
<span data-ttu-id="dd292-109">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="dd292-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="dd292-110">例子</span><span class="sxs-lookup"><span data-stu-id="dd292-110">EXAMPLES</span></span>

### <span data-ttu-id="dd292-111">範例 1：在 PostgreSql 伺服器中列出所有組配置</span><span class="sxs-lookup"><span data-stu-id="dd292-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="dd292-112">此 Cmdlet 會列出指定 PostgreSql 伺服器的所有組配置。</span><span class="sxs-lookup"><span data-stu-id="dd292-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="dd292-113">範例 2：根據名稱取得指定的 PostgreSql 組配置</span><span class="sxs-lookup"><span data-stu-id="dd292-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="dd292-114">此 Cmdlet 會以名稱指定 PostgreSql 組配置。</span><span class="sxs-lookup"><span data-stu-id="dd292-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="dd292-115">參數</span><span class="sxs-lookup"><span data-stu-id="dd292-115">PARAMETERS</span></span>

### <span data-ttu-id="dd292-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd292-116">-DefaultProfile</span></span>
<span data-ttu-id="dd292-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd292-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd292-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd292-118">-InputObject</span></span>
<span data-ttu-id="dd292-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dd292-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dd292-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd292-120">-Name</span></span>
<span data-ttu-id="dd292-121">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="dd292-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="dd292-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd292-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd292-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-123">The name of the resource group.</span></span>
<span data-ttu-id="dd292-124">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dd292-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dd292-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dd292-125">-ServerName</span></span>
<span data-ttu-id="dd292-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-126">The name of the server.</span></span>

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

### <span data-ttu-id="dd292-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd292-127">-SubscriptionId</span></span>
<span data-ttu-id="dd292-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd292-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dd292-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd292-129">CommonParameters</span></span>
<span data-ttu-id="dd292-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd292-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd292-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd292-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd292-132">輸入</span><span class="sxs-lookup"><span data-stu-id="dd292-132">INPUTS</span></span>

### <span data-ttu-id="dd292-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dd292-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="dd292-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dd292-134">OUTPUTS</span></span>

### <span data-ttu-id="dd292-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd292-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="dd292-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dd292-136">NOTES</span></span>

<span data-ttu-id="dd292-137">別名</span><span class="sxs-lookup"><span data-stu-id="dd292-137">ALIASES</span></span>

<span data-ttu-id="dd292-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="dd292-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd292-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dd292-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd292-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dd292-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd292-141">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="dd292-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd292-142">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dd292-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dd292-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dd292-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="dd292-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd292-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dd292-147">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dd292-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dd292-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="dd292-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dd292-150">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dd292-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd292-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dd292-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd292-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dd292-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd292-153">RELATED LINKS</span></span>

