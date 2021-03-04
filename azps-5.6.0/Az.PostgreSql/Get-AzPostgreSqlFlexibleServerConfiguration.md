---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 31f99de8a0afaf77345fbdc20782bdd725cb660b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906538"
---
# <span data-ttu-id="a525c-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a525c-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a525c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a525c-102">SYNOPSIS</span></span>
<span data-ttu-id="a525c-103">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="a525c-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a525c-104">語法</span><span class="sxs-lookup"><span data-stu-id="a525c-104">SYNTAX</span></span>

### <span data-ttu-id="a525c-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="a525c-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a525c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a525c-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a525c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a525c-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a525c-108">描述</span><span class="sxs-lookup"><span data-stu-id="a525c-108">DESCRIPTION</span></span>
<span data-ttu-id="a525c-109">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="a525c-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a525c-110">例子</span><span class="sxs-lookup"><span data-stu-id="a525c-110">EXAMPLES</span></span>

### <span data-ttu-id="a525c-111">範例 1：根據名稱取得指定的 PostgreSql 組配置</span><span class="sxs-lookup"><span data-stu-id="a525c-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="a525c-112">此 Cmdlet 會以名稱指定 PostgreSql 組配置。</span><span class="sxs-lookup"><span data-stu-id="a525c-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="a525c-113">範例 2：列出指定 PostgreSql 伺服器的所有組配置</span><span class="sxs-lookup"><span data-stu-id="a525c-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="a525c-114">此 Cmdlet 會列出指定 PostgreSql 伺服器的所有組配置。</span><span class="sxs-lookup"><span data-stu-id="a525c-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="a525c-115">參數</span><span class="sxs-lookup"><span data-stu-id="a525c-115">PARAMETERS</span></span>

### <span data-ttu-id="a525c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a525c-116">-DefaultProfile</span></span>
<span data-ttu-id="a525c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a525c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a525c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a525c-118">-InputObject</span></span>
<span data-ttu-id="a525c-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a525c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a525c-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a525c-120">-Name</span></span>
<span data-ttu-id="a525c-121">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="a525c-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a525c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a525c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a525c-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-123">The name of the resource group.</span></span>
<span data-ttu-id="a525c-124">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a525c-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a525c-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a525c-125">-ServerName</span></span>
<span data-ttu-id="a525c-126">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-126">The name of the server.</span></span>

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

### <span data-ttu-id="a525c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a525c-127">-SubscriptionId</span></span>
<span data-ttu-id="a525c-128">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a525c-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a525c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a525c-129">CommonParameters</span></span>
<span data-ttu-id="a525c-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a525c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a525c-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a525c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a525c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a525c-132">INPUTS</span></span>

### <span data-ttu-id="a525c-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a525c-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a525c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a525c-134">OUTPUTS</span></span>

### <span data-ttu-id="a525c-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a525c-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a525c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a525c-136">NOTES</span></span>

<span data-ttu-id="a525c-137">別名</span><span class="sxs-lookup"><span data-stu-id="a525c-137">ALIASES</span></span>

<span data-ttu-id="a525c-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a525c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a525c-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a525c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a525c-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a525c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a525c-141">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a525c-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a525c-142">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a525c-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a525c-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a525c-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a525c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a525c-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a525c-147">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a525c-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a525c-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="a525c-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a525c-150">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a525c-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a525c-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a525c-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a525c-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a525c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a525c-153">RELATED LINKS</span></span>

