---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438024"
---
# <span data-ttu-id="71e68-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="71e68-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="71e68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71e68-102">SYNOPSIS</span></span>
<span data-ttu-id="71e68-103">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="71e68-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="71e68-104">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzMariaDbServer]。</span><span class="sxs-lookup"><span data-stu-id="71e68-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="71e68-105">句法</span><span class="sxs-lookup"><span data-stu-id="71e68-105">SYNTAX</span></span>

### <span data-ttu-id="71e68-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="71e68-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71e68-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="71e68-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71e68-108">說明</span><span class="sxs-lookup"><span data-stu-id="71e68-108">DESCRIPTION</span></span>
<span data-ttu-id="71e68-109">補救伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="71e68-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="71e68-110">如果您想要更新 AdministratorLoginPassword、sku 等，請改用 [Update-AzMariaDberver]。</span><span class="sxs-lookup"><span data-stu-id="71e68-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="71e68-111">示例</span><span class="sxs-lookup"><span data-stu-id="71e68-111">EXAMPLES</span></span>

### <span data-ttu-id="71e68-112">範例1：更新 MariaDB 設定</span><span class="sxs-lookup"><span data-stu-id="71e68-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="71e68-113">這個命令會更新 MariaDB 設定。</span><span class="sxs-lookup"><span data-stu-id="71e68-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="71e68-114">參數</span><span class="sxs-lookup"><span data-stu-id="71e68-114">PARAMETERS</span></span>

### <span data-ttu-id="71e68-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71e68-115">-AsJob</span></span>
<span data-ttu-id="71e68-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="71e68-116">Run the command as a job</span></span>

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

### <span data-ttu-id="71e68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e68-117">-DefaultProfile</span></span>
<span data-ttu-id="71e68-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71e68-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71e68-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71e68-119">-InputObject</span></span>
<span data-ttu-id="71e68-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="71e68-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="71e68-121">-Name</span></span>
<span data-ttu-id="71e68-122">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-122">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71e68-123">-NoWait</span></span>
<span data-ttu-id="71e68-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="71e68-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71e68-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e68-125">-ResourceGroupName</span></span>
<span data-ttu-id="71e68-126">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="71e68-127">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="71e68-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71e68-128">-ServerName</span></span>
<span data-ttu-id="71e68-129">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-130">-來源</span><span class="sxs-lookup"><span data-stu-id="71e68-130">-Source</span></span>
<span data-ttu-id="71e68-131">配置來源。</span><span class="sxs-lookup"><span data-stu-id="71e68-131">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71e68-132">-SubscriptionId</span></span>
<span data-ttu-id="71e68-133">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="71e68-133">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-134">-值</span><span class="sxs-lookup"><span data-stu-id="71e68-134">-Value</span></span>
<span data-ttu-id="71e68-135">配置的值。</span><span class="sxs-lookup"><span data-stu-id="71e68-135">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e68-136">-確認</span><span class="sxs-lookup"><span data-stu-id="71e68-136">-Confirm</span></span>
<span data-ttu-id="71e68-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71e68-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e68-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e68-138">-WhatIf</span></span>
<span data-ttu-id="71e68-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71e68-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71e68-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71e68-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e68-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e68-141">CommonParameters</span></span>
<span data-ttu-id="71e68-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71e68-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e68-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71e68-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e68-144">輸入</span><span class="sxs-lookup"><span data-stu-id="71e68-144">INPUTS</span></span>

### <span data-ttu-id="71e68-145">IMariaDbIdentity （MariaDb）的</span><span class="sxs-lookup"><span data-stu-id="71e68-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="71e68-146">輸出</span><span class="sxs-lookup"><span data-stu-id="71e68-146">OUTPUTS</span></span>

### <span data-ttu-id="71e68-147">IConfiguration （MariaDb）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="71e68-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="71e68-148">筆記</span><span class="sxs-lookup"><span data-stu-id="71e68-148">NOTES</span></span>

<span data-ttu-id="71e68-149">別名</span><span class="sxs-lookup"><span data-stu-id="71e68-149">ALIASES</span></span>

<span data-ttu-id="71e68-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="71e68-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71e68-151">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="71e68-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71e68-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="71e68-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71e68-153">INPUTOBJECT <IMariaDbIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="71e68-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71e68-154">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="71e68-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="71e68-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="71e68-157">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="71e68-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71e68-158">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="71e68-159">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="71e68-160">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="71e68-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="71e68-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="71e68-162">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="71e68-163">`[SubscriptionId <String>]`：識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="71e68-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="71e68-164">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e68-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="71e68-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="71e68-165">RELATED LINKS</span></span>

