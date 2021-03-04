---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c40f8ad000bca3026860ebc328be57e6931a1546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910965"
---
# <span data-ttu-id="b4fc5-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b4fc5-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="b4fc5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fc5-103">建立新伺服器。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-103">Creates a new server.</span></span>

## <span data-ttu-id="b4fc5-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4fc5-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-Zone <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b4fc5-105">描述</span><span class="sxs-lookup"><span data-stu-id="b4fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="b4fc5-106">建立新伺服器。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-106">Creates a new server.</span></span>

## <span data-ttu-id="b4fc5-107">例子</span><span class="sxs-lookup"><span data-stu-id="b4fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="b4fc5-108">範例 1：建立具有引數的新 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fc5-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="b4fc5-109">範例 2：使用預設設定建立一個新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fc5-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="b4fc5-110">此 Cmdlet 會建立 PostgreSql 彈性伺服器與預設參數值，並新虛擬網路內提供伺服器，並且將子網委派給伺服器。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="b4fc5-111">位置的預設值為美國西部 2、SKU 為 Standard_D2s_v3、SKU 層級為 GeneralPurpose，而儲存大小為 128GiB。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="b4fc5-112">如果您想要尋找伺服器自動產生的密碼，請使用 ConvertFrom-SecureString 將 "SecuredPassword" 屬性轉換為純文字。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="b4fc5-113"> (例如，$server。SecuredPassword |ConvertFrom-SecureString -AsP一文集) </span><span class="sxs-lookup"><span data-stu-id="b4fc5-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="b4fc5-114">範例 3：使用虛擬網路建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fc5-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="b4fc5-115">此 Cmdlet 會建立 PostgreSql 彈性伺服器，以及使用者提供的 vnet 識別碼或 vnet 名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="b4fc5-116">如果虛擬網路不存在，Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="b4fc5-117">範例 4：使用虛擬網路和子網名稱建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fc5-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforPostgreSQL/flexibleServers
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="b4fc5-118">此 Cmdlet 會建立 PostgreSql 彈性伺服器，包含 vnet 名稱、子網名稱、vnet 首碼和子網首碼。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="b4fc5-119">如果虛擬網路和子網不存在，Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="b4fc5-120">範例 7：建立具有所有 IP 公用存取權的新 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fc5-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="b4fc5-121">此 Cmdlet 會建立 PostgreSql 彈性伺服器，可開啟至所有 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="b4fc5-122">範例 8：建立具有防火牆的新 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="b4fc5-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating PostgreSQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="b4fc5-123">此 Cmdlet 會建立 PostgreSql 彈性伺服器，以開啟至指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="b4fc5-124">參數</span><span class="sxs-lookup"><span data-stu-id="b4fc5-124">PARAMETERS</span></span>

### <span data-ttu-id="b4fc5-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b4fc5-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b4fc5-126">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-126">The password of the administrator.</span></span>
<span data-ttu-id="b4fc5-127">最少 8 個字元，最多 128 個字元。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b4fc5-128">密碼必須包含下列三種類別的字元：英文大寫字母、英文小寫字母、數位和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b4fc5-129">-AdministratorUserName</span></span>
<span data-ttu-id="b4fc5-130">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-130">Administrator username for the server.</span></span>
<span data-ttu-id="b4fc5-131">設定完成後，即無法變更。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b4fc5-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4fc5-132">-AsJob</span></span>
<span data-ttu-id="b4fc5-133">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="b4fc5-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b4fc5-134">-BackupRetentionDay</span></span>
<span data-ttu-id="b4fc5-135">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-135">Backup retention days for the server.</span></span>
<span data-ttu-id="b4fc5-136">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-136">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fc5-137">-DefaultProfile</span></span>
<span data-ttu-id="b4fc5-138">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4fc5-139">-位置</span><span class="sxs-lookup"><span data-stu-id="b4fc5-139">-Location</span></span>
<span data-ttu-id="b4fc5-140">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b4fc5-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4fc5-141">-Name</span></span>
<span data-ttu-id="b4fc5-142">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-142">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b4fc5-143">-NoWait</span></span>
<span data-ttu-id="b4fc5-144">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b4fc5-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="b4fc5-145">-PublicAccess</span></span>
<span data-ttu-id="b4fc5-146">決定公用存取權。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-146">Determines the public access.</span></span>
<span data-ttu-id="b4fc5-147">輸入要包含在允許 IP 清單中的單一或多個 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="b4fc5-148">IP 位址範圍必須以虛線分隔，且不得包含任何空格。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="b4fc5-149">指定 0.0.0.0 可讓公用存取 Azure 內部署的任何資源來存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="b4fc5-150">指定沒有 IP 位址時，伺服器會設定為公用存取模式，但不建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="b4fc5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4fc5-151">-ResourceGroupName</span></span>
<span data-ttu-id="b4fc5-152">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b4fc5-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="b4fc5-153">-Sku</span></span>
<span data-ttu-id="b4fc5-154">SKU 的名稱，通常是 tier + family + 核心，例如Standard_B1ms、Standard_D2ds_v4。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="b4fc5-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b4fc5-155">-SkuTier</span></span>
<span data-ttu-id="b4fc5-156">伺服器的計算層級。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-156">Compute tier of the server.</span></span>
<span data-ttu-id="b4fc5-157">接受的值：可重值、GeneralPurpose、記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="b4fc5-158">預設值：可重複。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="b4fc5-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b4fc5-159">-StorageInMb</span></span>
<span data-ttu-id="b4fc5-160">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-160">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-161">-子網</span><span class="sxs-lookup"><span data-stu-id="b4fc5-161">-Subnet</span></span>
<span data-ttu-id="b4fc5-162">現有子網的名稱或識別碼，或要建立之新子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="b4fc5-163">請注意，子網會委派給 Microsoft.DBforPostgreSQL/flexibleServers。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="b4fc5-164">委派之後，這個子網就無法用於任何其他 Azure 資源類型。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="b4fc5-165">-子網Prefix</span><span class="sxs-lookup"><span data-stu-id="b4fc5-165">-SubnetPrefix</span></span>
<span data-ttu-id="b4fc5-166">以 CIDR 格式建立新 vnet 時，使用的子網 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="b4fc5-167">預設值為 10.0.0.0/24。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="b4fc5-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4fc5-168">-SubscriptionId</span></span>
<span data-ttu-id="b4fc5-169">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-169">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-170">-標記</span><span class="sxs-lookup"><span data-stu-id="b4fc5-170">-Tag</span></span>
<span data-ttu-id="b4fc5-171">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-171">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-172">-版本</span><span class="sxs-lookup"><span data-stu-id="b4fc5-172">-Version</span></span>
<span data-ttu-id="b4fc5-173">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-173">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fc5-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="b4fc5-174">-Vnet</span></span>
<span data-ttu-id="b4fc5-175">現有虛擬網路的名稱或識別碼，或要建立之新網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="b4fc5-176">名稱必須介於 2 到 64 個字元之間。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="b4fc5-177">名稱必須以字母或數位開頭，結尾必須是字母、數位或底數，而且可能只包含字母、數位、底數、句點或連字號。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="b4fc5-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="b4fc5-178">-VnetPrefix</span></span>
<span data-ttu-id="b4fc5-179">以 CIDR 格式建立新 vnet 時，使用的 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="b4fc5-180">預設值為 10.0.0.0/16。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="b4fc5-181">-區域</span><span class="sxs-lookup"><span data-stu-id="b4fc5-181">-Zone</span></span>
<span data-ttu-id="b4fc5-182">資源要置入的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-182">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="b4fc5-183">-確認</span><span class="sxs-lookup"><span data-stu-id="b4fc5-183">-Confirm</span></span>
<span data-ttu-id="b4fc5-184">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4fc5-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4fc5-185">-WhatIf</span></span>
<span data-ttu-id="b4fc5-186">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4fc5-187">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4fc5-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fc5-188">CommonParameters</span></span>
<span data-ttu-id="b4fc5-189">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4fc5-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fc5-190">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4fc5-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fc5-191">輸入</span><span class="sxs-lookup"><span data-stu-id="b4fc5-191">INPUTS</span></span>

## <span data-ttu-id="b4fc5-192">輸出</span><span class="sxs-lookup"><span data-stu-id="b4fc5-192">OUTPUTS</span></span>

### <span data-ttu-id="b4fc5-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b4fc5-193">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="b4fc5-194">筆記</span><span class="sxs-lookup"><span data-stu-id="b4fc5-194">NOTES</span></span>

<span data-ttu-id="b4fc5-195">別名</span><span class="sxs-lookup"><span data-stu-id="b4fc5-195">ALIASES</span></span>

## <span data-ttu-id="b4fc5-196">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4fc5-196">RELATED LINKS</span></span>

