---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916920"
---
# <span data-ttu-id="216a4-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="216a4-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="216a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="216a4-102">SYNOPSIS</span></span>
<span data-ttu-id="216a4-103">根據用戶端連接提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="216a4-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="216a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="216a4-104">SYNTAX</span></span>

### <span data-ttu-id="216a4-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="216a4-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="216a4-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="216a4-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="216a4-107">描述</span><span class="sxs-lookup"><span data-stu-id="216a4-107">DESCRIPTION</span></span>
<span data-ttu-id="216a4-108">根據用戶端連接提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="216a4-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="216a4-109">例子</span><span class="sxs-lookup"><span data-stu-id="216a4-109">EXAMPLES</span></span>

### <span data-ttu-id="216a4-110">範例 1：按名稱取得連接字串</span><span class="sxs-lookup"><span data-stu-id="216a4-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="216a4-111">此 Cmdlet 會以伺服器名稱顯示用戶端的連接字串。</span><span class="sxs-lookup"><span data-stu-id="216a4-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="216a4-112">範例 2：根據身分識別取得 MySql 伺服器連接字串</span><span class="sxs-lookup"><span data-stu-id="216a4-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="216a4-113">此 Cmdlet 會以身分識別方式獲得 MySql 伺服器連接字串。</span><span class="sxs-lookup"><span data-stu-id="216a4-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="216a4-114">參數</span><span class="sxs-lookup"><span data-stu-id="216a4-114">PARAMETERS</span></span>

### <span data-ttu-id="216a4-115">-用戶端</span><span class="sxs-lookup"><span data-stu-id="216a4-115">-Client</span></span>
<span data-ttu-id="216a4-116">用戶端連接提供者。</span><span class="sxs-lookup"><span data-stu-id="216a4-116">Client connection provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216a4-117">-DefaultProfile</span></span>
<span data-ttu-id="216a4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="216a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216a4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="216a4-119">-InputObject</span></span>
<span data-ttu-id="216a4-120">連接字串的伺服器。</span><span class="sxs-lookup"><span data-stu-id="216a4-120">The server for the connection string.</span></span>
<span data-ttu-id="216a4-121">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="216a4-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="216a4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="216a4-122">-Name</span></span>
<span data-ttu-id="216a4-123">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="216a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="216a4-125">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="216a4-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216a4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="216a4-126">-SubscriptionId</span></span>
<span data-ttu-id="216a4-127">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="216a4-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216a4-128">CommonParameters</span></span>
<span data-ttu-id="216a4-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="216a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216a4-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="216a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216a4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="216a4-131">INPUTS</span></span>

### <span data-ttu-id="216a4-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="216a4-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="216a4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="216a4-133">OUTPUTS</span></span>

### <span data-ttu-id="216a4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="216a4-134">System.String</span></span>

## <span data-ttu-id="216a4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="216a4-135">NOTES</span></span>

<span data-ttu-id="216a4-136">別名</span><span class="sxs-lookup"><span data-stu-id="216a4-136">ALIASES</span></span>

<span data-ttu-id="216a4-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="216a4-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="216a4-138">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="216a4-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="216a4-139">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="216a4-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="216a4-140">INPUTOBJECT： <IMySqlIdentity> 連接字串的伺服器。</span><span class="sxs-lookup"><span data-stu-id="216a4-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="216a4-141">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="216a4-142">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="216a4-143">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="216a4-144">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="216a4-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="216a4-145">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="216a4-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="216a4-147">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="216a4-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="216a4-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="216a4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="216a4-150">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="216a4-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="216a4-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="216a4-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="216a4-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="216a4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="216a4-153">RELATED LINKS</span></span>

