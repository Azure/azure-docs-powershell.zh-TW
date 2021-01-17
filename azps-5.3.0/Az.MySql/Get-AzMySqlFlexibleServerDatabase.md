---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436900"
---
# <span data-ttu-id="a1cac-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="a1cac-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="a1cac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1cac-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cac-103">取得資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1cac-103">Gets information about a database.</span></span>

## <span data-ttu-id="a1cac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1cac-104">SYNTAX</span></span>

### <span data-ttu-id="a1cac-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="a1cac-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1cac-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a1cac-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1cac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1cac-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1cac-108">說明</span><span class="sxs-lookup"><span data-stu-id="a1cac-108">DESCRIPTION</span></span>
<span data-ttu-id="a1cac-109">取得資料庫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a1cac-109">Gets information about a database.</span></span>

## <span data-ttu-id="a1cac-110">示例</span><span class="sxs-lookup"><span data-stu-id="a1cac-110">EXAMPLES</span></span>

### <span data-ttu-id="a1cac-111">範例1：透過資源名稱取得 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="a1cac-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="a1cac-112">這個 Cmdlet 透過資源名稱取得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a1cac-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="a1cac-113">範例2：透過身分識別取得 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="a1cac-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="a1cac-114">這個 Cmdlet 透過身分識別取得 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a1cac-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="a1cac-115">範例3：列出指定伺服器中的所有 MySql 資料庫</span><span class="sxs-lookup"><span data-stu-id="a1cac-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="a1cac-116">這個 Cmdlet 會列出指定伺服器中的所有 MySql 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a1cac-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="a1cac-117">參數</span><span class="sxs-lookup"><span data-stu-id="a1cac-117">PARAMETERS</span></span>

### <span data-ttu-id="a1cac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cac-118">-DefaultProfile</span></span>
<span data-ttu-id="a1cac-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1cac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1cac-120">-InputObject</span></span>
<span data-ttu-id="a1cac-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1cac-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1cac-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1cac-122">-Name</span></span>
<span data-ttu-id="a1cac-123">資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-123">The name of the database.</span></span>

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

### <span data-ttu-id="a1cac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1cac-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1cac-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-125">The name of the resource group.</span></span>
<span data-ttu-id="a1cac-126">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1cac-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a1cac-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a1cac-127">-ServerName</span></span>
<span data-ttu-id="a1cac-128">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-128">The name of the server.</span></span>

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

### <span data-ttu-id="a1cac-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1cac-129">-SubscriptionId</span></span>
<span data-ttu-id="a1cac-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="a1cac-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a1cac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cac-131">CommonParameters</span></span>
<span data-ttu-id="a1cac-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1cac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cac-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1cac-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cac-134">輸入</span><span class="sxs-lookup"><span data-stu-id="a1cac-134">INPUTS</span></span>

### <span data-ttu-id="a1cac-135">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a1cac-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a1cac-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a1cac-136">OUTPUTS</span></span>

### <span data-ttu-id="a1cac-137">IDatabase 中的 Api20171201 （）。</span><span class="sxs-lookup"><span data-stu-id="a1cac-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="a1cac-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a1cac-138">NOTES</span></span>

<span data-ttu-id="a1cac-139">別名</span><span class="sxs-lookup"><span data-stu-id="a1cac-139">ALIASES</span></span>

<span data-ttu-id="a1cac-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a1cac-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1cac-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a1cac-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1cac-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a1cac-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1cac-143">INPUTOBJECT <IMySqlIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a1cac-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1cac-144">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a1cac-145">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a1cac-146">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a1cac-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="a1cac-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1cac-148">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a1cac-149">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a1cac-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a1cac-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1cac-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a1cac-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a1cac-153">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a1cac-154">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1cac-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a1cac-155">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1cac-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a1cac-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1cac-156">RELATED LINKS</span></span>

