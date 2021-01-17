---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287335"
---
# <span data-ttu-id="04df8-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="04df8-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="04df8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04df8-102">SYNOPSIS</span></span>
<span data-ttu-id="04df8-103">建立新資料庫或更新現有的資料庫。</span><span class="sxs-lookup"><span data-stu-id="04df8-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="04df8-104">句法</span><span class="sxs-lookup"><span data-stu-id="04df8-104">SYNTAX</span></span>

### <span data-ttu-id="04df8-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="04df8-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="04df8-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="04df8-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04df8-107">說明</span><span class="sxs-lookup"><span data-stu-id="04df8-107">DESCRIPTION</span></span>
<span data-ttu-id="04df8-108">建立新資料庫或更新現有的資料庫。</span><span class="sxs-lookup"><span data-stu-id="04df8-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="04df8-109">示例</span><span class="sxs-lookup"><span data-stu-id="04df8-109">EXAMPLES</span></span>

### <span data-ttu-id="04df8-110">範例1：建立新的 MySql 伺服器資料庫</span><span class="sxs-lookup"><span data-stu-id="04df8-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="04df8-111">使用預設設定建立資料庫。</span><span class="sxs-lookup"><span data-stu-id="04df8-111">Create a database with default settings.</span></span>

## <span data-ttu-id="04df8-112">參數</span><span class="sxs-lookup"><span data-stu-id="04df8-112">PARAMETERS</span></span>

### <span data-ttu-id="04df8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04df8-113">-AsJob</span></span>
<span data-ttu-id="04df8-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="04df8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="04df8-115">字元集</span><span class="sxs-lookup"><span data-stu-id="04df8-115">-Charset</span></span>
<span data-ttu-id="04df8-116">資料庫的字元集。</span><span class="sxs-lookup"><span data-stu-id="04df8-116">The charset of the database.</span></span>

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

### <span data-ttu-id="04df8-117">-排序規則</span><span class="sxs-lookup"><span data-stu-id="04df8-117">-Collation</span></span>
<span data-ttu-id="04df8-118">資料庫的排序規則。</span><span class="sxs-lookup"><span data-stu-id="04df8-118">The collation of the database.</span></span>

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

### <span data-ttu-id="04df8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04df8-119">-DefaultProfile</span></span>
<span data-ttu-id="04df8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04df8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04df8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04df8-121">-InputObject</span></span>
<span data-ttu-id="04df8-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="04df8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="04df8-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="04df8-123">-Name</span></span>
<span data-ttu-id="04df8-124">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-124">The name of the database.</span></span>

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

### <span data-ttu-id="04df8-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04df8-125">-NoWait</span></span>
<span data-ttu-id="04df8-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="04df8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="04df8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04df8-127">-ResourceGroupName</span></span>
<span data-ttu-id="04df8-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-128">The name of the resource group.</span></span>
<span data-ttu-id="04df8-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="04df8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="04df8-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="04df8-130">-ServerName</span></span>
<span data-ttu-id="04df8-131">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-131">The name of the server.</span></span>

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

### <span data-ttu-id="04df8-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04df8-132">-SubscriptionId</span></span>
<span data-ttu-id="04df8-133">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="04df8-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="04df8-134">-確認</span><span class="sxs-lookup"><span data-stu-id="04df8-134">-Confirm</span></span>
<span data-ttu-id="04df8-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04df8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04df8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04df8-136">-WhatIf</span></span>
<span data-ttu-id="04df8-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04df8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04df8-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04df8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04df8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04df8-139">CommonParameters</span></span>
<span data-ttu-id="04df8-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04df8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04df8-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04df8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04df8-142">輸入</span><span class="sxs-lookup"><span data-stu-id="04df8-142">INPUTS</span></span>

### <span data-ttu-id="04df8-143">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="04df8-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="04df8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="04df8-144">OUTPUTS</span></span>

### <span data-ttu-id="04df8-145">IDatabase 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="04df8-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="04df8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="04df8-146">NOTES</span></span>

<span data-ttu-id="04df8-147">別名</span><span class="sxs-lookup"><span data-stu-id="04df8-147">ALIASES</span></span>

<span data-ttu-id="04df8-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="04df8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="04df8-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="04df8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="04df8-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="04df8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="04df8-151">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="04df8-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="04df8-152">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="04df8-153">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="04df8-154">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="04df8-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="04df8-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="04df8-156">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="04df8-157">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="04df8-158">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="04df8-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="04df8-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="04df8-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="04df8-161">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="04df8-162">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="04df8-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="04df8-163">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="04df8-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="04df8-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="04df8-164">RELATED LINKS</span></span>

