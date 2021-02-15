---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142253"
---
# <span data-ttu-id="ed39f-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="ed39f-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="ed39f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed39f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed39f-103">建立新資料庫或更新現有的資料庫。</span><span class="sxs-lookup"><span data-stu-id="ed39f-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ed39f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed39f-104">SYNTAX</span></span>

### <span data-ttu-id="ed39f-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="ed39f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ed39f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ed39f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed39f-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed39f-107">DESCRIPTION</span></span>
<span data-ttu-id="ed39f-108">建立新資料庫或更新現有的資料庫。</span><span class="sxs-lookup"><span data-stu-id="ed39f-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ed39f-109">示例</span><span class="sxs-lookup"><span data-stu-id="ed39f-109">EXAMPLES</span></span>

### <span data-ttu-id="ed39f-110">範例1：依名稱更新 MySql 伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="ed39f-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="ed39f-111">依資源名稱更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="ed39f-111">Update a database by resource name.</span></span>

### <span data-ttu-id="ed39f-112">範例2：依參數更新 MySql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ed39f-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="ed39f-113">依參數更新資料庫</span><span class="sxs-lookup"><span data-stu-id="ed39f-113">Update a database by parameter</span></span>

## <span data-ttu-id="ed39f-114">參數</span><span class="sxs-lookup"><span data-stu-id="ed39f-114">PARAMETERS</span></span>

### <span data-ttu-id="ed39f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed39f-115">-AsJob</span></span>
<span data-ttu-id="ed39f-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ed39f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ed39f-117">字元集</span><span class="sxs-lookup"><span data-stu-id="ed39f-117">-Charset</span></span>
<span data-ttu-id="ed39f-118">資料庫的字元集。</span><span class="sxs-lookup"><span data-stu-id="ed39f-118">The charset of the database.</span></span>

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

### <span data-ttu-id="ed39f-119">-排序規則</span><span class="sxs-lookup"><span data-stu-id="ed39f-119">-Collation</span></span>
<span data-ttu-id="ed39f-120">資料庫的排序規則。</span><span class="sxs-lookup"><span data-stu-id="ed39f-120">The collation of the database.</span></span>

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

### <span data-ttu-id="ed39f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed39f-121">-DefaultProfile</span></span>
<span data-ttu-id="ed39f-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed39f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed39f-123">-InputObject</span></span>
<span data-ttu-id="ed39f-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ed39f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ed39f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed39f-125">-Name</span></span>
<span data-ttu-id="ed39f-126">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed39f-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed39f-127">-NoWait</span></span>
<span data-ttu-id="ed39f-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ed39f-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed39f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed39f-129">-ResourceGroupName</span></span>
<span data-ttu-id="ed39f-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-130">The name of the resource group.</span></span>
<span data-ttu-id="ed39f-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ed39f-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ed39f-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ed39f-132">-ServerName</span></span>
<span data-ttu-id="ed39f-133">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-133">The name of the server.</span></span>

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

### <span data-ttu-id="ed39f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed39f-134">-SubscriptionId</span></span>
<span data-ttu-id="ed39f-135">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ed39f-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ed39f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="ed39f-136">-Confirm</span></span>
<span data-ttu-id="ed39f-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed39f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed39f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed39f-138">-WhatIf</span></span>
<span data-ttu-id="ed39f-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed39f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed39f-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed39f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed39f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed39f-141">CommonParameters</span></span>
<span data-ttu-id="ed39f-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed39f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed39f-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ed39f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed39f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ed39f-144">INPUTS</span></span>

### <span data-ttu-id="ed39f-145">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ed39f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ed39f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ed39f-146">OUTPUTS</span></span>

### <span data-ttu-id="ed39f-147">IDatabase 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="ed39f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="ed39f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ed39f-148">NOTES</span></span>

<span data-ttu-id="ed39f-149">別名</span><span class="sxs-lookup"><span data-stu-id="ed39f-149">ALIASES</span></span>

<span data-ttu-id="ed39f-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ed39f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed39f-151">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ed39f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed39f-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ed39f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed39f-153">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ed39f-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed39f-154">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ed39f-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ed39f-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ed39f-157">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ed39f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed39f-158">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ed39f-159">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ed39f-160">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ed39f-161">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ed39f-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="ed39f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ed39f-163">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ed39f-164">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed39f-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ed39f-165">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed39f-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ed39f-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed39f-166">RELATED LINKS</span></span>

