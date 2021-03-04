---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: e4ea7cf3b8f85b018ec087122bda8dcfeec066d7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915441"
---
# <span data-ttu-id="d0022-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d0022-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="d0022-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0022-102">SYNOPSIS</span></span>
<span data-ttu-id="d0022-103">刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="d0022-103">Deletes a server.</span></span>

## <span data-ttu-id="d0022-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0022-104">SYNTAX</span></span>

### <span data-ttu-id="d0022-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="d0022-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d0022-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d0022-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0022-107">描述</span><span class="sxs-lookup"><span data-stu-id="d0022-107">DESCRIPTION</span></span>
<span data-ttu-id="d0022-108">刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="d0022-108">Deletes a server.</span></span>

## <span data-ttu-id="d0022-109">例子</span><span class="sxs-lookup"><span data-stu-id="d0022-109">EXAMPLES</span></span>

### <span data-ttu-id="d0022-110">範例 1：移除 MariaDB</span><span class="sxs-lookup"><span data-stu-id="d0022-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="d0022-111">此命令會移除 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="d0022-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="d0022-112">範例 2：移除 MariaDB</span><span class="sxs-lookup"><span data-stu-id="d0022-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="d0022-113">此命令會移除 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="d0022-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="d0022-114">參數</span><span class="sxs-lookup"><span data-stu-id="d0022-114">PARAMETERS</span></span>

### <span data-ttu-id="d0022-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0022-115">-AsJob</span></span>
<span data-ttu-id="d0022-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="d0022-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d0022-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0022-117">-DefaultProfile</span></span>
<span data-ttu-id="d0022-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0022-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0022-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0022-119">-InputObject</span></span>
<span data-ttu-id="d0022-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d0022-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0022-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0022-121">-Name</span></span>
<span data-ttu-id="d0022-122">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-122">The name of the server.</span></span>

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

### <span data-ttu-id="d0022-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0022-123">-NoWait</span></span>
<span data-ttu-id="d0022-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="d0022-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0022-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0022-125">-PassThru</span></span>
<span data-ttu-id="d0022-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="d0022-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d0022-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0022-127">-ResourceGroupName</span></span>
<span data-ttu-id="d0022-128">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d0022-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d0022-129">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="d0022-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d0022-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0022-130">-SubscriptionId</span></span>
<span data-ttu-id="d0022-131">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0022-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d0022-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d0022-132">-Confirm</span></span>
<span data-ttu-id="d0022-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0022-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0022-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0022-134">-WhatIf</span></span>
<span data-ttu-id="d0022-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0022-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0022-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0022-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0022-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0022-137">CommonParameters</span></span>
<span data-ttu-id="d0022-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0022-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0022-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0022-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0022-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d0022-140">INPUTS</span></span>

### <span data-ttu-id="d0022-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.models.IAzaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d0022-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d0022-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d0022-142">OUTPUTS</span></span>

### <span data-ttu-id="d0022-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0022-143">System.Boolean</span></span>

## <span data-ttu-id="d0022-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d0022-144">NOTES</span></span>

<span data-ttu-id="d0022-145">別名</span><span class="sxs-lookup"><span data-stu-id="d0022-145">ALIASES</span></span>

<span data-ttu-id="d0022-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d0022-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d0022-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d0022-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d0022-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d0022-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d0022-149">INPUTOBJECT： <IMariaDbIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d0022-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d0022-150">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d0022-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d0022-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d0022-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="d0022-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d0022-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d0022-155">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d0022-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d0022-156">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="d0022-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d0022-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d0022-158">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d0022-159">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d0022-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d0022-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0022-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d0022-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0022-161">RELATED LINKS</span></span>

