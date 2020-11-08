---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139668"
---
# <span data-ttu-id="d2643-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="d2643-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="d2643-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2643-102">SYNOPSIS</span></span>
<span data-ttu-id="d2643-103">重新開機伺服器。</span><span class="sxs-lookup"><span data-stu-id="d2643-103">Restarts a server.</span></span>

## <span data-ttu-id="d2643-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2643-104">SYNTAX</span></span>

### <span data-ttu-id="d2643-105">重新開機 (預設) </span><span class="sxs-lookup"><span data-stu-id="d2643-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2643-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2643-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2643-107">說明</span><span class="sxs-lookup"><span data-stu-id="d2643-107">DESCRIPTION</span></span>
<span data-ttu-id="d2643-108">重新開機伺服器。</span><span class="sxs-lookup"><span data-stu-id="d2643-108">Restarts a server.</span></span>

## <span data-ttu-id="d2643-109">示例</span><span class="sxs-lookup"><span data-stu-id="d2643-109">EXAMPLES</span></span>

### <span data-ttu-id="d2643-110">範例1：依資源群組和伺服器名稱重新開機 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="d2643-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="d2643-111">這個 Cmdlet 會依資源群組和伺服器名稱來重新開機 PostgreSql server。</span><span class="sxs-lookup"><span data-stu-id="d2643-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="d2643-112">範例2：依身分識別重新開機 PostgreSql 伺服器</span><span class="sxs-lookup"><span data-stu-id="d2643-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="d2643-113">這些 Cmdlet 會依身分識別來重新開機 PostgreSql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d2643-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="d2643-114">參數</span><span class="sxs-lookup"><span data-stu-id="d2643-114">PARAMETERS</span></span>

### <span data-ttu-id="d2643-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2643-115">-AsJob</span></span>
<span data-ttu-id="d2643-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="d2643-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d2643-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2643-117">-DefaultProfile</span></span>
<span data-ttu-id="d2643-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2643-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2643-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2643-119">-InputObject</span></span>
<span data-ttu-id="d2643-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d2643-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2643-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2643-121">-Name</span></span>
<span data-ttu-id="d2643-122">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-122">The name of the server.</span></span>

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

### <span data-ttu-id="d2643-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2643-123">-NoWait</span></span>
<span data-ttu-id="d2643-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="d2643-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2643-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2643-125">-PassThru</span></span>
<span data-ttu-id="d2643-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="d2643-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2643-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2643-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2643-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-128">The name of the resource group.</span></span>
<span data-ttu-id="d2643-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d2643-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d2643-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2643-130">-SubscriptionId</span></span>
<span data-ttu-id="d2643-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="d2643-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d2643-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d2643-132">-Confirm</span></span>
<span data-ttu-id="d2643-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2643-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2643-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2643-134">-WhatIf</span></span>
<span data-ttu-id="d2643-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2643-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2643-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2643-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2643-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2643-137">CommonParameters</span></span>
<span data-ttu-id="d2643-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2643-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2643-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d2643-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2643-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d2643-140">INPUTS</span></span>

### <span data-ttu-id="d2643-141">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="d2643-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d2643-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d2643-142">OUTPUTS</span></span>

### <span data-ttu-id="d2643-143">System.object</span><span class="sxs-lookup"><span data-stu-id="d2643-143">System.Boolean</span></span>

## <span data-ttu-id="d2643-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d2643-144">NOTES</span></span>

<span data-ttu-id="d2643-145">別名</span><span class="sxs-lookup"><span data-stu-id="d2643-145">ALIASES</span></span>

<span data-ttu-id="d2643-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d2643-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2643-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d2643-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2643-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d2643-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2643-149">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d2643-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2643-150">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d2643-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d2643-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d2643-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d2643-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2643-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d2643-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2643-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d2643-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2643-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d2643-158">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d2643-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2643-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2643-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2643-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d2643-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2643-161">RELATED LINKS</span></span>

