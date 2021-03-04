---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: b29f1162f784535ab635c437d9d481bb9f9492cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915446"
---
# <span data-ttu-id="6250a-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6250a-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="6250a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6250a-102">SYNOPSIS</span></span>
<span data-ttu-id="6250a-103">刪除伺服器防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6250a-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="6250a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6250a-104">SYNTAX</span></span>

### <span data-ttu-id="6250a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="6250a-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6250a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6250a-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6250a-107">描述</span><span class="sxs-lookup"><span data-stu-id="6250a-107">DESCRIPTION</span></span>
<span data-ttu-id="6250a-108">刪除伺服器防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6250a-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="6250a-109">例子</span><span class="sxs-lookup"><span data-stu-id="6250a-109">EXAMPLES</span></span>

### <span data-ttu-id="6250a-110">範例 1：移除 MariaDB 下的防火牆規則</span><span class="sxs-lookup"><span data-stu-id="6250a-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="6250a-111">此命令會移除 MariaDB 下的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="6250a-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="6250a-112">參數</span><span class="sxs-lookup"><span data-stu-id="6250a-112">PARAMETERS</span></span>

### <span data-ttu-id="6250a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6250a-113">-AsJob</span></span>
<span data-ttu-id="6250a-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="6250a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="6250a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6250a-115">-DefaultProfile</span></span>
<span data-ttu-id="6250a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6250a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6250a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6250a-117">-InputObject</span></span>
<span data-ttu-id="6250a-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6250a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6250a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6250a-119">-Name</span></span>
<span data-ttu-id="6250a-120">伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6250a-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6250a-121">-NoWait</span></span>
<span data-ttu-id="6250a-122">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="6250a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6250a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6250a-123">-PassThru</span></span>
<span data-ttu-id="6250a-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="6250a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6250a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6250a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6250a-126">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6250a-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6250a-127">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6250a-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6250a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6250a-128">-ServerName</span></span>
<span data-ttu-id="6250a-129">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6250a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6250a-130">-SubscriptionId</span></span>
<span data-ttu-id="6250a-131">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6250a-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6250a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6250a-132">-Confirm</span></span>
<span data-ttu-id="6250a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6250a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6250a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6250a-134">-WhatIf</span></span>
<span data-ttu-id="6250a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6250a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6250a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6250a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6250a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6250a-137">CommonParameters</span></span>
<span data-ttu-id="6250a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6250a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6250a-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6250a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6250a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6250a-140">INPUTS</span></span>

### <span data-ttu-id="6250a-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="6250a-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="6250a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6250a-142">OUTPUTS</span></span>

### <span data-ttu-id="6250a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6250a-143">System.Boolean</span></span>

## <span data-ttu-id="6250a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6250a-144">NOTES</span></span>

<span data-ttu-id="6250a-145">別名</span><span class="sxs-lookup"><span data-stu-id="6250a-145">ALIASES</span></span>

<span data-ttu-id="6250a-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6250a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6250a-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6250a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6250a-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6250a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6250a-149">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6250a-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6250a-150">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6250a-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6250a-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6250a-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6250a-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6250a-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6250a-155">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6250a-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6250a-156">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="6250a-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6250a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6250a-158">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6250a-159">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="6250a-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="6250a-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6250a-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6250a-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="6250a-161">RELATED LINKS</span></span>

