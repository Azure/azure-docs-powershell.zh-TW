---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: c544ce2ea5f02d5c0b3b7aee41e19992a0dc356d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135071"
---
# <span data-ttu-id="f1779-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="f1779-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="f1779-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1779-102">SYNOPSIS</span></span>
<span data-ttu-id="f1779-103">建立新的 MySQL 靈活伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1779-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="f1779-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1779-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f1779-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1779-105">DESCRIPTION</span></span>
<span data-ttu-id="f1779-106">建立新的 MySQL 靈活伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1779-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="f1779-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1779-107">EXAMPLES</span></span>

### <span data-ttu-id="f1779-108">範例1：使用引數建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="f1779-108">Example 1: Create a new MySql flexible server with arguments</span></span>
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



### <span data-ttu-id="f1779-109">範例2：使用預設設定建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="f1779-109">Example 2: Create a new MySql flexible server with default setting</span></span>
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

<span data-ttu-id="f1779-110">這個 Cmdlet 會使用預設參數值來建立 MySql 彈性伺服器，並在新的虛擬網路中提供伺服器，並將子網委派給伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1779-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="f1779-111">[地點] 的預設值是 [西部美國 2]、Sku 為 Standard_B1ms、Sku 層是 Burstable，而 [儲存空間大小] 是10GiB。</span><span class="sxs-lookup"><span data-stu-id="f1779-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="f1779-112">如果您想要尋找伺服器的自動產生的密碼，請使用 ConvertFrom-SecureString 將 ' SecuredPassword」屬性轉換為純文字。</span><span class="sxs-lookup"><span data-stu-id="f1779-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="f1779-113"> (例如 $server。SecuredPassword |ConvertFrom-SecureString AsPlainText) </span><span class="sxs-lookup"><span data-stu-id="f1779-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="f1779-114">範例3：使用虛擬網路建立新的 MySql 靈活伺服器</span><span class="sxs-lookup"><span data-stu-id="f1779-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
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

<span data-ttu-id="f1779-115">這個 Cmdlet 會使用使用者提供的 vnet id 或 vnet 名稱來建立 MySql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1779-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="f1779-116">如果虛擬網路不存在，則 Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="f1779-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="f1779-117">範例4：使用虛擬網路和子網名稱建立新的 MySql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="f1779-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
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

<span data-ttu-id="f1779-118">這個 Cmdlet 會使用 vnet 名稱、子網名稱、vnet 首碼及子網首碼來建立 MySql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1779-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="f1779-119">如果虛擬網路和子網不存在，則 Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="f1779-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="f1779-120">範例7：建立新的 MySql 靈活的伺服器，以公開存取所有 Ip</span><span class="sxs-lookup"><span data-stu-id="f1779-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
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

<span data-ttu-id="f1779-121">這個 Cmdlet 會建立 MySql 彈性伺服器來開啟所有 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f1779-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="f1779-122">範例8：使用防火牆建立新的 MySql 靈活伺服器</span><span class="sxs-lookup"><span data-stu-id="f1779-122">Example 8: Create a new MySql flexible server with firewall</span></span>
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

<span data-ttu-id="f1779-123">這個 Cmdlet 會將 MySql 靈活的伺服器建立為指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f1779-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="f1779-124">參數</span><span class="sxs-lookup"><span data-stu-id="f1779-124">PARAMETERS</span></span>

### <span data-ttu-id="f1779-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="f1779-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="f1779-126">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="f1779-126">The password of the administrator.</span></span>
<span data-ttu-id="f1779-127">最少8個字元和最大的128個字元。</span><span class="sxs-lookup"><span data-stu-id="f1779-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="f1779-128">密碼必須包含下列其中三種類別的字元：英文大寫字母、英文小寫字母、數位和非數位元字元。</span><span class="sxs-lookup"><span data-stu-id="f1779-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="f1779-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="f1779-129">-AdministratorUserName</span></span>
<span data-ttu-id="f1779-130">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="f1779-130">Administrator username for the server.</span></span>
<span data-ttu-id="f1779-131">一旦設定，就無法變更。</span><span class="sxs-lookup"><span data-stu-id="f1779-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="f1779-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1779-132">-AsJob</span></span>
<span data-ttu-id="f1779-133">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="f1779-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="f1779-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="f1779-134">-BackupRetentionDay</span></span>
<span data-ttu-id="f1779-135">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="f1779-135">Backup retention days for the server.</span></span>
<span data-ttu-id="f1779-136">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="f1779-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="f1779-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1779-137">-DefaultProfile</span></span>
<span data-ttu-id="f1779-138">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1779-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1779-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="f1779-139">-HighAvailability</span></span>
<span data-ttu-id="f1779-140">啟用或停用高可用性功能。</span><span class="sxs-lookup"><span data-stu-id="f1779-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="f1779-141">預設值為 Disabled。</span><span class="sxs-lookup"><span data-stu-id="f1779-141">Default value is Disabled.</span></span>
<span data-ttu-id="f1779-142">預設：已停用。</span><span class="sxs-lookup"><span data-stu-id="f1779-142">Default: Disabled.</span></span>

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

### <span data-ttu-id="f1779-143">-位置</span><span class="sxs-lookup"><span data-stu-id="f1779-143">-Location</span></span>
<span data-ttu-id="f1779-144">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="f1779-144">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f1779-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1779-145">-Name</span></span>
<span data-ttu-id="f1779-146">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1779-146">The name of the server.</span></span>

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

### <span data-ttu-id="f1779-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f1779-147">-NoWait</span></span>
<span data-ttu-id="f1779-148">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="f1779-148">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f1779-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="f1779-149">-PublicAccess</span></span>
<span data-ttu-id="f1779-150">決定公用存取。</span><span class="sxs-lookup"><span data-stu-id="f1779-150">Determines the public access.</span></span>
<span data-ttu-id="f1779-151">輸入要包含在允許的 ip 地址清單中的一或一系列 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="f1779-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="f1779-152">IP 位址範圍必須以破折號分隔，且不能包含任何空格。</span><span class="sxs-lookup"><span data-stu-id="f1779-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="f1779-153">指定0.0.0.0 允許從 Azure 中部署的任何資源公開存取，以存取您的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1779-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="f1779-154">指定 [沒有 IP 位址] 會將伺服器設定為 [公用存取] 模式，但不會建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="f1779-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="f1779-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1779-155">-ResourceGroupName</span></span>
<span data-ttu-id="f1779-156">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="f1779-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f1779-157">-Sku</span><span class="sxs-lookup"><span data-stu-id="f1779-157">-Sku</span></span>
<span data-ttu-id="f1779-158">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 Standard_B1ms、Standard_D2ds_v4。</span><span class="sxs-lookup"><span data-stu-id="f1779-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="f1779-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f1779-159">-SkuTier</span></span>
<span data-ttu-id="f1779-160">計算伺服器的層級。</span><span class="sxs-lookup"><span data-stu-id="f1779-160">Compute tier of the server.</span></span>
<span data-ttu-id="f1779-161">已接受的值： Burstable、GeneralPurpose、記憶體已優化。</span><span class="sxs-lookup"><span data-stu-id="f1779-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="f1779-162">預設值： Burstable。</span><span class="sxs-lookup"><span data-stu-id="f1779-162">Default: Burstable.</span></span>

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

### <span data-ttu-id="f1779-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="f1779-163">-StorageInMb</span></span>
<span data-ttu-id="f1779-164">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="f1779-164">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="f1779-165">-子網</span><span class="sxs-lookup"><span data-stu-id="f1779-165">-Subnet</span></span>
<span data-ttu-id="f1779-166">要建立之現有子網或新名稱的名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1779-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="f1779-167">請注意，該子網會委派給 DBforMySQL/flexibleServers。</span><span class="sxs-lookup"><span data-stu-id="f1779-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="f1779-168">委派之後，此子網無法用於任何其他類型的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="f1779-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="f1779-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="f1779-169">-SubnetPrefix</span></span>
<span data-ttu-id="f1779-170">以 CIDR 格式建立新的 vnet 時要使用的子網 IP 位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="f1779-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="f1779-171">預設值為 10.0.0.0/24。</span><span class="sxs-lookup"><span data-stu-id="f1779-171">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="f1779-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f1779-172">-SubscriptionId</span></span>
<span data-ttu-id="f1779-173">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f1779-173">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f1779-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1779-174">-Tag</span></span>
<span data-ttu-id="f1779-175">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="f1779-175">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f1779-176">-版本</span><span class="sxs-lookup"><span data-stu-id="f1779-176">-Version</span></span>
<span data-ttu-id="f1779-177">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="f1779-177">Server version.</span></span>

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

### <span data-ttu-id="f1779-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="f1779-178">-Vnet</span></span>
<span data-ttu-id="f1779-179">要建立之現有虛擬網路或新名稱的名稱或 Id。</span><span class="sxs-lookup"><span data-stu-id="f1779-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="f1779-180">名稱必須介於2到64個字元之間。</span><span class="sxs-lookup"><span data-stu-id="f1779-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="f1779-181">名稱必須以字母或數位開頭、以字母、數位或底線結尾，且只能包含字母、數位、底線、句號或連字號。</span><span class="sxs-lookup"><span data-stu-id="f1779-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="f1779-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="f1779-182">-VnetPrefix</span></span>
<span data-ttu-id="f1779-183">以 CIDR 格式建立新的 vnet 時要使用的 IP 位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="f1779-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="f1779-184">預設值為 10.0.0.0/16。</span><span class="sxs-lookup"><span data-stu-id="f1779-184">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="f1779-185">-確認</span><span class="sxs-lookup"><span data-stu-id="f1779-185">-Confirm</span></span>
<span data-ttu-id="f1779-186">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1779-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1779-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1779-187">-WhatIf</span></span>
<span data-ttu-id="f1779-188">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1779-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1779-189">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1779-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1779-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1779-190">CommonParameters</span></span>
<span data-ttu-id="f1779-191">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1779-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1779-192">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1779-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1779-193">輸入</span><span class="sxs-lookup"><span data-stu-id="f1779-193">INPUTS</span></span>

## <span data-ttu-id="f1779-194">輸出</span><span class="sxs-lookup"><span data-stu-id="f1779-194">OUTPUTS</span></span>

### <span data-ttu-id="f1779-195">IServerAutoGenerated 中的 Api20200701Preview （）。</span><span class="sxs-lookup"><span data-stu-id="f1779-195">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="f1779-196">筆記</span><span class="sxs-lookup"><span data-stu-id="f1779-196">NOTES</span></span>

<span data-ttu-id="f1779-197">別名</span><span class="sxs-lookup"><span data-stu-id="f1779-197">ALIASES</span></span>

## <span data-ttu-id="f1779-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1779-198">RELATED LINKS</span></span>

