---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/start-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
ms.openlocfilehash: bdda5653a3b7f612fc96d3522bffe15e92649bbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129031"
---
# <span data-ttu-id="47229-101">Start-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="47229-101">Start-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="47229-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47229-102">SYNOPSIS</span></span>
<span data-ttu-id="47229-103">啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="47229-103">Starts a server.</span></span>

## <span data-ttu-id="47229-104">句法</span><span class="sxs-lookup"><span data-stu-id="47229-104">SYNTAX</span></span>

### <span data-ttu-id="47229-105">開始 (預設) </span><span class="sxs-lookup"><span data-stu-id="47229-105">Start (Default)</span></span>
```
Start-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47229-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47229-106">StartViaIdentity</span></span>
```
Start-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47229-107">說明</span><span class="sxs-lookup"><span data-stu-id="47229-107">DESCRIPTION</span></span>
<span data-ttu-id="47229-108">啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="47229-108">Starts a server.</span></span>

## <span data-ttu-id="47229-109">示例</span><span class="sxs-lookup"><span data-stu-id="47229-109">EXAMPLES</span></span>

### <span data-ttu-id="47229-110">範例1：依資源名稱啟動伺服器</span><span class="sxs-lookup"><span data-stu-id="47229-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="47229-111">依名稱啟動伺服器</span><span class="sxs-lookup"><span data-stu-id="47229-111">Start the server by name</span></span>

### <span data-ttu-id="47229-112">範例2：依身分識別啟動伺服器</span><span class="sxs-lookup"><span data-stu-id="47229-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/start"
PS C:\> Start-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="47229-113">依身分識別啟動伺服器</span><span class="sxs-lookup"><span data-stu-id="47229-113">Start the server by identity</span></span>

## <span data-ttu-id="47229-114">參數</span><span class="sxs-lookup"><span data-stu-id="47229-114">PARAMETERS</span></span>

### <span data-ttu-id="47229-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47229-115">-AsJob</span></span>
<span data-ttu-id="47229-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="47229-116">Run the command as a job</span></span>

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

### <span data-ttu-id="47229-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47229-117">-DefaultProfile</span></span>
<span data-ttu-id="47229-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="47229-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47229-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47229-119">-InputObject</span></span>
<span data-ttu-id="47229-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="47229-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47229-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="47229-121">-Name</span></span>
<span data-ttu-id="47229-122">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47229-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="47229-123">-NoWait</span></span>
<span data-ttu-id="47229-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="47229-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47229-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47229-125">-PassThru</span></span>
<span data-ttu-id="47229-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="47229-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="47229-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47229-127">-ResourceGroupName</span></span>
<span data-ttu-id="47229-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-128">The name of the resource group.</span></span>
<span data-ttu-id="47229-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="47229-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47229-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47229-130">-SubscriptionId</span></span>
<span data-ttu-id="47229-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="47229-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47229-132">-確認</span><span class="sxs-lookup"><span data-stu-id="47229-132">-Confirm</span></span>
<span data-ttu-id="47229-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="47229-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47229-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47229-134">-WhatIf</span></span>
<span data-ttu-id="47229-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47229-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47229-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47229-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47229-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47229-137">CommonParameters</span></span>
<span data-ttu-id="47229-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47229-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47229-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="47229-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47229-140">輸入</span><span class="sxs-lookup"><span data-stu-id="47229-140">INPUTS</span></span>

### <span data-ttu-id="47229-141">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="47229-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="47229-142">輸出</span><span class="sxs-lookup"><span data-stu-id="47229-142">OUTPUTS</span></span>

### <span data-ttu-id="47229-143">System.object</span><span class="sxs-lookup"><span data-stu-id="47229-143">System.Boolean</span></span>

## <span data-ttu-id="47229-144">筆記</span><span class="sxs-lookup"><span data-stu-id="47229-144">NOTES</span></span>

<span data-ttu-id="47229-145">別名</span><span class="sxs-lookup"><span data-stu-id="47229-145">ALIASES</span></span>

<span data-ttu-id="47229-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="47229-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47229-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="47229-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47229-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="47229-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47229-149">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="47229-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47229-150">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="47229-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="47229-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="47229-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="47229-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47229-154">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="47229-155">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="47229-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47229-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="47229-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="47229-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="47229-159">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="47229-160">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="47229-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47229-161">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="47229-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="47229-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="47229-162">RELATED LINKS</span></span>

