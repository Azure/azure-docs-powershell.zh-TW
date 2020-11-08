---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: bacd5e1636457fac172cd54c9fcf4407247d88ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126288"
---
# <span data-ttu-id="b3be6-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b3be6-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="b3be6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3be6-102">SYNOPSIS</span></span>
<span data-ttu-id="b3be6-103">刪除具有指定名稱的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b3be6-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="b3be6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3be6-104">SYNTAX</span></span>

### <span data-ttu-id="b3be6-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b3be6-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b3be6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3be6-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3be6-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3be6-107">DESCRIPTION</span></span>
<span data-ttu-id="b3be6-108">刪除具有指定名稱的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b3be6-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="b3be6-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3be6-109">EXAMPLES</span></span>

### <span data-ttu-id="b3be6-110">範例1：依名稱移除 PostgreSql server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="b3be6-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="b3be6-111">這個 Cmdlet 會依名稱移除 PostgreSql server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b3be6-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="b3be6-112">範例2：依身分識別移除 PostgreSql server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="b3be6-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="b3be6-113">這些 Cmdlet 會依身分識別來移除 PostgreSql server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="b3be6-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="b3be6-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3be6-114">PARAMETERS</span></span>

### <span data-ttu-id="b3be6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3be6-115">-AsJob</span></span>
<span data-ttu-id="b3be6-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b3be6-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3be6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3be6-117">-DefaultProfile</span></span>
<span data-ttu-id="b3be6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3be6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3be6-119">-InputObject</span></span>
<span data-ttu-id="b3be6-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3be6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3be6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3be6-121">-Name</span></span>
<span data-ttu-id="b3be6-122">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3be6-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3be6-123">-NoWait</span></span>
<span data-ttu-id="b3be6-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b3be6-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3be6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3be6-125">-PassThru</span></span>
<span data-ttu-id="b3be6-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b3be6-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3be6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3be6-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3be6-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-128">The name of the resource group.</span></span>
<span data-ttu-id="b3be6-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3be6-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b3be6-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3be6-130">-ServerName</span></span>
<span data-ttu-id="b3be6-131">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-131">The name of the server.</span></span>

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

### <span data-ttu-id="b3be6-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3be6-132">-SubscriptionId</span></span>
<span data-ttu-id="b3be6-133">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="b3be6-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b3be6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b3be6-134">-Confirm</span></span>
<span data-ttu-id="b3be6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3be6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3be6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3be6-136">-WhatIf</span></span>
<span data-ttu-id="b3be6-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3be6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3be6-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3be6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3be6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3be6-139">CommonParameters</span></span>
<span data-ttu-id="b3be6-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3be6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3be6-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b3be6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3be6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b3be6-142">INPUTS</span></span>

### <span data-ttu-id="b3be6-143">IPostgreSqlIdentity （PostgreSql）的</span><span class="sxs-lookup"><span data-stu-id="b3be6-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="b3be6-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b3be6-144">OUTPUTS</span></span>

### <span data-ttu-id="b3be6-145">System.object</span><span class="sxs-lookup"><span data-stu-id="b3be6-145">System.Boolean</span></span>

## <span data-ttu-id="b3be6-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b3be6-146">NOTES</span></span>

<span data-ttu-id="b3be6-147">別名</span><span class="sxs-lookup"><span data-stu-id="b3be6-147">ALIASES</span></span>

<span data-ttu-id="b3be6-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b3be6-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3be6-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b3be6-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3be6-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b3be6-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3be6-151">INPUTOBJECT <IPostgreSqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b3be6-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3be6-152">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b3be6-153">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b3be6-154">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b3be6-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b3be6-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3be6-156">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b3be6-157">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b3be6-158">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b3be6-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="b3be6-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b3be6-160">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b3be6-161">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3be6-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b3be6-162">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be6-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b3be6-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3be6-163">RELATED LINKS</span></span>

