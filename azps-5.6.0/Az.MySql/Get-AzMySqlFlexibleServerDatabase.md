---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: b060657d9e8d69ebddf639847de7718ec626fdb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911918"
---
# <span data-ttu-id="240b8-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="240b8-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="240b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="240b8-102">SYNOPSIS</span></span>
<span data-ttu-id="240b8-103">獲得資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="240b8-103">Gets information about a database.</span></span>

## <span data-ttu-id="240b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="240b8-104">SYNTAX</span></span>

### <span data-ttu-id="240b8-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="240b8-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="240b8-106">獲取</span><span class="sxs-lookup"><span data-stu-id="240b8-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="240b8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="240b8-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="240b8-108">描述</span><span class="sxs-lookup"><span data-stu-id="240b8-108">DESCRIPTION</span></span>
<span data-ttu-id="240b8-109">獲得資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="240b8-109">Gets information about a database.</span></span>

## <span data-ttu-id="240b8-110">例子</span><span class="sxs-lookup"><span data-stu-id="240b8-110">EXAMPLES</span></span>

### <span data-ttu-id="240b8-111">範例 1：根據資源名稱取得 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="240b8-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="240b8-112">此 Cmdlet 會按資源名稱獲得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="240b8-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="240b8-113">範例 2：根據身分識別取得 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="240b8-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="240b8-114">此 Cmdlet 會以身分識別獲得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="240b8-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="240b8-115">範例 3：列出指定伺服器中所有的 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="240b8-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="240b8-116">此 Cmdlet 會列出指定伺服器中所有的 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="240b8-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="240b8-117">參數</span><span class="sxs-lookup"><span data-stu-id="240b8-117">PARAMETERS</span></span>

### <span data-ttu-id="240b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="240b8-118">-DefaultProfile</span></span>
<span data-ttu-id="240b8-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="240b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="240b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="240b8-120">-InputObject</span></span>
<span data-ttu-id="240b8-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="240b8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="240b8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="240b8-122">-Name</span></span>
<span data-ttu-id="240b8-123">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="240b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="240b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="240b8-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-125">The name of the resource group.</span></span>
<span data-ttu-id="240b8-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="240b8-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="240b8-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="240b8-127">-ServerName</span></span>
<span data-ttu-id="240b8-128">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-128">The name of the server.</span></span>

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

### <span data-ttu-id="240b8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="240b8-129">-SubscriptionId</span></span>
<span data-ttu-id="240b8-130">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="240b8-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="240b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="240b8-131">CommonParameters</span></span>
<span data-ttu-id="240b8-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="240b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="240b8-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="240b8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="240b8-134">輸入</span><span class="sxs-lookup"><span data-stu-id="240b8-134">INPUTS</span></span>

### <span data-ttu-id="240b8-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="240b8-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="240b8-136">輸出</span><span class="sxs-lookup"><span data-stu-id="240b8-136">OUTPUTS</span></span>

### <span data-ttu-id="240b8-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="240b8-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="240b8-138">筆記</span><span class="sxs-lookup"><span data-stu-id="240b8-138">NOTES</span></span>

<span data-ttu-id="240b8-139">別名</span><span class="sxs-lookup"><span data-stu-id="240b8-139">ALIASES</span></span>

<span data-ttu-id="240b8-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="240b8-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="240b8-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="240b8-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="240b8-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="240b8-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="240b8-143">INPUTOBJECT： <IMySqlIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="240b8-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="240b8-144">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="240b8-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="240b8-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="240b8-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="240b8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="240b8-148">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="240b8-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="240b8-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="240b8-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="240b8-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="240b8-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="240b8-153">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="240b8-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="240b8-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="240b8-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="240b8-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="240b8-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="240b8-156">RELATED LINKS</span></span>

