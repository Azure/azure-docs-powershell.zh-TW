---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/test-azmysqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
ms.openlocfilehash: 5616eb79575154e2cbd5128f10eabc1913c9d506
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906133"
---
# <span data-ttu-id="96b6b-101">Test-AzMySqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="96b6b-101">Test-AzMySqlFlexibleServerConnect</span></span>

## <span data-ttu-id="96b6b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="96b6b-103">測試資料庫伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="96b6b-104">語法</span><span class="sxs-lookup"><span data-stu-id="96b6b-104">SYNTAX</span></span>

### <span data-ttu-id="96b6b-105">測試 (預設) </span><span class="sxs-lookup"><span data-stu-id="96b6b-105">Test (Default)</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96b6b-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="96b6b-106">TestAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96b6b-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="96b6b-107">TestViaIdentity</span></span>
```
Test-AzMySqlFlexibleServerConnect -AdministratorLoginPassword <SecureString> -InputObject <IMySqlIdentity>
 [-DatabaseName <String>] [-AdministratorUserName <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="96b6b-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="96b6b-108">TestViaIdentityAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IMySqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="96b6b-109">描述</span><span class="sxs-lookup"><span data-stu-id="96b6b-109">DESCRIPTION</span></span>
<span data-ttu-id="96b6b-110">測試資料庫伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="96b6b-111">例子</span><span class="sxs-lookup"><span data-stu-id="96b6b-111">EXAMPLES</span></span>

### <span data-ttu-id="96b6b-112">範例 1：根據名稱測試連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="96b6b-113">根據資源群組和伺服器名稱測試連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="96b6b-114">範例 2：根據身分識別測試連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="96b6b-115">根據身分識別測試連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-115">Test connection by the identity</span></span>

### <span data-ttu-id="96b6b-116">範例 3：按名稱測試查詢</span><span class="sxs-lookup"><span data-stu-id="96b6b-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="96b6b-117">根據資源群組和伺服器名稱測試查詢</span><span class="sxs-lookup"><span data-stu-id="96b6b-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="96b6b-118">範例 4：根據身分識別測試連接</span><span class="sxs-lookup"><span data-stu-id="96b6b-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="96b6b-119">根據身分識別測試查詢</span><span class="sxs-lookup"><span data-stu-id="96b6b-119">Test a query by the identity</span></span>

## <span data-ttu-id="96b6b-120">參數</span><span class="sxs-lookup"><span data-stu-id="96b6b-120">PARAMETERS</span></span>

### <span data-ttu-id="96b6b-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="96b6b-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="96b6b-122">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="96b6b-122">The password of the administrator.</span></span>
<span data-ttu-id="96b6b-123">最少 8 個字元，最多 128 個字元。</span><span class="sxs-lookup"><span data-stu-id="96b6b-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="96b6b-124">密碼必須包含下列三種類別的字元：英文大寫字母、英文小寫字母、數位和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="96b6b-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b6b-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="96b6b-125">-AdministratorUserName</span></span>
<span data-ttu-id="96b6b-126">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-126">Administrator username for the server.</span></span>
<span data-ttu-id="96b6b-127">設定完成後，即無法變更。</span><span class="sxs-lookup"><span data-stu-id="96b6b-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="96b6b-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96b6b-128">-DatabaseName</span></span>
<span data-ttu-id="96b6b-129">要連接的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-129">The database name to connect.</span></span>

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

### <span data-ttu-id="96b6b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b6b-130">-DefaultProfile</span></span>
<span data-ttu-id="96b6b-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96b6b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96b6b-132">-InputObject</span></span>
<span data-ttu-id="96b6b-133">要連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="96b6b-133">The server to connect.</span></span>
<span data-ttu-id="96b6b-134">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96b6b-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b6b-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="96b6b-135">-Name</span></span>
<span data-ttu-id="96b6b-136">要連接的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b6b-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="96b6b-137">-QueryText</span></span>
<span data-ttu-id="96b6b-138">要測試之資料庫的查詢</span><span class="sxs-lookup"><span data-stu-id="96b6b-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b6b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b6b-139">-ResourceGroupName</span></span>
<span data-ttu-id="96b6b-140">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="96b6b-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b6b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b6b-141">CommonParameters</span></span>
<span data-ttu-id="96b6b-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96b6b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b6b-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96b6b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b6b-144">輸入</span><span class="sxs-lookup"><span data-stu-id="96b6b-144">INPUTS</span></span>

### <span data-ttu-id="96b6b-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="96b6b-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="96b6b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="96b6b-146">OUTPUTS</span></span>

### <span data-ttu-id="96b6b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="96b6b-147">System.String</span></span>

## <span data-ttu-id="96b6b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="96b6b-148">NOTES</span></span>

<span data-ttu-id="96b6b-149">別名</span><span class="sxs-lookup"><span data-stu-id="96b6b-149">ALIASES</span></span>

<span data-ttu-id="96b6b-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="96b6b-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="96b6b-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="96b6b-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="96b6b-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="96b6b-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="96b6b-153">INPUTOBJECT： <IMySqlIdentity> 要連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="96b6b-153">INPUTOBJECT <IMySqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="96b6b-154">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="96b6b-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="96b6b-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="96b6b-157">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="96b6b-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="96b6b-158">`[KeyName <String>]`：伺服器金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="96b6b-159">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="96b6b-160">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="96b6b-161">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="96b6b-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="96b6b-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="96b6b-163">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="96b6b-164">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="96b6b-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="96b6b-165">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="96b6b-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="96b6b-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="96b6b-166">RELATED LINKS</span></span>

