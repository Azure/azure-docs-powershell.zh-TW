---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/restart-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 8e969551724a4965d17ce34e3b18c794705b764f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902326"
---
# <span data-ttu-id="3d193-101">Restart-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="3d193-101">Restart-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="3d193-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3d193-102">SYNOPSIS</span></span>
<span data-ttu-id="3d193-103">重新開機伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d193-103">Restarts a server.</span></span>

## <span data-ttu-id="3d193-104">語法</span><span class="sxs-lookup"><span data-stu-id="3d193-104">SYNTAX</span></span>

### <span data-ttu-id="3d193-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="3d193-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3d193-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d193-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3d193-107">描述</span><span class="sxs-lookup"><span data-stu-id="3d193-107">DESCRIPTION</span></span>
<span data-ttu-id="3d193-108">重新開機伺服器。</span><span class="sxs-lookup"><span data-stu-id="3d193-108">Restarts a server.</span></span>

## <span data-ttu-id="3d193-109">例子</span><span class="sxs-lookup"><span data-stu-id="3d193-109">EXAMPLES</span></span>

### <span data-ttu-id="3d193-110">範例 1：按資源名稱重新開機伺服器</span><span class="sxs-lookup"><span data-stu-id="3d193-110">Example 1: Restart the server by resource name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test
```

<span data-ttu-id="3d193-111">按名稱重新開機伺服器</span><span class="sxs-lookup"><span data-stu-id="3d193-111">Restart the server by name</span></span>

### <span data-ttu-id="3d193-112">範例 2：以身分識別重新開機伺服器</span><span class="sxs-lookup"><span data-stu-id="3d193-112">Example 2: Restart the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test/restart"
PS C:\> Restart-AzPostgreSqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="3d193-113">以身分識別重新開機伺服器</span><span class="sxs-lookup"><span data-stu-id="3d193-113">Restart the server by identity</span></span>

## <span data-ttu-id="3d193-114">參數</span><span class="sxs-lookup"><span data-stu-id="3d193-114">PARAMETERS</span></span>

### <span data-ttu-id="3d193-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d193-115">-AsJob</span></span>
<span data-ttu-id="3d193-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="3d193-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3d193-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d193-117">-DefaultProfile</span></span>
<span data-ttu-id="3d193-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d193-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d193-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d193-119">-InputObject</span></span>
<span data-ttu-id="3d193-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3d193-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d193-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d193-121">-Name</span></span>
<span data-ttu-id="3d193-122">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d193-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3d193-123">-NoWait</span></span>
<span data-ttu-id="3d193-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="3d193-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3d193-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d193-125">-PassThru</span></span>
<span data-ttu-id="3d193-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="3d193-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3d193-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d193-127">-ResourceGroupName</span></span>
<span data-ttu-id="3d193-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-128">The name of the resource group.</span></span>
<span data-ttu-id="3d193-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3d193-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d193-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d193-130">-SubscriptionId</span></span>
<span data-ttu-id="3d193-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d193-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d193-132">-確認</span><span class="sxs-lookup"><span data-stu-id="3d193-132">-Confirm</span></span>
<span data-ttu-id="3d193-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3d193-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d193-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d193-134">-WhatIf</span></span>
<span data-ttu-id="3d193-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3d193-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d193-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d193-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d193-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d193-137">CommonParameters</span></span>
<span data-ttu-id="3d193-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3d193-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d193-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d193-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d193-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3d193-140">INPUTS</span></span>

### <span data-ttu-id="3d193-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3d193-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3d193-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3d193-142">OUTPUTS</span></span>

### <span data-ttu-id="3d193-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d193-143">System.Boolean</span></span>

## <span data-ttu-id="3d193-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3d193-144">NOTES</span></span>

<span data-ttu-id="3d193-145">別名</span><span class="sxs-lookup"><span data-stu-id="3d193-145">ALIASES</span></span>

<span data-ttu-id="3d193-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3d193-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d193-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3d193-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d193-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3d193-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d193-149">INPUTOBJECT： <IPostgreSqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3d193-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d193-150">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3d193-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3d193-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3d193-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3d193-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d193-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3d193-155">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3d193-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3d193-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="3d193-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3d193-158">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3d193-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d193-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3d193-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d193-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3d193-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d193-161">RELATED LINKS</span></span>

