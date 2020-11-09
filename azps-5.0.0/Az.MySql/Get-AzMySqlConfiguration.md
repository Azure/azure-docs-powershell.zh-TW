---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286976"
---
# <span data-ttu-id="ebbd0-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebbd0-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="ebbd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbd0-103">取得伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="ebbd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebbd0-104">SYNTAX</span></span>

### <span data-ttu-id="ebbd0-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="ebbd0-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ebbd0-106">獲取</span><span class="sxs-lookup"><span data-stu-id="ebbd0-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ebbd0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ebbd0-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ebbd0-108">說明</span><span class="sxs-lookup"><span data-stu-id="ebbd0-108">DESCRIPTION</span></span>
<span data-ttu-id="ebbd0-109">取得伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="ebbd0-110">示例</span><span class="sxs-lookup"><span data-stu-id="ebbd0-110">EXAMPLES</span></span>

### <span data-ttu-id="ebbd0-111">範例1：列出指定 MySql 伺服器中的所有配置</span><span class="sxs-lookup"><span data-stu-id="ebbd0-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="ebbd0-112">這個 Cmdlet 會列出指定 MySql 伺服器中的所有設定。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="ebbd0-113">範例2：依名稱取得指定的 MySql 配置</span><span class="sxs-lookup"><span data-stu-id="ebbd0-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="ebbd0-114">這個 Cmdlet 透過名稱取得指定的 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="ebbd0-115">參數</span><span class="sxs-lookup"><span data-stu-id="ebbd0-115">PARAMETERS</span></span>

### <span data-ttu-id="ebbd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbd0-116">-DefaultProfile</span></span>
<span data-ttu-id="ebbd0-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebbd0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebbd0-118">-InputObject</span></span>
<span data-ttu-id="ebbd0-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebbd0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebbd0-120">-Name</span></span>
<span data-ttu-id="ebbd0-121">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbd0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbd0-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebbd0-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-123">The name of the resource group.</span></span>
<span data-ttu-id="ebbd0-124">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-124">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbd0-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ebbd0-125">-ServerName</span></span>
<span data-ttu-id="ebbd0-126">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbd0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebbd0-127">-SubscriptionId</span></span>
<span data-ttu-id="ebbd0-128">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbd0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbd0-129">CommonParameters</span></span>
<span data-ttu-id="ebbd0-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbd0-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbd0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ebbd0-132">INPUTS</span></span>

### <span data-ttu-id="ebbd0-133">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ebbd0-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ebbd0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ebbd0-134">OUTPUTS</span></span>

### <span data-ttu-id="ebbd0-135">IConfiguration 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="ebbd0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ebbd0-136">NOTES</span></span>

<span data-ttu-id="ebbd0-137">別名</span><span class="sxs-lookup"><span data-stu-id="ebbd0-137">ALIASES</span></span>

<span data-ttu-id="ebbd0-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ebbd0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ebbd0-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebbd0-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ebbd0-141">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ebbd0-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebbd0-142">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ebbd0-143">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ebbd0-144">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ebbd0-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ebbd0-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebbd0-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ebbd0-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ebbd0-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="ebbd0-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ebbd0-150">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ebbd0-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ebbd0-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebbd0-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ebbd0-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebbd0-153">RELATED LINKS</span></span>

