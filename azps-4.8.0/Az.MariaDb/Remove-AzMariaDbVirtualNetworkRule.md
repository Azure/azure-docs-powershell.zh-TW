---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 474b4dc71658c1b8d79577f029d7ce0e098cca91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970999"
---
# <span data-ttu-id="84090-101">Remove-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="84090-101">Remove-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="84090-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84090-102">SYNOPSIS</span></span>
<span data-ttu-id="84090-103">刪除具有指定名稱的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="84090-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="84090-104">句法</span><span class="sxs-lookup"><span data-stu-id="84090-104">SYNTAX</span></span>

### <span data-ttu-id="84090-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="84090-105">Delete (Default)</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="84090-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="84090-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84090-107">說明</span><span class="sxs-lookup"><span data-stu-id="84090-107">DESCRIPTION</span></span>
<span data-ttu-id="84090-108">刪除具有指定名稱的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="84090-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="84090-109">示例</span><span class="sxs-lookup"><span data-stu-id="84090-109">EXAMPLES</span></span>

### <span data-ttu-id="84090-110">範例1：移除虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="84090-110">Example 1: Remove a virtual network rule</span></span>
```powershell
PS C:\> Remove-AzMariaDbVirtualNetworkRule -Name vnet-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

```

<span data-ttu-id="84090-111">這個命令會移除虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="84090-111">This command removes a virtual network rule.</span></span>

## <span data-ttu-id="84090-112">參數</span><span class="sxs-lookup"><span data-stu-id="84090-112">PARAMETERS</span></span>

### <span data-ttu-id="84090-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84090-113">-AsJob</span></span>
<span data-ttu-id="84090-114">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="84090-114">Run the command as a job</span></span>

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

### <span data-ttu-id="84090-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84090-115">-DefaultProfile</span></span>
<span data-ttu-id="84090-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84090-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84090-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84090-117">-InputObject</span></span>
<span data-ttu-id="84090-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="84090-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="84090-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="84090-119">-Name</span></span>
<span data-ttu-id="84090-120">虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-120">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="84090-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84090-121">-NoWait</span></span>
<span data-ttu-id="84090-122">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="84090-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="84090-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84090-123">-PassThru</span></span>
<span data-ttu-id="84090-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="84090-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="84090-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84090-125">-ResourceGroupName</span></span>
<span data-ttu-id="84090-126">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="84090-127">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="84090-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="84090-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="84090-128">-ServerName</span></span>
<span data-ttu-id="84090-129">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-129">The name of the server.</span></span>

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

### <span data-ttu-id="84090-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84090-130">-SubscriptionId</span></span>
<span data-ttu-id="84090-131">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="84090-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="84090-132">-確認</span><span class="sxs-lookup"><span data-stu-id="84090-132">-Confirm</span></span>
<span data-ttu-id="84090-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84090-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84090-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84090-134">-WhatIf</span></span>
<span data-ttu-id="84090-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84090-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84090-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84090-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84090-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84090-137">CommonParameters</span></span>
<span data-ttu-id="84090-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84090-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84090-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="84090-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84090-140">輸入</span><span class="sxs-lookup"><span data-stu-id="84090-140">INPUTS</span></span>

### <span data-ttu-id="84090-141">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="84090-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="84090-142">輸出</span><span class="sxs-lookup"><span data-stu-id="84090-142">OUTPUTS</span></span>

### <span data-ttu-id="84090-143">System.object</span><span class="sxs-lookup"><span data-stu-id="84090-143">System.Boolean</span></span>

## <span data-ttu-id="84090-144">筆記</span><span class="sxs-lookup"><span data-stu-id="84090-144">NOTES</span></span>

<span data-ttu-id="84090-145">別名</span><span class="sxs-lookup"><span data-stu-id="84090-145">ALIASES</span></span>

<span data-ttu-id="84090-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="84090-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84090-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="84090-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84090-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="84090-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84090-149">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="84090-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="84090-150">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="84090-151">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="84090-152">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="84090-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="84090-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="84090-154">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="84090-155">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="84090-156">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="84090-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="84090-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="84090-158">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="84090-159">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="84090-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="84090-160">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="84090-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="84090-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="84090-161">RELATED LINKS</span></span>
