---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906473"
---
# <span data-ttu-id="37838-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="37838-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="37838-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37838-102">SYNOPSIS</span></span>
<span data-ttu-id="37838-103">建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="37838-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="37838-104">語法</span><span class="sxs-lookup"><span data-stu-id="37838-104">SYNTAX</span></span>

### <span data-ttu-id="37838-105">NewByEditionAndComputeGenerationParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="37838-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37838-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37838-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37838-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37838-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37838-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="37838-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37838-109">描述</span><span class="sxs-lookup"><span data-stu-id="37838-109">DESCRIPTION</span></span>
<span data-ttu-id="37838-110">**New-AzSqlInstance** Cmdlet 會建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="37838-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="37838-111">例子</span><span class="sxs-lookup"><span data-stu-id="37838-111">EXAMPLES</span></span>

### <span data-ttu-id="37838-112">範例 1：建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="37838-113">此命令會使用 SKUName 參數建立新實例。</span><span class="sxs-lookup"><span data-stu-id="37838-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="37838-114">範例 2：建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="37838-115">此命令會使用 Edition 和 ComputeGeneration 參數來建立新實例。</span><span class="sxs-lookup"><span data-stu-id="37838-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="37838-116">範例 3：使用實例資料庫物件在實例資料庫內建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="37838-117">此命令會使用實例資料庫物件在實例資料庫內建立新實例。</span><span class="sxs-lookup"><span data-stu-id="37838-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="37838-118">範例 4：在實例資料庫使用實例資料庫資源識別碼建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="37838-119">此命令會使用實例資料庫的資源識別碼，在實例資料庫內建立新實例。</span><span class="sxs-lookup"><span data-stu-id="37838-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="37838-120">範例 5：在實例資料庫建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="37838-121">此命令會使用 name instancePool0 在實例資料庫建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="37838-122">範例 6：使用維護組配置建立新實例</span><span class="sxs-lookup"><span data-stu-id="37838-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="37838-123">此命令會建立具有維護組MI_2</span><span class="sxs-lookup"><span data-stu-id="37838-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="37838-124">參數</span><span class="sxs-lookup"><span data-stu-id="37838-124">PARAMETERS</span></span>

### <span data-ttu-id="37838-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="37838-125">-AdministratorCredential</span></span>
<span data-ttu-id="37838-126">實例的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="37838-126">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="37838-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37838-127">-AsJob</span></span>
<span data-ttu-id="37838-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37838-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37838-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="37838-129">-AssignIdentity</span></span>
<span data-ttu-id="37838-130">為此 Managed 實例產生並指派 Azure Active Directory 身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="37838-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="37838-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="37838-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="37838-132">用來儲存 Sql Azure Managed 實例之備份的備份儲存備份的備份儲存空間。</span><span class="sxs-lookup"><span data-stu-id="37838-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="37838-133">選項為：本地、區域及地理位置</span><span class="sxs-lookup"><span data-stu-id="37838-133">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37838-134">-排序</span><span class="sxs-lookup"><span data-stu-id="37838-134">-Collation</span></span>
<span data-ttu-id="37838-135">Azure SQL Managed 實例的排序方式。</span><span class="sxs-lookup"><span data-stu-id="37838-135">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="37838-136">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="37838-136">-ComputeGeneration</span></span>
<span data-ttu-id="37838-137">實例的計算產生。</span><span class="sxs-lookup"><span data-stu-id="37838-137">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="37838-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37838-138">-DefaultProfile</span></span>
<span data-ttu-id="37838-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="37838-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37838-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="37838-140">-DnsZonePartner</span></span>
<span data-ttu-id="37838-141">從受管理實例建立繼承 DnsZone 屬性的合作夥伴 Managed Server 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="37838-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="37838-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="37838-142">-Edition</span></span>
<span data-ttu-id="37838-143">實例的版本。</span><span class="sxs-lookup"><span data-stu-id="37838-143">The edition for the instance.</span></span>

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

### <span data-ttu-id="37838-144">-強制</span><span class="sxs-lookup"><span data-stu-id="37838-144">-Force</span></span>
<span data-ttu-id="37838-145">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="37838-145">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="37838-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="37838-146">-InstancePool</span></span>
<span data-ttu-id="37838-147">實例資料庫父物件。</span><span class="sxs-lookup"><span data-stu-id="37838-147">The instance pool parent object.</span></span>

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

### <span data-ttu-id="37838-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="37838-148">-InstancePoolName</span></span>
<span data-ttu-id="37838-149">放置此實例的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="37838-149">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="37838-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="37838-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="37838-151">實例資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="37838-151">The instance pool resource id.</span></span>

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

### <span data-ttu-id="37838-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="37838-152">-LicenseType</span></span>
<span data-ttu-id="37838-153">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="37838-153">Determines which License Type to use.</span></span> <span data-ttu-id="37838-154">可能的值有：</span><span class="sxs-lookup"><span data-stu-id="37838-154">Possible values are:</span></span>
- <span data-ttu-id="37838-155">BasePrice - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="37838-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="37838-156">受管理的實例服務價格會針對現有的 SQL Server 授權擁有者折扣。</span><span class="sxs-lookup"><span data-stu-id="37838-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="37838-157">LicenseIncluded - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格不會適用。</span><span class="sxs-lookup"><span data-stu-id="37838-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="37838-158">受管理的實例服務價格會包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="37838-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="37838-159">-位置</span><span class="sxs-lookup"><span data-stu-id="37838-159">-Location</span></span>
<span data-ttu-id="37838-160">建立實例的位置</span><span class="sxs-lookup"><span data-stu-id="37838-160">The location in which to create the instance</span></span>

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

### <span data-ttu-id="37838-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="37838-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="37838-162">Sql Azure 受管理實例的維護組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="37838-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="37838-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="37838-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="37838-164">針對受管理實例強制執行的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="37838-164">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37838-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="37838-165">-Name</span></span>
<span data-ttu-id="37838-166">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="37838-166">Instance name.</span></span>

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

### <span data-ttu-id="37838-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="37838-167">-ProxyOverride</span></span>
<span data-ttu-id="37838-168">用於連接到實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="37838-168">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="37838-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="37838-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="37838-170">實例是否已啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="37838-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="37838-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37838-171">-ResourceGroupName</span></span>
<span data-ttu-id="37838-172">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37838-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="37838-173">-SKUName</span><span class="sxs-lookup"><span data-stu-id="37838-173">-SkuName</span></span>
<span data-ttu-id="37838-174">實例的 SKU 名稱，例如'GP_Gen4'、'BC_Gen4'。</span><span class="sxs-lookup"><span data-stu-id="37838-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="37838-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="37838-175">-StorageSizeInGB</span></span>
<span data-ttu-id="37838-176">決定要與實例關聯的儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="37838-176">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="37838-177">-子網Id</span><span class="sxs-lookup"><span data-stu-id="37838-177">-SubnetId</span></span>
<span data-ttu-id="37838-178">用於建立實例的子網識別碼</span><span class="sxs-lookup"><span data-stu-id="37838-178">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="37838-179">-標記</span><span class="sxs-lookup"><span data-stu-id="37838-179">-Tag</span></span>
<span data-ttu-id="37838-180">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="37838-180">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="37838-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="37838-181">-TimezoneId</span></span>
<span data-ttu-id="37838-182">要設定實例的時區識別碼。</span><span class="sxs-lookup"><span data-stu-id="37838-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="37838-183">時區識別碼清單會透過 Transact-SQL sys.time_zone_info (顯示) 顯示。</span><span class="sxs-lookup"><span data-stu-id="37838-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="37838-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="37838-184">-VCore</span></span>
<span data-ttu-id="37838-185">決定要與實例關聯多少 VCore</span><span class="sxs-lookup"><span data-stu-id="37838-185">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="37838-186">-確認</span><span class="sxs-lookup"><span data-stu-id="37838-186">-Confirm</span></span>
<span data-ttu-id="37838-187">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="37838-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37838-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37838-188">-WhatIf</span></span>
<span data-ttu-id="37838-189">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37838-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37838-190">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37838-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37838-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37838-191">CommonParameters</span></span>
<span data-ttu-id="37838-192">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37838-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37838-193">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37838-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37838-194">輸入</span><span class="sxs-lookup"><span data-stu-id="37838-194">INPUTS</span></span>

### <span data-ttu-id="37838-195">沒有</span><span class="sxs-lookup"><span data-stu-id="37838-195">None</span></span>

## <span data-ttu-id="37838-196">輸出</span><span class="sxs-lookup"><span data-stu-id="37838-196">OUTPUTS</span></span>

### <span data-ttu-id="37838-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="37838-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="37838-198">筆記</span><span class="sxs-lookup"><span data-stu-id="37838-198">NOTES</span></span>

## <span data-ttu-id="37838-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="37838-199">RELATED LINKS</span></span>
