---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c658780407454f780ccbd00cb824dd1032f3463d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135591"
---
# <span data-ttu-id="ca32c-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="ca32c-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="ca32c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca32c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca32c-103">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca32c-103">Creates a new server.</span></span>

## <span data-ttu-id="ca32c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca32c-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ca32c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca32c-105">DESCRIPTION</span></span>
<span data-ttu-id="ca32c-106">建立新的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca32c-106">Creates a new server.</span></span>

## <span data-ttu-id="ca32c-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca32c-107">EXAMPLES</span></span>

### <span data-ttu-id="ca32c-108">範例1：使用引數建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="ca32c-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="ca32c-109">範例2：使用預設設定建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="ca32c-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="ca32c-110">這個 Cmdlet 會建立含預設參數值的 PostgreSql 彈性伺服器，並在新的虛擬網路內提供伺服器，並將子網委派給伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca32c-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="ca32c-111">[地點] 的預設值是 [西部美國 2]、Sku 為 Standard_D2s_v3、Sku 層是 GeneralPurpose，而 [儲存空間大小] 是128GiB。</span><span class="sxs-lookup"><span data-stu-id="ca32c-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="ca32c-112">如果您想要尋找伺服器的自動產生的密碼，請使用 ConvertFrom-SecureString 將 ' SecuredPassword」屬性轉換為純文字。</span><span class="sxs-lookup"><span data-stu-id="ca32c-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="ca32c-113"> (例如 $server。SecuredPassword |ConvertFrom-SecureString AsPlainText) </span><span class="sxs-lookup"><span data-stu-id="ca32c-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="ca32c-114">範例3：使用虛擬網路建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="ca32c-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="ca32c-115">這個 Cmdlet 會使用使用者提供的 vnet id 或 vnet 名稱來建立 PostgreSql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca32c-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="ca32c-116">如果虛擬網路不存在，則 Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="ca32c-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="ca32c-117">範例4：使用虛擬網路和子網名稱建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="ca32c-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="ca32c-118">這個 Cmdlet 會建立含 vnet 名稱、子網名稱、vnet 首碼及子網首碼的 PostgreSql 彈性伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca32c-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="ca32c-119">如果虛擬網路和子網不存在，則 Cmdlet 會建立一個。</span><span class="sxs-lookup"><span data-stu-id="ca32c-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="ca32c-120">範例7：建立新的 PostgreSql 彈性伺服器，以公開存取所有 Ip</span><span class="sxs-lookup"><span data-stu-id="ca32c-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="ca32c-121">這個 Cmdlet 會建立 PostgreSql 彈性伺服器來開啟所有 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ca32c-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="ca32c-122">範例8：使用防火牆建立新的 PostgreSql 彈性伺服器</span><span class="sxs-lookup"><span data-stu-id="ca32c-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="ca32c-123">這個 Cmdlet 會建立 PostgreSql 彈性伺服器來開啟指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ca32c-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="ca32c-124">參數</span><span class="sxs-lookup"><span data-stu-id="ca32c-124">PARAMETERS</span></span>

### <span data-ttu-id="ca32c-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ca32c-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ca32c-126">系統管理員的密碼。</span><span class="sxs-lookup"><span data-stu-id="ca32c-126">The password of the administrator.</span></span>
<span data-ttu-id="ca32c-127">最少8個字元和最大的128個字元。</span><span class="sxs-lookup"><span data-stu-id="ca32c-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="ca32c-128">密碼必須包含下列其中三種類別的字元：英文大寫字母、英文小寫字母、數位和非數位元字元。</span><span class="sxs-lookup"><span data-stu-id="ca32c-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="ca32c-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="ca32c-129">-AdministratorUserName</span></span>
<span data-ttu-id="ca32c-130">伺服器的系統管理員使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ca32c-130">Administrator username for the server.</span></span>
<span data-ttu-id="ca32c-131">一旦設定，就無法變更。</span><span class="sxs-lookup"><span data-stu-id="ca32c-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="ca32c-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca32c-132">-AsJob</span></span>
<span data-ttu-id="ca32c-133">執行命令做為作業。</span><span class="sxs-lookup"><span data-stu-id="ca32c-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="ca32c-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="ca32c-134">-BackupRetentionDay</span></span>
<span data-ttu-id="ca32c-135">伺服器的備份保留天數。</span><span class="sxs-lookup"><span data-stu-id="ca32c-135">Backup retention days for the server.</span></span>
<span data-ttu-id="ca32c-136">日算在7到35。</span><span class="sxs-lookup"><span data-stu-id="ca32c-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="ca32c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca32c-137">-DefaultProfile</span></span>
<span data-ttu-id="ca32c-138">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca32c-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca32c-139">-位置</span><span class="sxs-lookup"><span data-stu-id="ca32c-139">-Location</span></span>
<span data-ttu-id="ca32c-140">資源所在的位置。</span><span class="sxs-lookup"><span data-stu-id="ca32c-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ca32c-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="ca32c-141">-Name</span></span>
<span data-ttu-id="ca32c-142">伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca32c-142">The name of the server.</span></span>

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

### <span data-ttu-id="ca32c-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca32c-143">-NoWait</span></span>
<span data-ttu-id="ca32c-144">以非同步方式執行命令。</span><span class="sxs-lookup"><span data-stu-id="ca32c-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="ca32c-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="ca32c-145">-PublicAccess</span></span>
<span data-ttu-id="ca32c-146">決定公用存取。</span><span class="sxs-lookup"><span data-stu-id="ca32c-146">Determines the public access.</span></span>
<span data-ttu-id="ca32c-147">輸入要包含在允許的 ip 地址清單中的一或一系列 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ca32c-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="ca32c-148">IP 位址範圍必須以破折號分隔，且不能包含任何空格。</span><span class="sxs-lookup"><span data-stu-id="ca32c-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="ca32c-149">指定0.0.0.0 允許從 Azure 中部署的任何資源公開存取，以存取您的伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca32c-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="ca32c-150">指定 [沒有 IP 位址] 會將伺服器設定為 [公用存取] 模式，但不會建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="ca32c-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="ca32c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca32c-151">-ResourceGroupName</span></span>
<span data-ttu-id="ca32c-152">包含資源之資源群組的名稱，您可以從 Azure 資源管理員 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="ca32c-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ca32c-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="ca32c-153">-Sku</span></span>
<span data-ttu-id="ca32c-154">Sku 的名稱，通常是 [層 + 家庭 + 核心]，例如 Standard_B1ms、Standard_D2ds_v4。</span><span class="sxs-lookup"><span data-stu-id="ca32c-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="ca32c-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ca32c-155">-SkuTier</span></span>
<span data-ttu-id="ca32c-156">計算伺服器的層級。</span><span class="sxs-lookup"><span data-stu-id="ca32c-156">Compute tier of the server.</span></span>
<span data-ttu-id="ca32c-157">已接受的值： Burstable、GeneralPurpose、記憶體已優化。</span><span class="sxs-lookup"><span data-stu-id="ca32c-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="ca32c-158">預設值： Burstable。</span><span class="sxs-lookup"><span data-stu-id="ca32c-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="ca32c-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ca32c-159">-StorageInMb</span></span>
<span data-ttu-id="ca32c-160">伺服器允許的最大儲存空間。</span><span class="sxs-lookup"><span data-stu-id="ca32c-160">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ca32c-161">-子網</span><span class="sxs-lookup"><span data-stu-id="ca32c-161">-Subnet</span></span>
<span data-ttu-id="ca32c-162">要建立之現有子網或新名稱的名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="ca32c-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="ca32c-163">請注意，該子網會委派給 DBforPostgreSQL/flexibleServers。</span><span class="sxs-lookup"><span data-stu-id="ca32c-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="ca32c-164">委派之後，此子網無法用於任何其他類型的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="ca32c-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="ca32c-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="ca32c-165">-SubnetPrefix</span></span>
<span data-ttu-id="ca32c-166">以 CIDR 格式建立新的 vnet 時要使用的子網 IP 位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="ca32c-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="ca32c-167">預設值為 10.0.0.0/24。</span><span class="sxs-lookup"><span data-stu-id="ca32c-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="ca32c-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca32c-168">-SubscriptionId</span></span>
<span data-ttu-id="ca32c-169">識別 Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="ca32c-169">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="ca32c-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca32c-170">-Tag</span></span>
<span data-ttu-id="ca32c-171">以鍵值對形式的特定應用程式中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ca32c-171">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ca32c-172">-版本</span><span class="sxs-lookup"><span data-stu-id="ca32c-172">-Version</span></span>
<span data-ttu-id="ca32c-173">伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="ca32c-173">Server version.</span></span>

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

### <span data-ttu-id="ca32c-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="ca32c-174">-Vnet</span></span>
<span data-ttu-id="ca32c-175">要建立之現有虛擬網路或新名稱的名稱或 Id。</span><span class="sxs-lookup"><span data-stu-id="ca32c-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="ca32c-176">名稱必須介於2到64個字元之間。</span><span class="sxs-lookup"><span data-stu-id="ca32c-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="ca32c-177">名稱必須以字母或數位開頭、以字母、數位或底線結尾，且只能包含字母、數位、底線、句號或連字號。</span><span class="sxs-lookup"><span data-stu-id="ca32c-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="ca32c-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="ca32c-178">-VnetPrefix</span></span>
<span data-ttu-id="ca32c-179">以 CIDR 格式建立新的 vnet 時要使用的 IP 位址前置詞。</span><span class="sxs-lookup"><span data-stu-id="ca32c-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="ca32c-180">預設值為 10.0.0.0/16。</span><span class="sxs-lookup"><span data-stu-id="ca32c-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="ca32c-181">-確認</span><span class="sxs-lookup"><span data-stu-id="ca32c-181">-Confirm</span></span>
<span data-ttu-id="ca32c-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca32c-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca32c-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca32c-183">-WhatIf</span></span>
<span data-ttu-id="ca32c-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca32c-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca32c-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca32c-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca32c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca32c-186">CommonParameters</span></span>
<span data-ttu-id="ca32c-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca32c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca32c-188">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca32c-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca32c-189">輸入</span><span class="sxs-lookup"><span data-stu-id="ca32c-189">INPUTS</span></span>

## <span data-ttu-id="ca32c-190">輸出</span><span class="sxs-lookup"><span data-stu-id="ca32c-190">OUTPUTS</span></span>

### <span data-ttu-id="ca32c-191">IServerAutoGenerated （PostgreSql）。 Api20200214Preview。</span><span class="sxs-lookup"><span data-stu-id="ca32c-191">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="ca32c-192">筆記</span><span class="sxs-lookup"><span data-stu-id="ca32c-192">NOTES</span></span>

<span data-ttu-id="ca32c-193">別名</span><span class="sxs-lookup"><span data-stu-id="ca32c-193">ALIASES</span></span>

## <span data-ttu-id="ca32c-194">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca32c-194">RELATED LINKS</span></span>

