---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlConfiguration.md
ms.openlocfilehash: e1b0ea3d07a7504e75f8bd6143820c52e73d9cf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437344"
---
# <span data-ttu-id="ed57c-101">Update-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed57c-101">Update-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="ed57c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed57c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed57c-103">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="ed57c-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="ed57c-104">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzPostgreSqlServer]。</span><span class="sxs-lookup"><span data-stu-id="ed57c-104">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="ed57c-105">句法</span><span class="sxs-lookup"><span data-stu-id="ed57c-105">SYNTAX</span></span>

### <span data-ttu-id="ed57c-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="ed57c-106">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed57c-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ed57c-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed57c-108">說明</span><span class="sxs-lookup"><span data-stu-id="ed57c-108">DESCRIPTION</span></span>
<span data-ttu-id="ed57c-109">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="ed57c-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="ed57c-110">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzPostgreSqlServer]。</span><span class="sxs-lookup"><span data-stu-id="ed57c-110">Use Update-AzPostgreSqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="ed57c-111">示例</span><span class="sxs-lookup"><span data-stu-id="ed57c-111">EXAMPLES</span></span>

### <span data-ttu-id="ed57c-112">範例1：依名稱更新 PostgreSql 設定</span><span class="sxs-lookup"><span data-stu-id="ed57c-112">Example 1: Update PostgreSql configuration by name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlConfiguration -Name intervalstyle -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -Value SQL_STANDARD

Name          Value
----          -----
intervalstyle SQL_STANDARD
```

<span data-ttu-id="ed57c-113">這個 Cmdlet 會依名稱更新 PostgreSql 設定。</span><span class="sxs-lookup"><span data-stu-id="ed57c-113">This cmdlet updates PostgreSql configuration by name.</span></span>

### <span data-ttu-id="ed57c-114">範例2：依身分識別來更新 PostgreSql 設定。</span><span class="sxs-lookup"><span data-stu-id="ed57c-114">Example 2: Update PostgreSql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/configurations/deadlock_timeout"
PS C:\> Update-AzPostgreSqlConfiguration -InputObject $ID -Value 2000

Name             Value
----             -----
deadlock_timeout 2000
```

<span data-ttu-id="ed57c-115">這些 Cmdlet 會依身分識別來更新 PostgreSql 設定。</span><span class="sxs-lookup"><span data-stu-id="ed57c-115">These cmdlets update PostgreSql configuration by identity.</span></span>

## <span data-ttu-id="ed57c-116">參數</span><span class="sxs-lookup"><span data-stu-id="ed57c-116">PARAMETERS</span></span>

### <span data-ttu-id="ed57c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed57c-117">-AsJob</span></span>
<span data-ttu-id="ed57c-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ed57c-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ed57c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed57c-119">-DefaultProfile</span></span>
<span data-ttu-id="ed57c-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed57c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed57c-121">-InputObject</span></span>
<span data-ttu-id="ed57c-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ed57c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ed57c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed57c-123">-Name</span></span>
<span data-ttu-id="ed57c-124">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-124">The name of the server configuration.</span></span>

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

### <span data-ttu-id="ed57c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed57c-125">-NoWait</span></span>
<span data-ttu-id="ed57c-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ed57c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed57c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed57c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed57c-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-128">The name of the resource group.</span></span>
<span data-ttu-id="ed57c-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ed57c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ed57c-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed57c-130">-ServerName</span></span>
<span data-ttu-id="ed57c-131">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-131">The name of the server.</span></span>

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

### <span data-ttu-id="ed57c-132">-來源</span><span class="sxs-lookup"><span data-stu-id="ed57c-132">-Source</span></span>
<span data-ttu-id="ed57c-133">配置來源。</span><span class="sxs-lookup"><span data-stu-id="ed57c-133">Source of the configuration.</span></span>

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

### <span data-ttu-id="ed57c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed57c-134">-SubscriptionId</span></span>
<span data-ttu-id="ed57c-135">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ed57c-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ed57c-136">-值</span><span class="sxs-lookup"><span data-stu-id="ed57c-136">-Value</span></span>
<span data-ttu-id="ed57c-137">配置的值。</span><span class="sxs-lookup"><span data-stu-id="ed57c-137">Value of the configuration.</span></span>

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

### <span data-ttu-id="ed57c-138">-確認</span><span class="sxs-lookup"><span data-stu-id="ed57c-138">-Confirm</span></span>
<span data-ttu-id="ed57c-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed57c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed57c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed57c-140">-WhatIf</span></span>
<span data-ttu-id="ed57c-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed57c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed57c-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed57c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed57c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed57c-143">CommonParameters</span></span>
<span data-ttu-id="ed57c-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed57c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed57c-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ed57c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed57c-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ed57c-146">INPUTS</span></span>

### <span data-ttu-id="ed57c-147">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="ed57c-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="ed57c-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ed57c-148">OUTPUTS</span></span>

### <span data-ttu-id="ed57c-149">IConfiguration （PostgreSql）。 Api20171201。</span><span class="sxs-lookup"><span data-stu-id="ed57c-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="ed57c-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ed57c-150">NOTES</span></span>

<span data-ttu-id="ed57c-151">別名</span><span class="sxs-lookup"><span data-stu-id="ed57c-151">ALIASES</span></span>

<span data-ttu-id="ed57c-152">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ed57c-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed57c-153">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ed57c-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed57c-154">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ed57c-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed57c-155">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ed57c-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed57c-156">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ed57c-157">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ed57c-158">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ed57c-159">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ed57c-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed57c-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ed57c-161">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ed57c-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ed57c-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="ed57c-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ed57c-164">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ed57c-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed57c-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ed57c-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed57c-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ed57c-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed57c-167">RELATED LINKS</span></span>

