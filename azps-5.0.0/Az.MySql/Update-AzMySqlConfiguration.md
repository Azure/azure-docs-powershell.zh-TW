---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: c4eb244dd2d1a0d685bf18f39deedf9992b5597e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139845"
---
# <span data-ttu-id="f95dd-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f95dd-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="f95dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f95dd-102">SYNOPSIS</span></span>
<span data-ttu-id="f95dd-103">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="f95dd-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="f95dd-104">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzMySqlServer]。</span><span class="sxs-lookup"><span data-stu-id="f95dd-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="f95dd-105">句法</span><span class="sxs-lookup"><span data-stu-id="f95dd-105">SYNTAX</span></span>

### <span data-ttu-id="f95dd-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f95dd-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f95dd-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f95dd-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f95dd-108">說明</span><span class="sxs-lookup"><span data-stu-id="f95dd-108">DESCRIPTION</span></span>
<span data-ttu-id="f95dd-109">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="f95dd-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="f95dd-110">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzMySqlServer]。</span><span class="sxs-lookup"><span data-stu-id="f95dd-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="f95dd-111">示例</span><span class="sxs-lookup"><span data-stu-id="f95dd-111">EXAMPLES</span></span>

### <span data-ttu-id="f95dd-112">範例1：依名稱更新 MySql 配置</span><span class="sxs-lookup"><span data-stu-id="f95dd-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="f95dd-113">這個 Cmdlet 會依名稱更新 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="f95dd-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="f95dd-114">範例2：依身分識別來更新 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="f95dd-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="f95dd-115">這些 Cmdlet 會依身分識別來更新 MySql 設定。</span><span class="sxs-lookup"><span data-stu-id="f95dd-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="f95dd-116">參數</span><span class="sxs-lookup"><span data-stu-id="f95dd-116">PARAMETERS</span></span>

### <span data-ttu-id="f95dd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f95dd-117">-AsJob</span></span>
<span data-ttu-id="f95dd-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f95dd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f95dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95dd-119">-DefaultProfile</span></span>
<span data-ttu-id="f95dd-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95dd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f95dd-121">-InputObject</span></span>
<span data-ttu-id="f95dd-122">身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="f95dd-122">Identity Parameter.</span></span>
<span data-ttu-id="f95dd-123">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f95dd-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f95dd-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f95dd-124">-Name</span></span>
<span data-ttu-id="f95dd-125">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-125">The name of the server configuration.</span></span>

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

### <span data-ttu-id="f95dd-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f95dd-126">-NoWait</span></span>
<span data-ttu-id="f95dd-127">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f95dd-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f95dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="f95dd-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-129">The name of the resource group.</span></span>
<span data-ttu-id="f95dd-130">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f95dd-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f95dd-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f95dd-131">-ServerName</span></span>
<span data-ttu-id="f95dd-132">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-132">The name of the server.</span></span>

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

### <span data-ttu-id="f95dd-133">-來源</span><span class="sxs-lookup"><span data-stu-id="f95dd-133">-Source</span></span>
<span data-ttu-id="f95dd-134">配置來源。</span><span class="sxs-lookup"><span data-stu-id="f95dd-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="f95dd-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f95dd-135">-SubscriptionId</span></span>
<span data-ttu-id="f95dd-136">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="f95dd-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f95dd-137">-值</span><span class="sxs-lookup"><span data-stu-id="f95dd-137">-Value</span></span>
<span data-ttu-id="f95dd-138">配置的值。</span><span class="sxs-lookup"><span data-stu-id="f95dd-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="f95dd-139">-確認</span><span class="sxs-lookup"><span data-stu-id="f95dd-139">-Confirm</span></span>
<span data-ttu-id="f95dd-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f95dd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95dd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95dd-141">-WhatIf</span></span>
<span data-ttu-id="f95dd-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f95dd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f95dd-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f95dd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95dd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95dd-144">CommonParameters</span></span>
<span data-ttu-id="f95dd-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f95dd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95dd-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f95dd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95dd-147">輸入</span><span class="sxs-lookup"><span data-stu-id="f95dd-147">INPUTS</span></span>

### <span data-ttu-id="f95dd-148">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f95dd-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="f95dd-149">輸出</span><span class="sxs-lookup"><span data-stu-id="f95dd-149">OUTPUTS</span></span>

### <span data-ttu-id="f95dd-150">IConfiguration 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="f95dd-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="f95dd-151">筆記</span><span class="sxs-lookup"><span data-stu-id="f95dd-151">NOTES</span></span>

<span data-ttu-id="f95dd-152">別名</span><span class="sxs-lookup"><span data-stu-id="f95dd-152">ALIASES</span></span>

<span data-ttu-id="f95dd-153">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f95dd-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f95dd-154">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f95dd-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f95dd-155">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f95dd-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f95dd-156">INPUTOBJECT <IMySqlIdentity> ：身分識別參數。</span><span class="sxs-lookup"><span data-stu-id="f95dd-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="f95dd-157">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f95dd-158">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f95dd-159">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f95dd-160">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f95dd-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f95dd-161">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f95dd-162">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f95dd-163">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f95dd-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="f95dd-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f95dd-165">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f95dd-166">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f95dd-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f95dd-167">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f95dd-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f95dd-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="f95dd-168">RELATED LINKS</span></span>

