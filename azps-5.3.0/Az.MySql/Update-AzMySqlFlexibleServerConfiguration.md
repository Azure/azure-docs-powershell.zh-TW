---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 7e3c3855fb36d1dbc96b399d5348f033ca74908e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436414"
---
# <span data-ttu-id="d374f-101">Update-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d374f-101">Update-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="d374f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d374f-102">SYNOPSIS</span></span>
<span data-ttu-id="d374f-103">更新有關 MySQL 靈活伺服器設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="d374f-103">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="d374f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d374f-104">SYNTAX</span></span>

### <span data-ttu-id="d374f-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="d374f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d374f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d374f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d374f-107">說明</span><span class="sxs-lookup"><span data-stu-id="d374f-107">DESCRIPTION</span></span>
<span data-ttu-id="d374f-108">更新有關 MySQL 靈活伺服器設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="d374f-108">Updates information about a configuration of a MySQL flexible server.</span></span>

## <span data-ttu-id="d374f-109">示例</span><span class="sxs-lookup"><span data-stu-id="d374f-109">EXAMPLES</span></span>

### <span data-ttu-id="d374f-110">範例1：依名稱更新 MySql 配置</span><span class="sxs-lookup"><span data-stu-id="d374f-110">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
net_retry_count 15    10            user-override  1-4294967295   Integer
```

<span data-ttu-id="d374f-111">這個 Cmdlet 會依名稱更新 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="d374f-111">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="d374f-112">範例2：依身分識別來更新 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="d374f-112">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlFlexibleServer -InputObject $ID -Value 150

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   150    28800         system-default   1-31536000   Integer
```

<span data-ttu-id="d374f-113">這些 Cmdlet 會依身分識別來更新 MySql 設定。</span><span class="sxs-lookup"><span data-stu-id="d374f-113">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="d374f-114">參數</span><span class="sxs-lookup"><span data-stu-id="d374f-114">PARAMETERS</span></span>

### <span data-ttu-id="d374f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d374f-115">-AsJob</span></span>
<span data-ttu-id="d374f-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="d374f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d374f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d374f-117">-DefaultProfile</span></span>
<span data-ttu-id="d374f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d374f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d374f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d374f-119">-InputObject</span></span>
<span data-ttu-id="d374f-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d374f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d374f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d374f-121">-Name</span></span>
<span data-ttu-id="d374f-122">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="d374f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d374f-123">-NoWait</span></span>
<span data-ttu-id="d374f-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="d374f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d374f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d374f-125">-ResourceGroupName</span></span>
<span data-ttu-id="d374f-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-126">The name of the resource group.</span></span>
<span data-ttu-id="d374f-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d374f-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d374f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d374f-128">-ServerName</span></span>
<span data-ttu-id="d374f-129">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-129">The name of the server.</span></span>

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

### <span data-ttu-id="d374f-130">-來源</span><span class="sxs-lookup"><span data-stu-id="d374f-130">-Source</span></span>
<span data-ttu-id="d374f-131">更新值的來源。</span><span class="sxs-lookup"><span data-stu-id="d374f-131">The source of the updating value.</span></span>
<span data-ttu-id="d374f-132">預設值為 user override</span><span class="sxs-lookup"><span data-stu-id="d374f-132">The default value is user-override</span></span>

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

### <span data-ttu-id="d374f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d374f-133">-SubscriptionId</span></span>
<span data-ttu-id="d374f-134">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="d374f-134">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d374f-135">-值</span><span class="sxs-lookup"><span data-stu-id="d374f-135">-Value</span></span>
<span data-ttu-id="d374f-136">配置的值。</span><span class="sxs-lookup"><span data-stu-id="d374f-136">Value of the configuration.</span></span>

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

### <span data-ttu-id="d374f-137">-確認</span><span class="sxs-lookup"><span data-stu-id="d374f-137">-Confirm</span></span>
<span data-ttu-id="d374f-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d374f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d374f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d374f-139">-WhatIf</span></span>
<span data-ttu-id="d374f-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d374f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d374f-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d374f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d374f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d374f-142">CommonParameters</span></span>
<span data-ttu-id="d374f-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d374f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d374f-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d374f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d374f-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d374f-145">INPUTS</span></span>

### <span data-ttu-id="d374f-146">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d374f-146">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d374f-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d374f-147">OUTPUTS</span></span>

### <span data-ttu-id="d374f-148">IConfigurationAutoGenerated 中的 Api20200701Preview （）。</span><span class="sxs-lookup"><span data-stu-id="d374f-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="d374f-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d374f-149">NOTES</span></span>

<span data-ttu-id="d374f-150">別名</span><span class="sxs-lookup"><span data-stu-id="d374f-150">ALIASES</span></span>

<span data-ttu-id="d374f-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d374f-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d374f-152">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d374f-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d374f-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d374f-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d374f-154">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d374f-154">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d374f-155">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-155">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d374f-156">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-156">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d374f-157">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-157">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d374f-158">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d374f-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d374f-159">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-159">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d374f-160">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d374f-161">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d374f-162">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d374f-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="d374f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d374f-164">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d374f-165">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d374f-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d374f-166">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d374f-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d374f-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="d374f-167">RELATED LINKS</span></span>

