---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: bff7f24ef88c8f6fc5022aae019a9c6f32bf95f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906122"
---
# <span data-ttu-id="8bfdf-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8bfdf-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="8bfdf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8bfdf-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfdf-103">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="8bfdf-104">如果您想要Update-AzMySqlServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="8bfdf-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="8bfdf-105">語法</span><span class="sxs-lookup"><span data-stu-id="8bfdf-105">SYNTAX</span></span>

### <span data-ttu-id="8bfdf-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8bfdf-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8bfdf-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8bfdf-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8bfdf-108">描述</span><span class="sxs-lookup"><span data-stu-id="8bfdf-108">DESCRIPTION</span></span>
<span data-ttu-id="8bfdf-109">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="8bfdf-110">如果您想要Update-AzMySqlServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="8bfdf-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="8bfdf-111">例子</span><span class="sxs-lookup"><span data-stu-id="8bfdf-111">EXAMPLES</span></span>

### <span data-ttu-id="8bfdf-112">範例 1：根據名稱更新 MySql 組配置</span><span class="sxs-lookup"><span data-stu-id="8bfdf-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="8bfdf-113">此 Cmdlet 會更新 MySql 的組名。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="8bfdf-114">範例 2：根據身分識別更新 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="8bfdf-115">這些 Cmdlet 會根據身分識別更新 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="8bfdf-116">參數</span><span class="sxs-lookup"><span data-stu-id="8bfdf-116">PARAMETERS</span></span>

### <span data-ttu-id="8bfdf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bfdf-117">-AsJob</span></span>
<span data-ttu-id="8bfdf-118">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="8bfdf-118">Run the command as a job</span></span>

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

### <span data-ttu-id="8bfdf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfdf-119">-DefaultProfile</span></span>
<span data-ttu-id="8bfdf-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bfdf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bfdf-121">-InputObject</span></span>
<span data-ttu-id="8bfdf-122">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-122">Identity Parameter.</span></span>
<span data-ttu-id="8bfdf-123">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bfdf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8bfdf-124">-Name</span></span>
<span data-ttu-id="8bfdf-125">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="8bfdf-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8bfdf-126">-NoWait</span></span>
<span data-ttu-id="8bfdf-127">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="8bfdf-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8bfdf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bfdf-128">-ResourceGroupName</span></span>
<span data-ttu-id="8bfdf-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-129">The name of the resource group.</span></span>
<span data-ttu-id="8bfdf-130">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8bfdf-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8bfdf-131">-ServerName</span></span>
<span data-ttu-id="8bfdf-132">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-132">The name of the server.</span></span>

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

### <span data-ttu-id="8bfdf-133">-來源</span><span class="sxs-lookup"><span data-stu-id="8bfdf-133">-Source</span></span>
<span data-ttu-id="8bfdf-134">組組的來源。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="8bfdf-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bfdf-135">-SubscriptionId</span></span>
<span data-ttu-id="8bfdf-136">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8bfdf-137">-值</span><span class="sxs-lookup"><span data-stu-id="8bfdf-137">-Value</span></span>
<span data-ttu-id="8bfdf-138">組名的值。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="8bfdf-139">-確認</span><span class="sxs-lookup"><span data-stu-id="8bfdf-139">-Confirm</span></span>
<span data-ttu-id="8bfdf-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bfdf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bfdf-141">-WhatIf</span></span>
<span data-ttu-id="8bfdf-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bfdf-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bfdf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfdf-144">CommonParameters</span></span>
<span data-ttu-id="8bfdf-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfdf-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bfdf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfdf-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8bfdf-147">INPUTS</span></span>

### <span data-ttu-id="8bfdf-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8bfdf-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8bfdf-149">輸出</span><span class="sxs-lookup"><span data-stu-id="8bfdf-149">OUTPUTS</span></span>

### <span data-ttu-id="8bfdf-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="8bfdf-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="8bfdf-151">筆記</span><span class="sxs-lookup"><span data-stu-id="8bfdf-151">NOTES</span></span>

<span data-ttu-id="8bfdf-152">別名</span><span class="sxs-lookup"><span data-stu-id="8bfdf-152">ALIASES</span></span>

<span data-ttu-id="8bfdf-153">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8bfdf-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8bfdf-154">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bfdf-155">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8bfdf-156">INPUTOBJECT： <IMySqlIdentity> 身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="8bfdf-157">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8bfdf-158">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8bfdf-159">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8bfdf-160">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8bfdf-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8bfdf-161">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8bfdf-162">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8bfdf-163">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8bfdf-164">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="8bfdf-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8bfdf-166">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8bfdf-167">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8bfdf-168">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bfdf-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8bfdf-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bfdf-169">RELATED LINKS</span></span>

