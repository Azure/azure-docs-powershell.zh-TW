---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1e49f5937196a402e051d28665614befbf6eb04c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902313"
---
# <span data-ttu-id="eade7-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="eade7-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="eade7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eade7-102">SYNOPSIS</span></span>
<span data-ttu-id="eade7-103">測試資料庫伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="eade7-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="eade7-104">語法</span><span class="sxs-lookup"><span data-stu-id="eade7-104">SYNTAX</span></span>

### <span data-ttu-id="eade7-105">測試 (預設) </span><span class="sxs-lookup"><span data-stu-id="eade7-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eade7-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="eade7-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eade7-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eade7-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eade7-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="eade7-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eade7-109">描述</span><span class="sxs-lookup"><span data-stu-id="eade7-109">DESCRIPTION</span></span>
<span data-ttu-id="eade7-110">測試資料庫伺服器的連接</span><span class="sxs-lookup"><span data-stu-id="eade7-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="eade7-111">例子</span><span class="sxs-lookup"><span data-stu-id="eade7-111">EXAMPLES</span></span>

### <span data-ttu-id="eade7-112">範例 1：根據名稱測試連接</span><span class="sxs-lookup"><span data-stu-id="eade7-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="eade7-113">根據資源群組和伺服器名稱測試連接</span><span class="sxs-lookup"><span data-stu-id="eade7-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="eade7-114">範例 2：根據身分識別測試連接</span><span class="sxs-lookup"><span data-stu-id="eade7-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="eade7-115">根據身分識別測試連接</span><span class="sxs-lookup"><span data-stu-id="eade7-115">Test connection by the identity</span></span>

### <span data-ttu-id="eade7-116">範例 3：按名稱測試查詢</span><span class="sxs-lookup"><span data-stu-id="eade7-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="eade7-117">根據資源群組和伺服器名稱測試查詢</span><span class="sxs-lookup"><span data-stu-id="eade7-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="eade7-118">範例 4：根據身分識別測試連接</span><span class="sxs-lookup"><span data-stu-id="eade7-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="eade7-119">根據身分識別測試查詢</span><span class="sxs-lookup"><span data-stu-id="eade7-119">Test a query by the identity</span></span>

## <span data-ttu-id="eade7-120">參數</span><span class="sxs-lookup"><span data-stu-id="eade7-120">PARAMETERS</span></span>

### <span data-ttu-id="eade7-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="eade7-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="eade7-122">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="eade7-122">The password of the administrator.</span></span>
<span data-ttu-id="eade7-123">最少 8 個字元，最多 128 個字元。</span><span class="sxs-lookup"><span data-stu-id="eade7-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="eade7-124">密碼必須包含下列三種類別的字元：英文大寫字母、英文小寫字母、數位和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="eade7-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="eade7-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="eade7-125">-AdministratorUserName</span></span>
<span data-ttu-id="eade7-126">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-126">Administrator username for the server.</span></span>
<span data-ttu-id="eade7-127">設定完成後，即無法變更。</span><span class="sxs-lookup"><span data-stu-id="eade7-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="eade7-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eade7-128">-DatabaseName</span></span>
<span data-ttu-id="eade7-129">要連接的資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-129">The database name to connect.</span></span>

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

### <span data-ttu-id="eade7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eade7-130">-DefaultProfile</span></span>
<span data-ttu-id="eade7-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eade7-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eade7-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eade7-132">-InputObject</span></span>
<span data-ttu-id="eade7-133">要連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="eade7-133">The server to connect.</span></span>
<span data-ttu-id="eade7-134">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eade7-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eade7-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="eade7-135">-Name</span></span>
<span data-ttu-id="eade7-136">要連接的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-136">The name of the server to connect.</span></span>

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

### <span data-ttu-id="eade7-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="eade7-137">-QueryText</span></span>
<span data-ttu-id="eade7-138">要測試之資料庫的查詢</span><span class="sxs-lookup"><span data-stu-id="eade7-138">The query for the database to test</span></span>

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

### <span data-ttu-id="eade7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eade7-139">-ResourceGroupName</span></span>
<span data-ttu-id="eade7-140">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="eade7-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eade7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eade7-141">CommonParameters</span></span>
<span data-ttu-id="eade7-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eade7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eade7-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eade7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eade7-144">輸入</span><span class="sxs-lookup"><span data-stu-id="eade7-144">INPUTS</span></span>

### <span data-ttu-id="eade7-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="eade7-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="eade7-146">輸出</span><span class="sxs-lookup"><span data-stu-id="eade7-146">OUTPUTS</span></span>

### <span data-ttu-id="eade7-147">System.String</span><span class="sxs-lookup"><span data-stu-id="eade7-147">System.String</span></span>

## <span data-ttu-id="eade7-148">筆記</span><span class="sxs-lookup"><span data-stu-id="eade7-148">NOTES</span></span>

<span data-ttu-id="eade7-149">別名</span><span class="sxs-lookup"><span data-stu-id="eade7-149">ALIASES</span></span>

<span data-ttu-id="eade7-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="eade7-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eade7-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="eade7-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eade7-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="eade7-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eade7-153">INPUTOBJECT： <IPostgreSqlIdentity> 要連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="eade7-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="eade7-154">`[ConfigurationName <String>]`：伺服器組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="eade7-155">`[DatabaseName <String>]`：資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="eade7-156">`[FirewallRuleName <String>]`：伺服器防火牆規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="eade7-157">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="eade7-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eade7-158">`[LocationName <String>]`：位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="eade7-159">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="eade7-160">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="eade7-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="eade7-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`：安全性警示策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="eade7-162">`[ServerName <String>]`：伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="eade7-163">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eade7-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="eade7-164">`[VirtualNetworkRuleName <String>]`：虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="eade7-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="eade7-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="eade7-165">RELATED LINKS</span></span>

