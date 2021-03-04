---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 6f1af89c1557739e218506d441e6acb109fcf773
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908873"
---
# <span data-ttu-id="9d445-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="9d445-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="9d445-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9d445-102">SYNOPSIS</span></span>
<span data-ttu-id="9d445-103">建立新資料庫或更新現有資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d445-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="9d445-104">語法</span><span class="sxs-lookup"><span data-stu-id="9d445-104">SYNTAX</span></span>

### <span data-ttu-id="9d445-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9d445-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9d445-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9d445-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d445-107">描述</span><span class="sxs-lookup"><span data-stu-id="9d445-107">DESCRIPTION</span></span>
<span data-ttu-id="9d445-108">建立新資料庫或更新現有資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d445-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="9d445-109">例子</span><span class="sxs-lookup"><span data-stu-id="9d445-109">EXAMPLES</span></span>

### <span data-ttu-id="9d445-110">範例 1：建立新 MySql 伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="9d445-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="9d445-111">使用預設設定建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="9d445-111">Create a database with default settings.</span></span>

## <span data-ttu-id="9d445-112">參數</span><span class="sxs-lookup"><span data-stu-id="9d445-112">PARAMETERS</span></span>

### <span data-ttu-id="9d445-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d445-113">-AsJob</span></span>
<span data-ttu-id="9d445-114">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="9d445-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9d445-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="9d445-115">-Charset</span></span>
<span data-ttu-id="9d445-116">資料庫的字元集。</span><span class="sxs-lookup"><span data-stu-id="9d445-116">The charset of the database.</span></span>

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

### <span data-ttu-id="9d445-117">-排序</span><span class="sxs-lookup"><span data-stu-id="9d445-117">-Collation</span></span>
<span data-ttu-id="9d445-118">資料庫的排序。</span><span class="sxs-lookup"><span data-stu-id="9d445-118">The collation of the database.</span></span>

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

### <span data-ttu-id="9d445-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d445-119">-DefaultProfile</span></span>
<span data-ttu-id="9d445-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d445-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d445-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d445-121">-InputObject</span></span>
<span data-ttu-id="9d445-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9d445-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d445-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d445-123">-Name</span></span>
<span data-ttu-id="9d445-124">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d445-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9d445-125">-NoWait</span></span>
<span data-ttu-id="9d445-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="9d445-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d445-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d445-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d445-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-128">The name of the resource group.</span></span>
<span data-ttu-id="9d445-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9d445-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d445-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9d445-130">-ServerName</span></span>
<span data-ttu-id="9d445-131">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d445-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d445-132">-SubscriptionId</span></span>
<span data-ttu-id="9d445-133">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d445-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d445-134">-確認</span><span class="sxs-lookup"><span data-stu-id="9d445-134">-Confirm</span></span>
<span data-ttu-id="9d445-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9d445-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d445-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d445-136">-WhatIf</span></span>
<span data-ttu-id="9d445-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d445-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d445-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d445-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d445-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d445-139">CommonParameters</span></span>
<span data-ttu-id="9d445-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9d445-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d445-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d445-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d445-142">輸入</span><span class="sxs-lookup"><span data-stu-id="9d445-142">INPUTS</span></span>

### <span data-ttu-id="9d445-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9d445-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9d445-144">輸出</span><span class="sxs-lookup"><span data-stu-id="9d445-144">OUTPUTS</span></span>

### <span data-ttu-id="9d445-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="9d445-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="9d445-146">筆記</span><span class="sxs-lookup"><span data-stu-id="9d445-146">NOTES</span></span>

<span data-ttu-id="9d445-147">別名</span><span class="sxs-lookup"><span data-stu-id="9d445-147">ALIASES</span></span>

<span data-ttu-id="9d445-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9d445-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d445-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9d445-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d445-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9d445-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d445-151">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9d445-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d445-152">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9d445-153">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9d445-154">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9d445-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="9d445-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d445-156">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="9d445-157">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9d445-158">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9d445-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9d445-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="9d445-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9d445-161">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9d445-162">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d445-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9d445-163">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d445-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9d445-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d445-164">RELATED LINKS</span></span>

