---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129469"
---
# <span data-ttu-id="52656-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="52656-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="52656-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52656-102">SYNOPSIS</span></span>
<span data-ttu-id="52656-103">重新開機伺服器。</span><span class="sxs-lookup"><span data-stu-id="52656-103">Restarts a server.</span></span>

## <span data-ttu-id="52656-104">句法</span><span class="sxs-lookup"><span data-stu-id="52656-104">SYNTAX</span></span>

### <span data-ttu-id="52656-105">ServerName (預設) </span><span class="sxs-lookup"><span data-stu-id="52656-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52656-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="52656-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52656-107">說明</span><span class="sxs-lookup"><span data-stu-id="52656-107">DESCRIPTION</span></span>
<span data-ttu-id="52656-108">重新開機伺服器。</span><span class="sxs-lookup"><span data-stu-id="52656-108">Restarts a server.</span></span>

## <span data-ttu-id="52656-109">示例</span><span class="sxs-lookup"><span data-stu-id="52656-109">EXAMPLES</span></span>

### <span data-ttu-id="52656-110">範例1：重新開機 MariaDB</span><span class="sxs-lookup"><span data-stu-id="52656-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="52656-111">這個命令會重新開機 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="52656-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="52656-112">範例2：重新開機 MariaDB</span><span class="sxs-lookup"><span data-stu-id="52656-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="52656-113">這個命令會重新開機 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="52656-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="52656-114">參數</span><span class="sxs-lookup"><span data-stu-id="52656-114">PARAMETERS</span></span>

### <span data-ttu-id="52656-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52656-115">-AsJob</span></span>
<span data-ttu-id="52656-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="52656-116">Run the command as a job</span></span>

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

### <span data-ttu-id="52656-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52656-117">-DefaultProfile</span></span>
<span data-ttu-id="52656-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52656-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52656-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52656-119">-InputObject</span></span>
<span data-ttu-id="52656-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="52656-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52656-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="52656-121">-Name</span></span>
<span data-ttu-id="52656-122">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52656-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="52656-123">-NoWait</span></span>
<span data-ttu-id="52656-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="52656-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52656-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52656-125">-PassThru</span></span>
<span data-ttu-id="52656-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="52656-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="52656-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52656-127">-ResourceGroupName</span></span>
<span data-ttu-id="52656-128">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="52656-129">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="52656-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52656-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52656-130">-SubscriptionId</span></span>
<span data-ttu-id="52656-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="52656-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52656-132">-確認</span><span class="sxs-lookup"><span data-stu-id="52656-132">-Confirm</span></span>
<span data-ttu-id="52656-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52656-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52656-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52656-134">-WhatIf</span></span>
<span data-ttu-id="52656-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52656-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52656-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52656-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52656-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52656-137">CommonParameters</span></span>
<span data-ttu-id="52656-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52656-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52656-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="52656-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52656-140">輸入</span><span class="sxs-lookup"><span data-stu-id="52656-140">INPUTS</span></span>

### <span data-ttu-id="52656-141">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="52656-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="52656-142">輸出</span><span class="sxs-lookup"><span data-stu-id="52656-142">OUTPUTS</span></span>

### <span data-ttu-id="52656-143">System.object</span><span class="sxs-lookup"><span data-stu-id="52656-143">System.Boolean</span></span>

## <span data-ttu-id="52656-144">筆記</span><span class="sxs-lookup"><span data-stu-id="52656-144">NOTES</span></span>

<span data-ttu-id="52656-145">別名</span><span class="sxs-lookup"><span data-stu-id="52656-145">ALIASES</span></span>

<span data-ttu-id="52656-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="52656-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52656-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="52656-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52656-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="52656-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52656-149">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="52656-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52656-150">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="52656-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="52656-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="52656-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="52656-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52656-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="52656-155">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="52656-156">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="52656-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="52656-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="52656-158">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="52656-159">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="52656-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="52656-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="52656-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="52656-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="52656-161">RELATED LINKS</span></span>
