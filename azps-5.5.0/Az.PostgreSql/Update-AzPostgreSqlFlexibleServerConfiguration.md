---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 82945caa08fb102c0ef5a05e95586f9c66d3d4a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131010"
---
# <span data-ttu-id="625ff-101">Update-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="625ff-101">Update-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="625ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="625ff-102">SYNOPSIS</span></span>
<span data-ttu-id="625ff-103">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="625ff-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="625ff-104">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzPostgreSqlFlexibleServer]。</span><span class="sxs-lookup"><span data-stu-id="625ff-104">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="625ff-105">句法</span><span class="sxs-lookup"><span data-stu-id="625ff-105">SYNTAX</span></span>

### <span data-ttu-id="625ff-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="625ff-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="625ff-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="625ff-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>]
 [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="625ff-108">說明</span><span class="sxs-lookup"><span data-stu-id="625ff-108">DESCRIPTION</span></span>
<span data-ttu-id="625ff-109">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="625ff-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="625ff-110">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzPostgreSqlFlexibleServer]。</span><span class="sxs-lookup"><span data-stu-id="625ff-110">Use Update-AzPostgreSqlFlexibleServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="625ff-111">示例</span><span class="sxs-lookup"><span data-stu-id="625ff-111">EXAMPLES</span></span>

### <span data-ttu-id="625ff-112">範例1：依名稱 Updatae 指定的 PostgreSql 設定</span><span class="sxs-lookup"><span data-stu-id="625ff-112">Example 1: Updatae specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="625ff-113">這個 Cmdlet 會依名稱更新指定的 PostgreSql 設定。</span><span class="sxs-lookup"><span data-stu-id="625ff-113">This cmdlet updates specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="625ff-114">範例1： Updatae 指定的 PostgreSql 設定（依身分識別）</span><span class="sxs-lookup"><span data-stu-id="625ff-114">Example 1: Updatae specified PostgreSql configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/configurations/work_mem"
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test -Value 8192

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem       8192  4096         system-default  4096-2097151   Integer
```

<span data-ttu-id="625ff-115">這個 Cmdlet 會依身分識別來更新指定的 PostgreSql 設定。</span><span class="sxs-lookup"><span data-stu-id="625ff-115">This cmdlet updates specified PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="625ff-116">參數</span><span class="sxs-lookup"><span data-stu-id="625ff-116">PARAMETERS</span></span>

### <span data-ttu-id="625ff-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="625ff-117">-AsJob</span></span>
<span data-ttu-id="625ff-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="625ff-118">Run the command as a job</span></span>

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

### <span data-ttu-id="625ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="625ff-119">-DefaultProfile</span></span>
<span data-ttu-id="625ff-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="625ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="625ff-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="625ff-121">-InputObject</span></span>
<span data-ttu-id="625ff-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="625ff-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="625ff-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="625ff-123">-Name</span></span>
<span data-ttu-id="625ff-124">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="625ff-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="625ff-125">-NoWait</span></span>
<span data-ttu-id="625ff-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="625ff-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="625ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="625ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="625ff-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-128">The name of the resource group.</span></span>
<span data-ttu-id="625ff-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="625ff-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="625ff-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="625ff-130">-ServerName</span></span>
<span data-ttu-id="625ff-131">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-131">The name of the server.</span></span>

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

### <span data-ttu-id="625ff-132">-來源</span><span class="sxs-lookup"><span data-stu-id="625ff-132">-Source</span></span>
<span data-ttu-id="625ff-133">配置來源。</span><span class="sxs-lookup"><span data-stu-id="625ff-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="625ff-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="625ff-134">-SubscriptionId</span></span>
<span data-ttu-id="625ff-135">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="625ff-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="625ff-136">-值</span><span class="sxs-lookup"><span data-stu-id="625ff-136">-Value</span></span>
<span data-ttu-id="625ff-137">配置的值。</span><span class="sxs-lookup"><span data-stu-id="625ff-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="625ff-138">-確認</span><span class="sxs-lookup"><span data-stu-id="625ff-138">-Confirm</span></span>
<span data-ttu-id="625ff-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="625ff-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="625ff-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="625ff-140">-WhatIf</span></span>
<span data-ttu-id="625ff-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="625ff-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="625ff-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="625ff-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="625ff-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625ff-143">CommonParameters</span></span>
<span data-ttu-id="625ff-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="625ff-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625ff-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="625ff-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625ff-146">輸入</span><span class="sxs-lookup"><span data-stu-id="625ff-146">INPUTS</span></span>

### <span data-ttu-id="625ff-147">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="625ff-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="625ff-148">輸出</span><span class="sxs-lookup"><span data-stu-id="625ff-148">OUTPUTS</span></span>

### <span data-ttu-id="625ff-149">IConfigurationAutoGenerated （PostgreSql）。 Api20200214Preview。</span><span class="sxs-lookup"><span data-stu-id="625ff-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="625ff-150">筆記</span><span class="sxs-lookup"><span data-stu-id="625ff-150">NOTES</span></span>

<span data-ttu-id="625ff-151">別名</span><span class="sxs-lookup"><span data-stu-id="625ff-151">ALIASES</span></span>

<span data-ttu-id="625ff-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="625ff-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="625ff-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="625ff-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="625ff-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="625ff-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="625ff-155">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="625ff-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="625ff-156">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="625ff-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="625ff-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="625ff-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="625ff-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="625ff-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="625ff-161">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="625ff-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="625ff-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="625ff-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="625ff-164">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="625ff-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="625ff-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="625ff-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="625ff-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="625ff-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="625ff-167">RELATED LINKS</span></span>

