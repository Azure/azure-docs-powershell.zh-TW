---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 98e476b2a1732d2c984d200265d817c3ff6d71a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906118"
---
# <span data-ttu-id="b92a6-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b92a6-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="b92a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b92a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b92a6-103">更新 MySQL 彈性伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="b92a6-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="b92a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="b92a6-104">SYNTAX</span></span>

### <span data-ttu-id="b92a6-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b92a6-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b92a6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b92a6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b92a6-107">描述</span><span class="sxs-lookup"><span data-stu-id="b92a6-107">DESCRIPTION</span></span>
<span data-ttu-id="b92a6-108">更新 MySQL 彈性伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="b92a6-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="b92a6-109">例子</span><span class="sxs-lookup"><span data-stu-id="b92a6-109">EXAMPLES</span></span>

### <span data-ttu-id="b92a6-110">範例 1：根據名稱更新 MySql 組配置</span><span class="sxs-lookup"><span data-stu-id="b92a6-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="b92a6-111">此 Cmdlet 會更新 MySql 的組名。</span><span class="sxs-lookup"><span data-stu-id="b92a6-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="b92a6-112">範例 2：根據身分識別更新 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="b92a6-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="b92a6-113">這些 Cmdlet 會根據身分識別更新 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="b92a6-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="b92a6-114">參數</span><span class="sxs-lookup"><span data-stu-id="b92a6-114">PARAMETERS</span></span>

### <span data-ttu-id="b92a6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b92a6-115">-AsJob</span></span>
<span data-ttu-id="b92a6-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b92a6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b92a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92a6-117">-DefaultProfile</span></span>
<span data-ttu-id="b92a6-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b92a6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b92a6-119">-InputObject</span></span>
<span data-ttu-id="b92a6-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b92a6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b92a6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b92a6-121">-Name</span></span>
<span data-ttu-id="b92a6-122">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="b92a6-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="b92a6-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b92a6-123">-NoWait</span></span>
<span data-ttu-id="b92a6-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b92a6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b92a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b92a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="b92a6-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-126">The name of the resource group.</span></span>
<span data-ttu-id="b92a6-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b92a6-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b92a6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b92a6-128">-ServerName</span></span>
<span data-ttu-id="b92a6-129">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-129">The name of the server.</span></span>

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

### <span data-ttu-id="b92a6-130">-來源</span><span class="sxs-lookup"><span data-stu-id="b92a6-130">-Source</span></span>
<span data-ttu-id="b92a6-131">更新值的來源。</span><span class="sxs-lookup"><span data-stu-id="b92a6-131">The source of the updating value.</span></span>
<span data-ttu-id="b92a6-132">預設值為使用者重寫</span><span class="sxs-lookup"><span data-stu-id="b92a6-132">The default value is user-override</span></span>

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

### <span data-ttu-id="b92a6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b92a6-133">-SubscriptionId</span></span>
<span data-ttu-id="b92a6-134">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b92a6-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b92a6-135">-值</span><span class="sxs-lookup"><span data-stu-id="b92a6-135">-Value</span></span>
<span data-ttu-id="b92a6-136">組名的值。</span><span class="sxs-lookup"><span data-stu-id="b92a6-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="b92a6-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b92a6-137">-Confirm</span></span>
<span data-ttu-id="b92a6-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b92a6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b92a6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b92a6-139">-WhatIf</span></span>
<span data-ttu-id="b92a6-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b92a6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b92a6-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b92a6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b92a6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92a6-142">CommonParameters</span></span>
<span data-ttu-id="b92a6-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b92a6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92a6-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b92a6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92a6-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b92a6-145">INPUTS</span></span>

### <span data-ttu-id="b92a6-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b92a6-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b92a6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b92a6-147">OUTPUTS</span></span>

### <span data-ttu-id="b92a6-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b92a6-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="b92a6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b92a6-149">NOTES</span></span>

<span data-ttu-id="b92a6-150">別名</span><span class="sxs-lookup"><span data-stu-id="b92a6-150">ALIASES</span></span>

<span data-ttu-id="b92a6-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b92a6-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b92a6-152">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b92a6-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b92a6-153">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b92a6-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b92a6-154">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b92a6-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b92a6-155">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b92a6-156">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b92a6-157">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b92a6-158">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b92a6-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b92a6-159">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b92a6-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b92a6-161">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b92a6-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b92a6-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="b92a6-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b92a6-164">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b92a6-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b92a6-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b92a6-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b92a6-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b92a6-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="b92a6-167">RELATED LINKS</span></span>

