---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 656fbdc012f4e6de5f80c88a20cde42a49244618
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435275"
---
# <span data-ttu-id="ecac0-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="ecac0-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="ecac0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecac0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecac0-103">刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecac0-103">Deletes a database.</span></span>

## <span data-ttu-id="ecac0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecac0-104">SYNTAX</span></span>

### <span data-ttu-id="ecac0-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ecac0-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ecac0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ecac0-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ecac0-107">說明</span><span class="sxs-lookup"><span data-stu-id="ecac0-107">DESCRIPTION</span></span>
<span data-ttu-id="ecac0-108">刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecac0-108">Deletes a database.</span></span>

## <span data-ttu-id="ecac0-109">示例</span><span class="sxs-lookup"><span data-stu-id="ecac0-109">EXAMPLES</span></span>

### <span data-ttu-id="ecac0-110">範例1：依名稱移除 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="ecac0-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="ecac0-111">這個 Cmdlet 會依名稱移除 MySql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecac0-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="ecac0-112">範例2：依身分識別移除 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="ecac0-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="ecac0-113">這些 Cmdlet 會透過身分識別來移除 MySql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="ecac0-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="ecac0-114">參數</span><span class="sxs-lookup"><span data-stu-id="ecac0-114">PARAMETERS</span></span>

### <span data-ttu-id="ecac0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecac0-115">-AsJob</span></span>
<span data-ttu-id="ecac0-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ecac0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ecac0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecac0-117">-DefaultProfile</span></span>
<span data-ttu-id="ecac0-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecac0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecac0-119">-InputObject</span></span>
<span data-ttu-id="ecac0-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ecac0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecac0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ecac0-121">-Name</span></span>
<span data-ttu-id="ecac0-122">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-122">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecac0-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ecac0-123">-NoWait</span></span>
<span data-ttu-id="ecac0-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="ecac0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ecac0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecac0-125">-PassThru</span></span>
<span data-ttu-id="ecac0-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ecac0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ecac0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecac0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ecac0-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-128">The name of the resource group.</span></span>
<span data-ttu-id="ecac0-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ecac0-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ecac0-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ecac0-130">-ServerName</span></span>
<span data-ttu-id="ecac0-131">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-131">The name of the server.</span></span>

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

### <span data-ttu-id="ecac0-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecac0-132">-SubscriptionId</span></span>
<span data-ttu-id="ecac0-133">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ecac0-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ecac0-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ecac0-134">-Confirm</span></span>
<span data-ttu-id="ecac0-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ecac0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecac0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecac0-136">-WhatIf</span></span>
<span data-ttu-id="ecac0-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ecac0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecac0-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecac0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecac0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecac0-139">CommonParameters</span></span>
<span data-ttu-id="ecac0-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecac0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecac0-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ecac0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecac0-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ecac0-142">INPUTS</span></span>

### <span data-ttu-id="ecac0-143">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ecac0-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ecac0-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ecac0-144">OUTPUTS</span></span>

### <span data-ttu-id="ecac0-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ecac0-145">System.Boolean</span></span>

## <span data-ttu-id="ecac0-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ecac0-146">NOTES</span></span>

<span data-ttu-id="ecac0-147">別名</span><span class="sxs-lookup"><span data-stu-id="ecac0-147">ALIASES</span></span>

<span data-ttu-id="ecac0-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ecac0-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ecac0-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ecac0-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ecac0-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ecac0-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ecac0-151">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ecac0-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ecac0-152">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ecac0-153">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ecac0-154">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ecac0-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ecac0-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ecac0-156">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ecac0-157">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ecac0-158">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ecac0-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ecac0-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="ecac0-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ecac0-161">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ecac0-162">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ecac0-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ecac0-163">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ecac0-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ecac0-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecac0-164">RELATED LINKS</span></span>

