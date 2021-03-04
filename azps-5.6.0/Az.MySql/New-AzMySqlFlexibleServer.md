---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 4d4581d78b2e1f90ce334fda77107058f2294f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913182"
---
# <span data-ttu-id="a9011-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="a9011-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="a9011-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9011-102">SYNOPSIS</span></span>
<span data-ttu-id="a9011-103">建立新的 MySQL 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="a9011-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9011-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a9011-105">描述</span><span class="sxs-lookup"><span data-stu-id="a9011-105">DESCRIPTION</span></span>
<span data-ttu-id="a9011-106">建立新的 MySQL 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="a9011-107">例子</span><span class="sxs-lookup"><span data-stu-id="a9011-107">EXAMPLES</span></span>

### <span data-ttu-id="a9011-108">範例 1：建立具有引數的新 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="a9011-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="a9011-109">範例 2：使用預設設定建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="a9011-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="a9011-110">此 Cmdlet 會建立具有預設參數值的 MySql 彈性伺服器，並新虛擬網路內提供伺服器，並且將子網委派給伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="a9011-111">位置的預設值為美國西部 2、SKU 為 Standard_B1ms、SKU 層級為可重複，而儲存大小為 10GiB。</span><span class="sxs-lookup"><span data-stu-id="a9011-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="a9011-112">如果您想要尋找伺服器自動產生的密碼，請使用 ConvertFrom-SecureString 將 "SecuredPassword" 屬性轉換為純文字。</span><span class="sxs-lookup"><span data-stu-id="a9011-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="a9011-113"> (例如，$server。SecuredPassword |ConvertFrom-SecureString -AsP一文集) </span><span class="sxs-lookup"><span data-stu-id="a9011-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="a9011-114">範例 3：使用虛擬網路建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="a9011-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="a9011-115">此 Cmdlet 會使用使用者提供的 vnet 識別碼或 vnet 名稱建立 MySql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="a9011-116">如果虛擬網路不存在，Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="a9011-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="a9011-117">範例 4：使用虛擬網路和子網名稱建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="a9011-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="a9011-118">此 Cmdlet 會建立具有 vnet 名稱、子網名稱、vnet 首碼和子網首碼的 MySql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="a9011-119">如果虛擬網路和子網不存在，Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="a9011-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="a9011-120">範例 7：建立具有所有 IP 公用存取權的新 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="a9011-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="a9011-121">此 Cmdlet 會建立可開啟至所有 IP 位址的 MySql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="a9011-122">範例 8：使用防火牆建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="a9011-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="a9011-123">此 Cmdlet 會建立 MySql 彈性伺服器，以開啟至指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a9011-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="a9011-124">參數</span><span class="sxs-lookup"><span data-stu-id="a9011-124">PARAMETERS</span></span>

### <span data-ttu-id="a9011-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a9011-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a9011-126">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="a9011-126">The password of the administrator.</span></span>
<span data-ttu-id="a9011-127">最少 8 個字元，最多 128 個字元。</span><span class="sxs-lookup"><span data-stu-id="a9011-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="a9011-128">密碼必須包含下列三種類別的字元：英文大寫字母、英文小寫字母、數位和非英數位元。</span><span class="sxs-lookup"><span data-stu-id="a9011-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="a9011-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="a9011-129">-AdministratorUserName</span></span>
<span data-ttu-id="a9011-130">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a9011-130">Administrator username for the server.</span></span>
<span data-ttu-id="a9011-131">設定完成後，即無法變更。</span><span class="sxs-lookup"><span data-stu-id="a9011-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="a9011-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9011-132">-AsJob</span></span>
<span data-ttu-id="a9011-133">以工作執行命令。</span><span class="sxs-lookup"><span data-stu-id="a9011-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="a9011-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="a9011-134">-BackupRetentionDay</span></span>
<span data-ttu-id="a9011-135">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="a9011-135">Backup retention days for the server.</span></span>
<span data-ttu-id="a9011-136">日計數介於 7 到 35 之間。</span><span class="sxs-lookup"><span data-stu-id="a9011-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="a9011-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9011-137">-DefaultProfile</span></span>
<span data-ttu-id="a9011-138">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9011-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9011-139">-高使用性</span><span class="sxs-lookup"><span data-stu-id="a9011-139">-HighAvailability</span></span>
<span data-ttu-id="a9011-140">啟用或停用高可用性功能。</span><span class="sxs-lookup"><span data-stu-id="a9011-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="a9011-141">預設值已停用。</span><span class="sxs-lookup"><span data-stu-id="a9011-141">Default value is Disabled.</span></span>
<span data-ttu-id="a9011-142">預設：已停用。</span><span class="sxs-lookup"><span data-stu-id="a9011-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9011-143">-位置</span><span class="sxs-lookup"><span data-stu-id="a9011-143">-Location</span></span>
<span data-ttu-id="a9011-144">資源所在位置。</span><span class="sxs-lookup"><span data-stu-id="a9011-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="a9011-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9011-145">-Name</span></span>
<span data-ttu-id="a9011-146">伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="a9011-146">The name of the server.</span></span>

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

### <span data-ttu-id="a9011-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a9011-147">-NoWait</span></span>
<span data-ttu-id="a9011-148">非同步執行命令。</span><span class="sxs-lookup"><span data-stu-id="a9011-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a9011-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="a9011-149">-PublicAccess</span></span>
<span data-ttu-id="a9011-150">決定公用存取權。</span><span class="sxs-lookup"><span data-stu-id="a9011-150">Determines the public access.</span></span>
<span data-ttu-id="a9011-151">輸入要包含在允許 IP 清單中的單一或多個 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="a9011-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="a9011-152">IP 位址範圍必須以虛線分隔，且不得包含任何空格。</span><span class="sxs-lookup"><span data-stu-id="a9011-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="a9011-153">指定 0.0.0.0 可讓公用存取 Azure 內部署的任何資源來存取伺服器。</span><span class="sxs-lookup"><span data-stu-id="a9011-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="a9011-154">指定沒有 IP 位址時，伺服器會設定為公用存取模式，但不建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="a9011-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="a9011-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9011-155">-ResourceGroupName</span></span>
<span data-ttu-id="a9011-156">包含資源的資源組名，您可從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="a9011-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a9011-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="a9011-157">-Sku</span></span>
<span data-ttu-id="a9011-158">SKU 的名稱，通常是 tier + family + 核心，例如Standard_B1ms、Standard_D2ds_v4。</span><span class="sxs-lookup"><span data-stu-id="a9011-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="a9011-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a9011-159">-SkuTier</span></span>
<span data-ttu-id="a9011-160">伺服器的計算層級。</span><span class="sxs-lookup"><span data-stu-id="a9011-160">Compute tier of the server.</span></span>
<span data-ttu-id="a9011-161">接受的值：可重值、GeneralPurpose、記憶體優化。</span><span class="sxs-lookup"><span data-stu-id="a9011-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="a9011-162">預設值：可重複。</span><span class="sxs-lookup"><span data-stu-id="a9011-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="a9011-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="a9011-163">-StorageInMb</span></span>
<span data-ttu-id="a9011-164">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="a9011-164">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="a9011-165">-子網</span><span class="sxs-lookup"><span data-stu-id="a9011-165">-Subnet</span></span>
<span data-ttu-id="a9011-166">現有子網的名稱或識別碼，或要建立之新子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9011-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="a9011-167">請注意，子網會委派給 Microsoft.DBforMySQL/flexibleServers。</span><span class="sxs-lookup"><span data-stu-id="a9011-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="a9011-168">委派之後，這個子網就無法用於任何其他 Azure 資源類型。</span><span class="sxs-lookup"><span data-stu-id="a9011-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="a9011-169">-子網Prefix</span><span class="sxs-lookup"><span data-stu-id="a9011-169">-SubnetPrefix</span></span>
<span data-ttu-id="a9011-170">以 CIDR 格式建立新 vnet 時，使用的子網 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a9011-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="a9011-171">預設值為 10.0.0.0/24。</span><span class="sxs-lookup"><span data-stu-id="a9011-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="a9011-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9011-172">-SubscriptionId</span></span>
<span data-ttu-id="a9011-173">可識別 Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9011-173">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a9011-174">-標記</span><span class="sxs-lookup"><span data-stu-id="a9011-174">-Tag</span></span>
<span data-ttu-id="a9011-175">以金鑰值組形式顯示的應用程式特定中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a9011-175">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="a9011-176">-版本</span><span class="sxs-lookup"><span data-stu-id="a9011-176">-Version</span></span>
<span data-ttu-id="a9011-177">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="a9011-177">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9011-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="a9011-178">-Vnet</span></span>
<span data-ttu-id="a9011-179">現有虛擬網路的名稱或識別碼，或要建立之新網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9011-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="a9011-180">名稱必須介於 2 到 64 個字元之間。</span><span class="sxs-lookup"><span data-stu-id="a9011-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="a9011-181">名稱必須以字母或數位開頭，結尾必須是字母、數位或底數，而且可能只包含字母、數位、底數、句點或連字號。</span><span class="sxs-lookup"><span data-stu-id="a9011-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="a9011-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="a9011-182">-VnetPrefix</span></span>
<span data-ttu-id="a9011-183">以 CIDR 格式建立新 vnet 時，使用的 IP 位址首碼。</span><span class="sxs-lookup"><span data-stu-id="a9011-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="a9011-184">預設值為 10.0.0.0/16。</span><span class="sxs-lookup"><span data-stu-id="a9011-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="a9011-185">-區域</span><span class="sxs-lookup"><span data-stu-id="a9011-185">-Zone</span></span>
<span data-ttu-id="a9011-186">資源要置入的可用性區域。</span><span class="sxs-lookup"><span data-stu-id="a9011-186">Availability zone into which to provision the resource.</span></span>

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

### <span data-ttu-id="a9011-187">-確認</span><span class="sxs-lookup"><span data-stu-id="a9011-187">-Confirm</span></span>
<span data-ttu-id="a9011-188">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a9011-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9011-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9011-189">-WhatIf</span></span>
<span data-ttu-id="a9011-190">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9011-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9011-191">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9011-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9011-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9011-192">CommonParameters</span></span>
<span data-ttu-id="a9011-193">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9011-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9011-194">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9011-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9011-195">輸入</span><span class="sxs-lookup"><span data-stu-id="a9011-195">INPUTS</span></span>

## <span data-ttu-id="a9011-196">輸出</span><span class="sxs-lookup"><span data-stu-id="a9011-196">OUTPUTS</span></span>

### <span data-ttu-id="a9011-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a9011-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="a9011-198">筆記</span><span class="sxs-lookup"><span data-stu-id="a9011-198">NOTES</span></span>

<span data-ttu-id="a9011-199">別名</span><span class="sxs-lookup"><span data-stu-id="a9011-199">ALIASES</span></span>

## <span data-ttu-id="a9011-200">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9011-200">RELATED LINKS</span></span>

