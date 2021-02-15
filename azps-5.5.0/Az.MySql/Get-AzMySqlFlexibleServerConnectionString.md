---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: c99a7c24e6582db9eea0bcf2811afded8c985489
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136039"
---
# <span data-ttu-id="39f91-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="39f91-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="39f91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39f91-102">SYNOPSIS</span></span>
<span data-ttu-id="39f91-103">根據用戶端連線提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="39f91-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="39f91-104">句法</span><span class="sxs-lookup"><span data-stu-id="39f91-104">SYNTAX</span></span>

### <span data-ttu-id="39f91-105">取得 (預設) </span><span class="sxs-lookup"><span data-stu-id="39f91-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="39f91-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39f91-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="39f91-107">說明</span><span class="sxs-lookup"><span data-stu-id="39f91-107">DESCRIPTION</span></span>
<span data-ttu-id="39f91-108">根據用戶端連線提供者取得連接字串。</span><span class="sxs-lookup"><span data-stu-id="39f91-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="39f91-109">示例</span><span class="sxs-lookup"><span data-stu-id="39f91-109">EXAMPLES</span></span>

### <span data-ttu-id="39f91-110">範例1：依名稱取得連接字串</span><span class="sxs-lookup"><span data-stu-id="39f91-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="39f91-111">這個 Cmdlet 會依伺服器名稱顯示用戶端的連線字串。</span><span class="sxs-lookup"><span data-stu-id="39f91-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="39f91-112">範例2：透過身分識別取得 MySql server 連線字串</span><span class="sxs-lookup"><span data-stu-id="39f91-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="39f91-113">這個 Cmdlet 透過身分識別來取得 MySql server 連線字串。</span><span class="sxs-lookup"><span data-stu-id="39f91-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="39f91-114">參數</span><span class="sxs-lookup"><span data-stu-id="39f91-114">PARAMETERS</span></span>

### <span data-ttu-id="39f91-115">-用戶端</span><span class="sxs-lookup"><span data-stu-id="39f91-115">-Client</span></span>
<span data-ttu-id="39f91-116">用戶端連線提供者。</span><span class="sxs-lookup"><span data-stu-id="39f91-116">Client connection provider.</span></span>

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

### <span data-ttu-id="39f91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f91-117">-DefaultProfile</span></span>
<span data-ttu-id="39f91-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39f91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39f91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39f91-119">-InputObject</span></span>
<span data-ttu-id="39f91-120">連接字串的伺服器。</span><span class="sxs-lookup"><span data-stu-id="39f91-120">The server for the connection string.</span></span>
<span data-ttu-id="39f91-121">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="39f91-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39f91-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="39f91-122">-Name</span></span>
<span data-ttu-id="39f91-123">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-123">The name of the server.</span></span>

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

### <span data-ttu-id="39f91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f91-124">-ResourceGroupName</span></span>
<span data-ttu-id="39f91-125">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="39f91-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="39f91-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39f91-126">-SubscriptionId</span></span>
<span data-ttu-id="39f91-127">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="39f91-127">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="39f91-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f91-128">CommonParameters</span></span>
<span data-ttu-id="39f91-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39f91-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f91-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39f91-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f91-131">輸入</span><span class="sxs-lookup"><span data-stu-id="39f91-131">INPUTS</span></span>

### <span data-ttu-id="39f91-132">IMySqlIdentity 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39f91-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="39f91-133">輸出</span><span class="sxs-lookup"><span data-stu-id="39f91-133">OUTPUTS</span></span>

### <span data-ttu-id="39f91-134">System.object</span><span class="sxs-lookup"><span data-stu-id="39f91-134">System.String</span></span>

## <span data-ttu-id="39f91-135">筆記</span><span class="sxs-lookup"><span data-stu-id="39f91-135">NOTES</span></span>

<span data-ttu-id="39f91-136">別名</span><span class="sxs-lookup"><span data-stu-id="39f91-136">ALIASES</span></span>

<span data-ttu-id="39f91-137">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="39f91-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39f91-138">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="39f91-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39f91-139">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="39f91-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39f91-140">INPUTOBJECT <IMySqlIdentity> ：連接字串的伺服器。</span><span class="sxs-lookup"><span data-stu-id="39f91-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="39f91-141">`[ConfigurationName <String>]`：伺服器配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="39f91-142">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="39f91-143">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="39f91-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="39f91-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39f91-145">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="39f91-146">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="39f91-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="39f91-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="39f91-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="39f91-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全警示原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="39f91-150">`[ServerName <String>]`：伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="39f91-151">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39f91-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="39f91-152">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="39f91-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="39f91-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="39f91-153">RELATED LINKS</span></span>

