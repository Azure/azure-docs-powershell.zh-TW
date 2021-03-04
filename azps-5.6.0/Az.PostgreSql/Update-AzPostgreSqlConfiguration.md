---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: c0af624683e3d12cc1b12c057caa419c5633d45f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902305"
---
# <span data-ttu-id="6a488-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a488-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="6a488-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a488-102">SYNOPSIS</span></span>
<span data-ttu-id="6a488-103">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="6a488-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="6a488-104">如果您想要Update-AzPostgreSqlServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="6a488-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6a488-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a488-105">SYNTAX</span></span>

### <span data-ttu-id="6a488-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6a488-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a488-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6a488-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a488-108">描述</span><span class="sxs-lookup"><span data-stu-id="6a488-108">DESCRIPTION</span></span>
<span data-ttu-id="6a488-109">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="6a488-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="6a488-110">如果您想要Update-AzPostgreSqlServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="6a488-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="6a488-111">例子</span><span class="sxs-lookup"><span data-stu-id="6a488-111">EXAMPLES</span></span>

### <span data-ttu-id="6a488-112">範例 1：根據名稱更新 PostgreSql 組配置</span><span class="sxs-lookup"><span data-stu-id="6a488-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="6a488-113">此 Cmdlet 會更新 PostgreSql 的組名。</span><span class="sxs-lookup"><span data-stu-id="6a488-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="6a488-114">範例 2：根據身分識別更新 PostgreSql 組配置。</span><span class="sxs-lookup"><span data-stu-id="6a488-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="6a488-115">這些 Cmdlet 會根據身分識別更新 PostgreSql 組配置。</span><span class="sxs-lookup"><span data-stu-id="6a488-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="6a488-116">參數</span><span class="sxs-lookup"><span data-stu-id="6a488-116">PARAMETERS</span></span>

### <span data-ttu-id="6a488-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a488-117">-AsJob</span></span>
<span data-ttu-id="6a488-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="6a488-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6a488-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a488-119">-DefaultProfile</span></span>
<span data-ttu-id="6a488-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a488-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a488-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a488-121">-InputObject</span></span>
<span data-ttu-id="6a488-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6a488-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a488-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a488-123">-Name</span></span>
<span data-ttu-id="6a488-124">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="6a488-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="6a488-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6a488-125">-NoWait</span></span>
<span data-ttu-id="6a488-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="6a488-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6a488-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a488-127">-ResourceGroupName</span></span>
<span data-ttu-id="6a488-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-128">The name of the resource group.</span></span>
<span data-ttu-id="6a488-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6a488-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6a488-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a488-130">-ServerName</span></span>
<span data-ttu-id="6a488-131">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-131">The name of the server.</span></span>

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

### <span data-ttu-id="6a488-132">-來源</span><span class="sxs-lookup"><span data-stu-id="6a488-132">-Source</span></span>
<span data-ttu-id="6a488-133">組組的來源。</span><span class="sxs-lookup"><span data-stu-id="6a488-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="6a488-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a488-134">-SubscriptionId</span></span>
<span data-ttu-id="6a488-135">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a488-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6a488-136">-值</span><span class="sxs-lookup"><span data-stu-id="6a488-136">-Value</span></span>
<span data-ttu-id="6a488-137">組名的值。</span><span class="sxs-lookup"><span data-stu-id="6a488-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="6a488-138">-確認</span><span class="sxs-lookup"><span data-stu-id="6a488-138">-Confirm</span></span>
<span data-ttu-id="6a488-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6a488-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a488-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a488-140">-WhatIf</span></span>
<span data-ttu-id="6a488-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6a488-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a488-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a488-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a488-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a488-143">CommonParameters</span></span>
<span data-ttu-id="6a488-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a488-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a488-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a488-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a488-146">輸入</span><span class="sxs-lookup"><span data-stu-id="6a488-146">INPUTS</span></span>

### <span data-ttu-id="6a488-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6a488-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6a488-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6a488-148">OUTPUTS</span></span>

### <span data-ttu-id="6a488-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a488-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="6a488-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6a488-150">NOTES</span></span>

<span data-ttu-id="6a488-151">別名</span><span class="sxs-lookup"><span data-stu-id="6a488-151">ALIASES</span></span>

<span data-ttu-id="6a488-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6a488-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a488-153">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6a488-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a488-154">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6a488-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a488-155">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6a488-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a488-156">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6a488-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6a488-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6a488-159">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6a488-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a488-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6a488-161">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6a488-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6a488-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="6a488-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6a488-164">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6a488-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a488-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6a488-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a488-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6a488-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a488-167">RELATED LINKS</span></span>

