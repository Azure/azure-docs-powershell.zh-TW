---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 7d356bc977ce02d998230ad755f43479e09f0a66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906117"
---
# <span data-ttu-id="b08e9-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="b08e9-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="b08e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b08e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b08e9-103">建立新資料庫或更新現有資料庫。</span><span class="sxs-lookup"><span data-stu-id="b08e9-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="b08e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="b08e9-104">SYNTAX</span></span>

### <span data-ttu-id="b08e9-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b08e9-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b08e9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b08e9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b08e9-107">描述</span><span class="sxs-lookup"><span data-stu-id="b08e9-107">DESCRIPTION</span></span>
<span data-ttu-id="b08e9-108">建立新資料庫或更新現有資料庫。</span><span class="sxs-lookup"><span data-stu-id="b08e9-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="b08e9-109">例子</span><span class="sxs-lookup"><span data-stu-id="b08e9-109">EXAMPLES</span></span>

### <span data-ttu-id="b08e9-110">範例 1：根據名稱更新 MySql 伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="b08e9-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="b08e9-111">根據資源名稱更新資料庫。</span><span class="sxs-lookup"><span data-stu-id="b08e9-111">Update a database by resource name.</span></span>

### <span data-ttu-id="b08e9-112">範例 2：根據參數更新 MySql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b08e9-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="b08e9-113">根據參數更新資料庫</span><span class="sxs-lookup"><span data-stu-id="b08e9-113">Update a database by parameter</span></span>

## <span data-ttu-id="b08e9-114">參數</span><span class="sxs-lookup"><span data-stu-id="b08e9-114">PARAMETERS</span></span>

### <span data-ttu-id="b08e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b08e9-115">-AsJob</span></span>
<span data-ttu-id="b08e9-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b08e9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b08e9-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="b08e9-117">-Charset</span></span>
<span data-ttu-id="b08e9-118">資料庫的字元集。</span><span class="sxs-lookup"><span data-stu-id="b08e9-118">The charset of the database.</span></span>

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

### <span data-ttu-id="b08e9-119">-排序</span><span class="sxs-lookup"><span data-stu-id="b08e9-119">-Collation</span></span>
<span data-ttu-id="b08e9-120">資料庫的排序。</span><span class="sxs-lookup"><span data-stu-id="b08e9-120">The collation of the database.</span></span>

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

### <span data-ttu-id="b08e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08e9-121">-DefaultProfile</span></span>
<span data-ttu-id="b08e9-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b08e9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b08e9-123">-InputObject</span></span>
<span data-ttu-id="b08e9-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b08e9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b08e9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b08e9-125">-Name</span></span>
<span data-ttu-id="b08e9-126">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-126">The name of the database.</span></span>

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

### <span data-ttu-id="b08e9-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b08e9-127">-NoWait</span></span>
<span data-ttu-id="b08e9-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b08e9-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b08e9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08e9-129">-ResourceGroupName</span></span>
<span data-ttu-id="b08e9-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-130">The name of the resource group.</span></span>
<span data-ttu-id="b08e9-131">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b08e9-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b08e9-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b08e9-132">-ServerName</span></span>
<span data-ttu-id="b08e9-133">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-133">The name of the server.</span></span>

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

### <span data-ttu-id="b08e9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b08e9-134">-SubscriptionId</span></span>
<span data-ttu-id="b08e9-135">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b08e9-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b08e9-136">-確認</span><span class="sxs-lookup"><span data-stu-id="b08e9-136">-Confirm</span></span>
<span data-ttu-id="b08e9-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b08e9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b08e9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b08e9-138">-WhatIf</span></span>
<span data-ttu-id="b08e9-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b08e9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b08e9-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b08e9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b08e9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08e9-141">CommonParameters</span></span>
<span data-ttu-id="b08e9-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b08e9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08e9-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b08e9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08e9-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b08e9-144">INPUTS</span></span>

### <span data-ttu-id="b08e9-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b08e9-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b08e9-146">輸出</span><span class="sxs-lookup"><span data-stu-id="b08e9-146">OUTPUTS</span></span>

### <span data-ttu-id="b08e9-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="b08e9-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="b08e9-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b08e9-148">NOTES</span></span>

<span data-ttu-id="b08e9-149">別名</span><span class="sxs-lookup"><span data-stu-id="b08e9-149">ALIASES</span></span>

<span data-ttu-id="b08e9-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b08e9-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b08e9-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b08e9-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b08e9-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b08e9-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b08e9-153">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b08e9-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b08e9-154">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b08e9-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b08e9-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b08e9-157">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b08e9-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b08e9-158">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b08e9-159">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b08e9-160">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b08e9-161">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b08e9-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="b08e9-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b08e9-163">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b08e9-164">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b08e9-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b08e9-165">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b08e9-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b08e9-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="b08e9-166">RELATED LINKS</span></span>

