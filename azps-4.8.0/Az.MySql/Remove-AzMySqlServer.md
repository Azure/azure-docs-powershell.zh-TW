---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlServer.md
ms.openlocfilehash: 86cc2a249479807adc14ad0faa4c682d1fef4725
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135857"
---
# <span data-ttu-id="c8862-101">Remove-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="c8862-101">Remove-AzMySqlServer</span></span>

## <span data-ttu-id="c8862-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8862-102">SYNOPSIS</span></span>
<span data-ttu-id="c8862-103">刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="c8862-103">Deletes a server.</span></span>

## <span data-ttu-id="c8862-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8862-104">SYNTAX</span></span>

### <span data-ttu-id="c8862-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c8862-105">Delete (Default)</span></span>
```
Remove-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c8862-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8862-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8862-107">說明</span><span class="sxs-lookup"><span data-stu-id="c8862-107">DESCRIPTION</span></span>
<span data-ttu-id="c8862-108">刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="c8862-108">Deletes a server.</span></span>

## <span data-ttu-id="c8862-109">示例</span><span class="sxs-lookup"><span data-stu-id="c8862-109">EXAMPLES</span></span>

### <span data-ttu-id="c8862-110">範例1：依 resourceGroup 和伺服器名稱移除 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="c8862-110">Example 1: Remove MySql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

```

<span data-ttu-id="c8862-111">這個 Cmdlet 會依 resourceGroup 和伺服器名稱移除 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c8862-111">This cmdlet removes MySql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="c8862-112">範例2：依身分識別移除 MySql 伺服器</span><span class="sxs-lookup"><span data-stu-id="c8862-112">Example 2: Remove MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Remove-AzMySqlServer -InputObject $ID
 
```

<span data-ttu-id="c8862-113">這些 Cmdlet 會依身分識別來移除 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c8862-113">These cmdlets remove MySql server by identity.</span></span>

## <span data-ttu-id="c8862-114">參數</span><span class="sxs-lookup"><span data-stu-id="c8862-114">PARAMETERS</span></span>

### <span data-ttu-id="c8862-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8862-115">-AsJob</span></span>
<span data-ttu-id="c8862-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="c8862-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c8862-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8862-117">-DefaultProfile</span></span>
<span data-ttu-id="c8862-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8862-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8862-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8862-119">-InputObject</span></span>
<span data-ttu-id="c8862-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c8862-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8862-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8862-121">-Name</span></span>
<span data-ttu-id="c8862-122">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8862-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c8862-123">-NoWait</span></span>
<span data-ttu-id="c8862-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="c8862-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c8862-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8862-125">-PassThru</span></span>
<span data-ttu-id="c8862-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="c8862-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c8862-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8862-127">-ResourceGroupName</span></span>
<span data-ttu-id="c8862-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-128">The name of the resource group.</span></span>
<span data-ttu-id="c8862-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c8862-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c8862-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8862-130">-SubscriptionId</span></span>
<span data-ttu-id="c8862-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="c8862-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c8862-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c8862-132">-Confirm</span></span>
<span data-ttu-id="c8862-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c8862-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8862-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8862-134">-WhatIf</span></span>
<span data-ttu-id="c8862-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8862-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8862-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8862-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8862-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8862-137">CommonParameters</span></span>
<span data-ttu-id="c8862-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8862-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8862-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8862-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8862-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c8862-140">INPUTS</span></span>

### <span data-ttu-id="c8862-141">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8862-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c8862-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c8862-142">OUTPUTS</span></span>

### <span data-ttu-id="c8862-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c8862-143">System.Boolean</span></span>

## <span data-ttu-id="c8862-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c8862-144">NOTES</span></span>

<span data-ttu-id="c8862-145">別名</span><span class="sxs-lookup"><span data-stu-id="c8862-145">ALIASES</span></span>

<span data-ttu-id="c8862-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c8862-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8862-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c8862-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8862-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c8862-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8862-149">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c8862-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8862-150">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c8862-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c8862-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c8862-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c8862-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8862-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c8862-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c8862-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c8862-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="c8862-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c8862-158">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c8862-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8862-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c8862-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8862-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c8862-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8862-161">RELATED LINKS</span></span>
