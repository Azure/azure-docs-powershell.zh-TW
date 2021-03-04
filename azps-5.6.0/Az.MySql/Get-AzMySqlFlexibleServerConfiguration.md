---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 8dca573eb0d527beb08bb591b0c8fa3b2fc6e30a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916921"
---
# <span data-ttu-id="cbac8-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbac8-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="cbac8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cbac8-102">SYNOPSIS</span></span>
<span data-ttu-id="cbac8-103">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="cbac8-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="cbac8-104">語法</span><span class="sxs-lookup"><span data-stu-id="cbac8-104">SYNTAX</span></span>

### <span data-ttu-id="cbac8-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="cbac8-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbac8-106">獲取</span><span class="sxs-lookup"><span data-stu-id="cbac8-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbac8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cbac8-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbac8-108">描述</span><span class="sxs-lookup"><span data-stu-id="cbac8-108">DESCRIPTION</span></span>
<span data-ttu-id="cbac8-109">獲得伺服器組配置的資訊。</span><span class="sxs-lookup"><span data-stu-id="cbac8-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="cbac8-110">例子</span><span class="sxs-lookup"><span data-stu-id="cbac8-110">EXAMPLES</span></span>

### <span data-ttu-id="cbac8-111">範例 1：列出指定 MySql 伺服器的所有組配置</span><span class="sxs-lookup"><span data-stu-id="cbac8-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="cbac8-112">此 Cmdlet 會列出指定 MySql 伺服器的所有組配置。</span><span class="sxs-lookup"><span data-stu-id="cbac8-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="cbac8-113">範例 2：根據名稱取得指定的 MySql 組配置</span><span class="sxs-lookup"><span data-stu-id="cbac8-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="cbac8-114">此 Cmdlet 會以名稱指定 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="cbac8-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="cbac8-115">範例 3：按身分識別列出組組</span><span class="sxs-lookup"><span data-stu-id="cbac8-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="cbac8-116">此 Cmdlet 會以身分識別指定 MySql 組配置。</span><span class="sxs-lookup"><span data-stu-id="cbac8-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="cbac8-117">參數</span><span class="sxs-lookup"><span data-stu-id="cbac8-117">PARAMETERS</span></span>

### <span data-ttu-id="cbac8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbac8-118">-DefaultProfile</span></span>
<span data-ttu-id="cbac8-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbac8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbac8-120">-InputObject</span></span>
<span data-ttu-id="cbac8-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbac8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbac8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbac8-122">-Name</span></span>
<span data-ttu-id="cbac8-123">伺服器組名。</span><span class="sxs-lookup"><span data-stu-id="cbac8-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="cbac8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbac8-124">-ResourceGroupName</span></span>
<span data-ttu-id="cbac8-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-125">The name of the resource group.</span></span>
<span data-ttu-id="cbac8-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cbac8-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cbac8-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbac8-127">-ServerName</span></span>
<span data-ttu-id="cbac8-128">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-128">The name of the server.</span></span>

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

### <span data-ttu-id="cbac8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbac8-129">-SubscriptionId</span></span>
<span data-ttu-id="cbac8-130">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbac8-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cbac8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbac8-131">CommonParameters</span></span>
<span data-ttu-id="cbac8-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cbac8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbac8-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbac8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbac8-134">輸入</span><span class="sxs-lookup"><span data-stu-id="cbac8-134">INPUTS</span></span>

### <span data-ttu-id="cbac8-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cbac8-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="cbac8-136">輸出</span><span class="sxs-lookup"><span data-stu-id="cbac8-136">OUTPUTS</span></span>

### <span data-ttu-id="cbac8-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="cbac8-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="cbac8-138">筆記</span><span class="sxs-lookup"><span data-stu-id="cbac8-138">NOTES</span></span>

<span data-ttu-id="cbac8-139">別名</span><span class="sxs-lookup"><span data-stu-id="cbac8-139">ALIASES</span></span>

<span data-ttu-id="cbac8-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cbac8-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbac8-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cbac8-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbac8-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cbac8-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbac8-143">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cbac8-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbac8-144">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cbac8-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cbac8-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cbac8-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="cbac8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbac8-148">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="cbac8-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cbac8-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cbac8-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cbac8-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="cbac8-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cbac8-153">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cbac8-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cbac8-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cbac8-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbac8-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cbac8-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbac8-156">RELATED LINKS</span></span>

