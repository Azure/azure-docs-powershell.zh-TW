---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9f2fbae69d2831d063ea6bfa92e2f1ece90e9f12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902950"
---
# <span data-ttu-id="b903c-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="b903c-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="b903c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b903c-102">SYNOPSIS</span></span>
<span data-ttu-id="b903c-103">刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="b903c-103">Deletes a database.</span></span>

## <span data-ttu-id="b903c-104">語法</span><span class="sxs-lookup"><span data-stu-id="b903c-104">SYNTAX</span></span>

### <span data-ttu-id="b903c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b903c-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b903c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b903c-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b903c-107">描述</span><span class="sxs-lookup"><span data-stu-id="b903c-107">DESCRIPTION</span></span>
<span data-ttu-id="b903c-108">刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="b903c-108">Deletes a database.</span></span>

## <span data-ttu-id="b903c-109">例子</span><span class="sxs-lookup"><span data-stu-id="b903c-109">EXAMPLES</span></span>

### <span data-ttu-id="b903c-110">範例 1：根據名稱移除 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="b903c-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="b903c-111">此 Cmdlet 會按名稱移除 MySql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b903c-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="b903c-112">範例 2：根據身分識別移除 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="b903c-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="b903c-113">這些 Cmdlet 會以身分識別移除 MySql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b903c-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="b903c-114">參數</span><span class="sxs-lookup"><span data-stu-id="b903c-114">PARAMETERS</span></span>

### <span data-ttu-id="b903c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b903c-115">-AsJob</span></span>
<span data-ttu-id="b903c-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b903c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b903c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b903c-117">-DefaultProfile</span></span>
<span data-ttu-id="b903c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b903c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b903c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b903c-119">-InputObject</span></span>
<span data-ttu-id="b903c-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b903c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b903c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b903c-121">-Name</span></span>
<span data-ttu-id="b903c-122">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-122">The name of the database.</span></span>

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

### <span data-ttu-id="b903c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b903c-123">-NoWait</span></span>
<span data-ttu-id="b903c-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b903c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b903c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b903c-125">-PassThru</span></span>
<span data-ttu-id="b903c-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="b903c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b903c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b903c-127">-ResourceGroupName</span></span>
<span data-ttu-id="b903c-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-128">The name of the resource group.</span></span>
<span data-ttu-id="b903c-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b903c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b903c-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b903c-130">-ServerName</span></span>
<span data-ttu-id="b903c-131">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-131">The name of the server.</span></span>

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

### <span data-ttu-id="b903c-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b903c-132">-SubscriptionId</span></span>
<span data-ttu-id="b903c-133">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b903c-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b903c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b903c-134">-Confirm</span></span>
<span data-ttu-id="b903c-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b903c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b903c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b903c-136">-WhatIf</span></span>
<span data-ttu-id="b903c-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b903c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b903c-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b903c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b903c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b903c-139">CommonParameters</span></span>
<span data-ttu-id="b903c-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b903c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b903c-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b903c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b903c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b903c-142">INPUTS</span></span>

### <span data-ttu-id="b903c-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b903c-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b903c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b903c-144">OUTPUTS</span></span>

### <span data-ttu-id="b903c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b903c-145">System.Boolean</span></span>

## <span data-ttu-id="b903c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b903c-146">NOTES</span></span>

<span data-ttu-id="b903c-147">別名</span><span class="sxs-lookup"><span data-stu-id="b903c-147">ALIASES</span></span>

<span data-ttu-id="b903c-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b903c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b903c-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b903c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b903c-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b903c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b903c-151">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b903c-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b903c-152">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b903c-153">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b903c-154">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b903c-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b903c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b903c-156">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b903c-157">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b903c-158">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b903c-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b903c-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="b903c-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b903c-161">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b903c-162">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b903c-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b903c-163">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b903c-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b903c-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="b903c-164">RELATED LINKS</span></span>

