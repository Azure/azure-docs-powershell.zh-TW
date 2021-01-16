---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: c495cb1372735c856224d45010728f264f73c252
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280697"
---
# <span data-ttu-id="b1b98-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="b1b98-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="b1b98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1b98-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b98-103">刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1b98-103">Deletes a server.</span></span>

## <span data-ttu-id="b1b98-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1b98-104">SYNTAX</span></span>

### <span data-ttu-id="b1b98-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b1b98-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1b98-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b1b98-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1b98-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1b98-107">DESCRIPTION</span></span>
<span data-ttu-id="b1b98-108">刪除伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1b98-108">Deletes a server.</span></span>

## <span data-ttu-id="b1b98-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1b98-109">EXAMPLES</span></span>

### <span data-ttu-id="b1b98-110">範例1：移除 MariaDB</span><span class="sxs-lookup"><span data-stu-id="b1b98-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="b1b98-111">這個命令會移除 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="b1b98-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="b1b98-112">範例2：移除 MariaDB</span><span class="sxs-lookup"><span data-stu-id="b1b98-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="b1b98-113">這個命令會移除 MariaDB。</span><span class="sxs-lookup"><span data-stu-id="b1b98-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="b1b98-114">參數</span><span class="sxs-lookup"><span data-stu-id="b1b98-114">PARAMETERS</span></span>

### <span data-ttu-id="b1b98-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1b98-115">-AsJob</span></span>
<span data-ttu-id="b1b98-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b1b98-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b1b98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b98-117">-DefaultProfile</span></span>
<span data-ttu-id="b1b98-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b98-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1b98-119">-InputObject</span></span>
<span data-ttu-id="b1b98-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1b98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1b98-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1b98-121">-Name</span></span>
<span data-ttu-id="b1b98-122">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-122">The name of the server.</span></span>

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

### <span data-ttu-id="b1b98-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1b98-123">-NoWait</span></span>
<span data-ttu-id="b1b98-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b1b98-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b1b98-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1b98-125">-PassThru</span></span>
<span data-ttu-id="b1b98-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b1b98-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b1b98-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b98-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1b98-128">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b1b98-129">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b1b98-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b1b98-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1b98-130">-SubscriptionId</span></span>
<span data-ttu-id="b1b98-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b1b98-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b1b98-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b1b98-132">-Confirm</span></span>
<span data-ttu-id="b1b98-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1b98-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b98-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b98-134">-WhatIf</span></span>
<span data-ttu-id="b1b98-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1b98-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b98-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1b98-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b98-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b98-137">CommonParameters</span></span>
<span data-ttu-id="b1b98-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1b98-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b98-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1b98-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b98-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b1b98-140">INPUTS</span></span>

### <span data-ttu-id="b1b98-141">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="b1b98-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b1b98-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b1b98-142">OUTPUTS</span></span>

### <span data-ttu-id="b1b98-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b1b98-143">System.Boolean</span></span>

## <span data-ttu-id="b1b98-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b1b98-144">NOTES</span></span>

<span data-ttu-id="b1b98-145">別名</span><span class="sxs-lookup"><span data-stu-id="b1b98-145">ALIASES</span></span>

<span data-ttu-id="b1b98-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b1b98-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1b98-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b1b98-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1b98-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b1b98-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1b98-149">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b1b98-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1b98-150">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b1b98-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b1b98-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b1b98-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b1b98-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1b98-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b1b98-155">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b1b98-156">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b1b98-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b1b98-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b1b98-158">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b1b98-159">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b1b98-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b1b98-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1b98-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b1b98-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1b98-161">RELATED LINKS</span></span>

