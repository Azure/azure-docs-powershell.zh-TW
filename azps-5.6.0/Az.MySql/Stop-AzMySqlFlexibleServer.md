---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/stop-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Stop-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Stop-AzMySqlFlexibleServer.md
ms.openlocfilehash: f6b6549b415404d9c336890970ff29510ffba99f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906141"
---
# <span data-ttu-id="3f00c-101">Stop-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="3f00c-101">Stop-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="3f00c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f00c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f00c-103">停止伺服器。</span><span class="sxs-lookup"><span data-stu-id="3f00c-103">Stops a server.</span></span>

## <span data-ttu-id="3f00c-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f00c-104">SYNTAX</span></span>

### <span data-ttu-id="3f00c-105">停止 (預設) </span><span class="sxs-lookup"><span data-stu-id="3f00c-105">Stop (Default)</span></span>
```
Stop-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3f00c-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f00c-106">StopViaIdentity</span></span>
```
Stop-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3f00c-107">描述</span><span class="sxs-lookup"><span data-stu-id="3f00c-107">DESCRIPTION</span></span>
<span data-ttu-id="3f00c-108">停止伺服器。</span><span class="sxs-lookup"><span data-stu-id="3f00c-108">Stops a server.</span></span>

## <span data-ttu-id="3f00c-109">例子</span><span class="sxs-lookup"><span data-stu-id="3f00c-109">EXAMPLES</span></span>

### <span data-ttu-id="3f00c-110">範例 1：根據資源名稱停止伺服器</span><span class="sxs-lookup"><span data-stu-id="3f00c-110">Example 1: Stop the server by resource name</span></span>
```powershell
PS C:\> Stop-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="3f00c-111">以名稱停止伺服器</span><span class="sxs-lookup"><span data-stu-id="3f00c-111">Stop the server by name</span></span>

### <span data-ttu-id="3f00c-112">範例 2：以身分識別停止伺服器</span><span class="sxs-lookup"><span data-stu-id="3f00c-112">Example 2: Stop the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/stop"
PS C:\> Stop-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="3f00c-113">以身分識別停止伺服器</span><span class="sxs-lookup"><span data-stu-id="3f00c-113">Stop the server by identity</span></span>

## <span data-ttu-id="3f00c-114">參數</span><span class="sxs-lookup"><span data-stu-id="3f00c-114">PARAMETERS</span></span>

### <span data-ttu-id="3f00c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f00c-115">-AsJob</span></span>
<span data-ttu-id="3f00c-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="3f00c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3f00c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f00c-117">-DefaultProfile</span></span>
<span data-ttu-id="3f00c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f00c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f00c-119">-InputObject</span></span>
<span data-ttu-id="3f00c-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3f00c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f00c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f00c-121">-Name</span></span>
<span data-ttu-id="3f00c-122">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f00c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3f00c-123">-NoWait</span></span>
<span data-ttu-id="3f00c-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="3f00c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3f00c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f00c-125">-PassThru</span></span>
<span data-ttu-id="3f00c-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="3f00c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3f00c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f00c-127">-ResourceGroupName</span></span>
<span data-ttu-id="3f00c-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-128">The name of the resource group.</span></span>
<span data-ttu-id="3f00c-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3f00c-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f00c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f00c-130">-SubscriptionId</span></span>
<span data-ttu-id="3f00c-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f00c-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f00c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="3f00c-132">-Confirm</span></span>
<span data-ttu-id="3f00c-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3f00c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f00c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f00c-134">-WhatIf</span></span>
<span data-ttu-id="3f00c-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f00c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f00c-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f00c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f00c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f00c-137">CommonParameters</span></span>
<span data-ttu-id="3f00c-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f00c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f00c-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f00c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f00c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3f00c-140">INPUTS</span></span>

### <span data-ttu-id="3f00c-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3f00c-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3f00c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3f00c-142">OUTPUTS</span></span>

### <span data-ttu-id="3f00c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f00c-143">System.Boolean</span></span>

## <span data-ttu-id="3f00c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3f00c-144">NOTES</span></span>

<span data-ttu-id="3f00c-145">別名</span><span class="sxs-lookup"><span data-stu-id="3f00c-145">ALIASES</span></span>

<span data-ttu-id="3f00c-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3f00c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3f00c-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3f00c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f00c-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3f00c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3f00c-149">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3f00c-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f00c-150">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3f00c-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3f00c-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3f00c-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3f00c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f00c-154">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="3f00c-155">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3f00c-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3f00c-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3f00c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="3f00c-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3f00c-159">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3f00c-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f00c-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3f00c-161">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f00c-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3f00c-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f00c-162">RELATED LINKS</span></span>

