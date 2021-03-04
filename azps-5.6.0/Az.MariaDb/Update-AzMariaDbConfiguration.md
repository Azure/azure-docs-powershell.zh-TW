---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: dc2a36a9ac8c2595ef2f60b8edc40582ad864ff8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915426"
---
# <span data-ttu-id="8507f-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="8507f-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="8507f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8507f-102">SYNOPSIS</span></span>
<span data-ttu-id="8507f-103">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="8507f-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="8507f-104">如果您想要Update-AzMariaDbServer AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="8507f-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="8507f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8507f-105">SYNTAX</span></span>

### <span data-ttu-id="8507f-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8507f-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8507f-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8507f-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8507f-108">描述</span><span class="sxs-lookup"><span data-stu-id="8507f-108">DESCRIPTION</span></span>
<span data-ttu-id="8507f-109">補救伺服器的組配置。</span><span class="sxs-lookup"><span data-stu-id="8507f-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="8507f-110">如果您想要Update-AzMariaDberver AdministratorLoginPassword、sKU 等，請改為使用</span><span class="sxs-lookup"><span data-stu-id="8507f-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="8507f-111">例子</span><span class="sxs-lookup"><span data-stu-id="8507f-111">EXAMPLES</span></span>

### <span data-ttu-id="8507f-112">範例 1：更新 MariaDB 組配置</span><span class="sxs-lookup"><span data-stu-id="8507f-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="8507f-113">此命令會更新 MariaDB 的組配置。</span><span class="sxs-lookup"><span data-stu-id="8507f-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="8507f-114">參數</span><span class="sxs-lookup"><span data-stu-id="8507f-114">PARAMETERS</span></span>

### <span data-ttu-id="8507f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8507f-115">-AsJob</span></span>
<span data-ttu-id="8507f-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="8507f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8507f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8507f-117">-DefaultProfile</span></span>
<span data-ttu-id="8507f-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8507f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8507f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8507f-119">-InputObject</span></span>
<span data-ttu-id="8507f-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8507f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8507f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8507f-121">-Name</span></span>
<span data-ttu-id="8507f-122">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="8507f-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="8507f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8507f-123">-NoWait</span></span>
<span data-ttu-id="8507f-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="8507f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8507f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8507f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8507f-126">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8507f-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8507f-127">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8507f-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8507f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8507f-128">-ServerName</span></span>
<span data-ttu-id="8507f-129">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-129">The name of the server.</span></span>

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

### <span data-ttu-id="8507f-130">-來源</span><span class="sxs-lookup"><span data-stu-id="8507f-130">-Source</span></span>
<span data-ttu-id="8507f-131">組組的來源。</span><span class="sxs-lookup"><span data-stu-id="8507f-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="8507f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8507f-132">-SubscriptionId</span></span>
<span data-ttu-id="8507f-133">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8507f-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8507f-134">-值</span><span class="sxs-lookup"><span data-stu-id="8507f-134">-Value</span></span>
<span data-ttu-id="8507f-135">組名的值。</span><span class="sxs-lookup"><span data-stu-id="8507f-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="8507f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="8507f-136">-Confirm</span></span>
<span data-ttu-id="8507f-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8507f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8507f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8507f-138">-WhatIf</span></span>
<span data-ttu-id="8507f-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8507f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8507f-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8507f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8507f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8507f-141">CommonParameters</span></span>
<span data-ttu-id="8507f-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8507f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8507f-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8507f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8507f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="8507f-144">INPUTS</span></span>

### <span data-ttu-id="8507f-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="8507f-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="8507f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8507f-146">OUTPUTS</span></span>

### <span data-ttu-id="8507f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="8507f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="8507f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8507f-148">NOTES</span></span>

<span data-ttu-id="8507f-149">別名</span><span class="sxs-lookup"><span data-stu-id="8507f-149">ALIASES</span></span>

<span data-ttu-id="8507f-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8507f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8507f-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8507f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8507f-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8507f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8507f-153">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8507f-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8507f-154">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8507f-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8507f-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8507f-157">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8507f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8507f-158">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8507f-159">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8507f-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8507f-160">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8507f-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8507f-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8507f-162">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8507f-163">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8507f-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="8507f-164">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8507f-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8507f-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="8507f-165">RELATED LINKS</span></span>

