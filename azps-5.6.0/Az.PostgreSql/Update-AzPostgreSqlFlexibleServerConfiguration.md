---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: e45d342f7bb02034b2adf0473e6d4d1eb3c2b370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907586"
---
# <span data-ttu-id="9c76d-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="9c76d-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="9c76d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c76d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c76d-103">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="9c76d-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="9c76d-104">如果您想要Update-AzPostgreSqlFlexibleServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="9c76d-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="9c76d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9c76d-105">SYNTAX</span></span>

### <span data-ttu-id="9c76d-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9c76d-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c76d-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9c76d-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c76d-108">描述</span><span class="sxs-lookup"><span data-stu-id="9c76d-108">DESCRIPTION</span></span>
<span data-ttu-id="9c76d-109">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="9c76d-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="9c76d-110">如果您想要Update-AzPostgreSqlFlexibleServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="9c76d-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="9c76d-111">例子</span><span class="sxs-lookup"><span data-stu-id="9c76d-111">EXAMPLES</span></span>

### <span data-ttu-id="9c76d-112">範例 1：更新指定的 PostgreSql 組名</span><span class="sxs-lookup"><span data-stu-id="9c76d-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="9c76d-113">此 Cmdlet 會更新指定的 PostgreSql 組名。</span><span class="sxs-lookup"><span data-stu-id="9c76d-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="9c76d-114">範例 1：根據身分識別更新指定的 PostgreSql 組配置</span><span class="sxs-lookup"><span data-stu-id="9c76d-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="9c76d-115">此 Cmdlet 會根據身分識別更新指定的 PostgreSql 組配置。</span><span class="sxs-lookup"><span data-stu-id="9c76d-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="9c76d-116">參數</span><span class="sxs-lookup"><span data-stu-id="9c76d-116">PARAMETERS</span></span>

### <span data-ttu-id="9c76d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c76d-117">-AsJob</span></span>
<span data-ttu-id="9c76d-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="9c76d-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9c76d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c76d-119">-DefaultProfile</span></span>
<span data-ttu-id="9c76d-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c76d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c76d-121">-InputObject</span></span>
<span data-ttu-id="9c76d-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9c76d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c76d-123">-Name</span></span>
<span data-ttu-id="9c76d-124">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="9c76d-124">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9c76d-125">-NoWait</span></span>
<span data-ttu-id="9c76d-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="9c76d-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9c76d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c76d-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c76d-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-128">The name of the resource group.</span></span>
<span data-ttu-id="9c76d-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9c76d-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c76d-130">-ServerName</span></span>
<span data-ttu-id="9c76d-131">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-132">-來源</span><span class="sxs-lookup"><span data-stu-id="9c76d-132">-Source</span></span>
<span data-ttu-id="9c76d-133">組組的來源。</span><span class="sxs-lookup"><span data-stu-id="9c76d-133">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c76d-134">-SubscriptionId</span></span>
<span data-ttu-id="9c76d-135">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c76d-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-136">-值</span><span class="sxs-lookup"><span data-stu-id="9c76d-136">-Value</span></span>
<span data-ttu-id="9c76d-137">組名的值。</span><span class="sxs-lookup"><span data-stu-id="9c76d-137">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-138">-確認</span><span class="sxs-lookup"><span data-stu-id="9c76d-138">-Confirm</span></span>
<span data-ttu-id="9c76d-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9c76d-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c76d-140">-WhatIf</span></span>
<span data-ttu-id="9c76d-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c76d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c76d-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c76d-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c76d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c76d-143">CommonParameters</span></span>
<span data-ttu-id="9c76d-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c76d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c76d-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c76d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c76d-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9c76d-146">INPUTS</span></span>

### <span data-ttu-id="9c76d-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9c76d-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9c76d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="9c76d-148">OUTPUTS</span></span>

### <span data-ttu-id="9c76d-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="9c76d-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="9c76d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="9c76d-150">NOTES</span></span>

<span data-ttu-id="9c76d-151">別名</span><span class="sxs-lookup"><span data-stu-id="9c76d-151">ALIASES</span></span>

<span data-ttu-id="9c76d-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9c76d-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c76d-153">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9c76d-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c76d-154">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9c76d-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c76d-155">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9c76d-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c76d-156">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9c76d-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9c76d-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9c76d-159">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="9c76d-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c76d-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9c76d-161">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9c76d-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9c76d-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="9c76d-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9c76d-164">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9c76d-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c76d-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9c76d-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c76d-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9c76d-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c76d-167">RELATED LINKS</span></span>

