---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792718"
---
# <span data-ttu-id="03ba5-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="03ba5-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="03ba5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="03ba5-103">建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="03ba5-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="03ba5-104">句法</span><span class="sxs-lookup"><span data-stu-id="03ba5-104">SYNTAX</span></span>

### <span data-ttu-id="03ba5-105">NewByEditionAndComputeGenerationParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="03ba5-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ba5-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ba5-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ba5-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ba5-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03ba5-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="03ba5-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03ba5-109">說明</span><span class="sxs-lookup"><span data-stu-id="03ba5-109">DESCRIPTION</span></span>
<span data-ttu-id="03ba5-110">**新的-AzSqlInstance** Cmdlet 會建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="03ba5-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="03ba5-111">示例</span><span class="sxs-lookup"><span data-stu-id="03ba5-111">EXAMPLES</span></span>

### <span data-ttu-id="03ba5-112">範例1：建立新的實例</span><span class="sxs-lookup"><span data-stu-id="03ba5-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="03ba5-113">這個命令會使用 SkuName 參數來建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="03ba5-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="03ba5-114">範例2：建立新的實例</span><span class="sxs-lookup"><span data-stu-id="03ba5-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="03ba5-115">這個命令會使用 Edition 與 ComputeGeneration 參數來建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="03ba5-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="03ba5-116">範例3：使用實例池物件在實例池中建立新的實例</span><span class="sxs-lookup"><span data-stu-id="03ba5-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="03ba5-117">這個命令會使用實例池物件在實例池中建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="03ba5-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="03ba5-118">範例4：使用實例池資源識別碼在實例池中建立新的實例</span><span class="sxs-lookup"><span data-stu-id="03ba5-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="03ba5-119">這個命令會使用實例池的資源識別碼，在實例池中建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="03ba5-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="03ba5-120">範例5：在實例池中建立新實例</span><span class="sxs-lookup"><span data-stu-id="03ba5-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="03ba5-121">這個命令會在名為 instancePool0 的實例池中建立新的實例</span><span class="sxs-lookup"><span data-stu-id="03ba5-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="03ba5-122">參數</span><span class="sxs-lookup"><span data-stu-id="03ba5-122">PARAMETERS</span></span>

### <span data-ttu-id="03ba5-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="03ba5-123">-AdministratorCredential</span></span>
<span data-ttu-id="03ba5-124">實例的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="03ba5-124">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03ba5-125">-AsJob</span></span>
<span data-ttu-id="03ba5-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="03ba5-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03ba5-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="03ba5-127">-AssignIdentity</span></span>
<span data-ttu-id="03ba5-128">針對此受管理的實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="03ba5-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="03ba5-129">-排序規則</span><span class="sxs-lookup"><span data-stu-id="03ba5-129">-Collation</span></span>
<span data-ttu-id="03ba5-130">要使用之 Azure SQL Managed 實例的排序規則。</span><span class="sxs-lookup"><span data-stu-id="03ba5-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="03ba5-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="03ba5-131">-ComputeGeneration</span></span>
<span data-ttu-id="03ba5-132">該實例的計算產生。</span><span class="sxs-lookup"><span data-stu-id="03ba5-132">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ba5-133">-DefaultProfile</span></span>
<span data-ttu-id="03ba5-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03ba5-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="03ba5-135">-DnsZonePartner</span></span>
<span data-ttu-id="03ba5-136">合作夥伴管理伺服器的資源識別碼，以繼承受管理實例建立的 DnsZone 屬性</span><span class="sxs-lookup"><span data-stu-id="03ba5-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="03ba5-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="03ba5-137">-Edition</span></span>
<span data-ttu-id="03ba5-138">實例的版本。</span><span class="sxs-lookup"><span data-stu-id="03ba5-138">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="03ba5-139">-InstancePool</span></span>
<span data-ttu-id="03ba5-140">實例池父物件。</span><span class="sxs-lookup"><span data-stu-id="03ba5-140">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-141">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="03ba5-141">-InstancePoolName</span></span>
<span data-ttu-id="03ba5-142">要放置此實例的實例池。</span><span class="sxs-lookup"><span data-stu-id="03ba5-142">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-143">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="03ba5-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="03ba5-144">實例池資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="03ba5-144">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="03ba5-145">-LicenseType</span></span>
<span data-ttu-id="03ba5-146">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="03ba5-146">Determines which License Type to use.</span></span> <span data-ttu-id="03ba5-147">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="03ba5-147">Possible values are:</span></span>
- <span data-ttu-id="03ba5-148">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="03ba5-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="03ba5-149">系統會針對現有的 SQL Server 授權擁有者，將折扣提供給受管理的實例服務價格。</span><span class="sxs-lookup"><span data-stu-id="03ba5-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="03ba5-150">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="03ba5-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="03ba5-151">受管理的實例服務價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="03ba5-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-152">-位置</span><span class="sxs-lookup"><span data-stu-id="03ba5-152">-Location</span></span>
<span data-ttu-id="03ba5-153">建立實例的位置</span><span class="sxs-lookup"><span data-stu-id="03ba5-153">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-154">-名稱</span><span class="sxs-lookup"><span data-stu-id="03ba5-154">-Name</span></span>
<span data-ttu-id="03ba5-155">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="03ba5-155">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="03ba5-156">-ProxyOverride</span></span>
<span data-ttu-id="03ba5-157">用來連接至實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="03ba5-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="03ba5-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="03ba5-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="03ba5-159">是否已針對實例啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="03ba5-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="03ba5-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ba5-160">-ResourceGroupName</span></span>
<span data-ttu-id="03ba5-161">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03ba5-161">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="03ba5-162">-SkuName</span></span>
<span data-ttu-id="03ba5-163">實例的 SKU 名稱（例如 "GP_Gen4"，"BC_Gen4"）。</span><span class="sxs-lookup"><span data-stu-id="03ba5-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="03ba5-164">-StorageSizeInGB</span></span>
<span data-ttu-id="03ba5-165">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="03ba5-165">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="03ba5-166">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="03ba5-166">-SubnetId</span></span>
<span data-ttu-id="03ba5-167">要用於建立實例的子網識別碼</span><span class="sxs-lookup"><span data-stu-id="03ba5-167">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="03ba5-168">-Tag</span></span>
<span data-ttu-id="03ba5-169">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="03ba5-169">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-170">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="03ba5-170">-TimezoneId</span></span>
<span data-ttu-id="03ba5-171">要設定之實例的時區 id。</span><span class="sxs-lookup"><span data-stu-id="03ba5-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="03ba5-172">時區識別碼的清單會透過 sys.time_zone_info (Transact-sql) view 公開。</span><span class="sxs-lookup"><span data-stu-id="03ba5-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="03ba5-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="03ba5-173">-VCore</span></span>
<span data-ttu-id="03ba5-174">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="03ba5-174">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ba5-175">-確認</span><span class="sxs-lookup"><span data-stu-id="03ba5-175">-Confirm</span></span>
<span data-ttu-id="03ba5-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03ba5-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ba5-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ba5-177">-WhatIf</span></span>
<span data-ttu-id="03ba5-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03ba5-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ba5-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03ba5-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ba5-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ba5-180">CommonParameters</span></span>
<span data-ttu-id="03ba5-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03ba5-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ba5-182">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="03ba5-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ba5-183">輸入</span><span class="sxs-lookup"><span data-stu-id="03ba5-183">INPUTS</span></span>

### <span data-ttu-id="03ba5-184">所有</span><span class="sxs-lookup"><span data-stu-id="03ba5-184">None</span></span>

## <span data-ttu-id="03ba5-185">輸出</span><span class="sxs-lookup"><span data-stu-id="03ba5-185">OUTPUTS</span></span>

### <span data-ttu-id="03ba5-186">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="03ba5-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="03ba5-187">筆記</span><span class="sxs-lookup"><span data-stu-id="03ba5-187">NOTES</span></span>

## <span data-ttu-id="03ba5-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="03ba5-188">RELATED LINKS</span></span>
