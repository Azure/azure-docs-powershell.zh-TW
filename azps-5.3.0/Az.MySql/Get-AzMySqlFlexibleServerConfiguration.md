---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435282"
---
# <span data-ttu-id="a95dd-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a95dd-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a95dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a95dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a95dd-103">取得伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a95dd-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a95dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="a95dd-104">SYNTAX</span></span>

### <span data-ttu-id="a95dd-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="a95dd-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a95dd-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a95dd-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a95dd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a95dd-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a95dd-108">說明</span><span class="sxs-lookup"><span data-stu-id="a95dd-108">DESCRIPTION</span></span>
<span data-ttu-id="a95dd-109">取得伺服器設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a95dd-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a95dd-110">示例</span><span class="sxs-lookup"><span data-stu-id="a95dd-110">EXAMPLES</span></span>

### <span data-ttu-id="a95dd-111">範例1：列出指定 MySql 伺服器中的所有配置</span><span class="sxs-lookup"><span data-stu-id="a95dd-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a95dd-112">這個 Cmdlet 會列出指定 MySql 伺服器中的所有設定。</span><span class="sxs-lookup"><span data-stu-id="a95dd-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="a95dd-113">範例2：依名稱取得指定的 MySql 配置</span><span class="sxs-lookup"><span data-stu-id="a95dd-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a95dd-114">這個 Cmdlet 透過名稱取得指定的 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="a95dd-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="a95dd-115">範例3：依身分識別列出配置</span><span class="sxs-lookup"><span data-stu-id="a95dd-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a95dd-116">這個 Cmdlet 透過身分識別來取得指定的 MySql 配置。</span><span class="sxs-lookup"><span data-stu-id="a95dd-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="a95dd-117">參數</span><span class="sxs-lookup"><span data-stu-id="a95dd-117">PARAMETERS</span></span>

### <span data-ttu-id="a95dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95dd-118">-DefaultProfile</span></span>
<span data-ttu-id="a95dd-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95dd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a95dd-120">-InputObject</span></span>
<span data-ttu-id="a95dd-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a95dd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a95dd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a95dd-122">-Name</span></span>
<span data-ttu-id="a95dd-123">伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="a95dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="a95dd-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-125">The name of the resource group.</span></span>
<span data-ttu-id="a95dd-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a95dd-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a95dd-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a95dd-127">-ServerName</span></span>
<span data-ttu-id="a95dd-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-128">The name of the server.</span></span>

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

### <span data-ttu-id="a95dd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a95dd-129">-SubscriptionId</span></span>
<span data-ttu-id="a95dd-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="a95dd-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a95dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95dd-131">CommonParameters</span></span>
<span data-ttu-id="a95dd-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a95dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95dd-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a95dd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95dd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a95dd-134">INPUTS</span></span>

### <span data-ttu-id="a95dd-135">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a95dd-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a95dd-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a95dd-136">OUTPUTS</span></span>

### <span data-ttu-id="a95dd-137">IConfigurationAutoGenerated 中的 Api20200701Preview （）。</span><span class="sxs-lookup"><span data-stu-id="a95dd-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a95dd-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a95dd-138">NOTES</span></span>

<span data-ttu-id="a95dd-139">別名</span><span class="sxs-lookup"><span data-stu-id="a95dd-139">ALIASES</span></span>

<span data-ttu-id="a95dd-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a95dd-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a95dd-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a95dd-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a95dd-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a95dd-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a95dd-143">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a95dd-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a95dd-144">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a95dd-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a95dd-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a95dd-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a95dd-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a95dd-148">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a95dd-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a95dd-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a95dd-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a95dd-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a95dd-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a95dd-153">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a95dd-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a95dd-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a95dd-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a95dd-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a95dd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a95dd-156">RELATED LINKS</span></span>

