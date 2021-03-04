---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917889"
---
# <span data-ttu-id="678e1-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="678e1-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="678e1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="678e1-102">SYNOPSIS</span></span>
<span data-ttu-id="678e1-103">設定 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="678e1-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="678e1-104">語法</span><span class="sxs-lookup"><span data-stu-id="678e1-104">SYNTAX</span></span>

### <span data-ttu-id="678e1-105">SetInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="678e1-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678e1-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="678e1-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678e1-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="678e1-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="678e1-108">描述</span><span class="sxs-lookup"><span data-stu-id="678e1-108">DESCRIPTION</span></span>
<span data-ttu-id="678e1-109">**Set-AzSqlInstance Cmdlet** 會修改 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="678e1-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="678e1-110">例子</span><span class="sxs-lookup"><span data-stu-id="678e1-110">EXAMPLES</span></span>

### <span data-ttu-id="678e1-111">範例 1：使用 -AdministratorPassword、-LicenseType、-StorageSizeInGB、-VCore 和 -Edition 的新值設定現有實例</span><span class="sxs-lookup"><span data-stu-id="678e1-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="678e1-112">範例 2：使用 -ComputeGeneration 的新值變更現有的實例硬體產生</span><span class="sxs-lookup"><span data-stu-id="678e1-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="678e1-113">此命令會使用 -AdministratorPassword、-LicenseType、-StorageSizeInGB 和 -VCore 的新值來設定現有實例</span><span class="sxs-lookup"><span data-stu-id="678e1-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="678e1-114">範例 3：針對實例集區中的實例，使用 -AdministratorPassword、-LicenseType、-StorageSizeInGB 和 -VCore 的新值設定現有實例</span><span class="sxs-lookup"><span data-stu-id="678e1-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="678e1-115">此命令會針對實例集區中的實例，使用 -AdministratorPassword、-LicenseType、-StorageSizeInGB 和 -VCore 的新值來設定現有實例</span><span class="sxs-lookup"><span data-stu-id="678e1-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="678e1-116">範例 4：更新現有實例的維護組</span><span class="sxs-lookup"><span data-stu-id="678e1-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="678e1-117">此命令會以維護組MI_2</span><span class="sxs-lookup"><span data-stu-id="678e1-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="678e1-118">範例 5：從現有實例移除維護組</span><span class="sxs-lookup"><span data-stu-id="678e1-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="678e1-119">此命令會對現有實例將維護設定重設為預設值</span><span class="sxs-lookup"><span data-stu-id="678e1-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="678e1-120">參數</span><span class="sxs-lookup"><span data-stu-id="678e1-120">PARAMETERS</span></span>

### <span data-ttu-id="678e1-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="678e1-121">-AdministratorPassword</span></span>
<span data-ttu-id="678e1-122">實例的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="678e1-122">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="678e1-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="678e1-123">-AsJob</span></span>
<span data-ttu-id="678e1-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="678e1-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="678e1-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="678e1-125">-AssignIdentity</span></span>
<span data-ttu-id="678e1-126">為此實例產生並指派 Azure Active Directory 身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="678e1-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="678e1-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="678e1-127">-ComputeGeneration</span></span>
<span data-ttu-id="678e1-128">實例的計算產生。</span><span class="sxs-lookup"><span data-stu-id="678e1-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="678e1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678e1-129">-DefaultProfile</span></span>
<span data-ttu-id="678e1-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="678e1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678e1-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="678e1-131">-Edition</span></span>
<span data-ttu-id="678e1-132">要指派給實例的版本。</span><span class="sxs-lookup"><span data-stu-id="678e1-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="678e1-133">-強制</span><span class="sxs-lookup"><span data-stu-id="678e1-133">-Force</span></span>
<span data-ttu-id="678e1-134">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="678e1-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="678e1-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="678e1-135">-InputObject</span></span>
<span data-ttu-id="678e1-136">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="678e1-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="678e1-137">-InstancePoolName</span></span>
<span data-ttu-id="678e1-138">實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="678e1-138">The instance pool name.</span></span>

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

### <span data-ttu-id="678e1-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="678e1-139">-LicenseType</span></span>
<span data-ttu-id="678e1-140">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="678e1-140">Determines which License Type to use.</span></span> <span data-ttu-id="678e1-141">可能的值有：</span><span class="sxs-lookup"><span data-stu-id="678e1-141">Possible values are:</span></span>
- <span data-ttu-id="678e1-142">BasePrice - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="678e1-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="678e1-143">受管理的實例服務價格會針對現有的 SQL Server 授權擁有者折扣。</span><span class="sxs-lookup"><span data-stu-id="678e1-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="678e1-144">LicenseIncluded - Azure 混合式權益 (AHB) 現有 SQL Server 授權擁有者的折扣價格不會適用。</span><span class="sxs-lookup"><span data-stu-id="678e1-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="678e1-145">受管理的實例服務價格會包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="678e1-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="678e1-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="678e1-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="678e1-147">Sql Azure 受管理實例的維護組組識別碼。</span><span class="sxs-lookup"><span data-stu-id="678e1-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="678e1-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="678e1-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="678e1-149">針對受管理實例強制執行的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="678e1-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="678e1-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="678e1-150">-Name</span></span>
<span data-ttu-id="678e1-151">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="678e1-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="678e1-152">-ProxyOverride</span></span>
<span data-ttu-id="678e1-153">用於連接到實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="678e1-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="678e1-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="678e1-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="678e1-155">實例是否已啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="678e1-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678e1-156">-ResourceGroupName</span></span>
<span data-ttu-id="678e1-157">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="678e1-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="678e1-158">-ResourceId</span></span>
<span data-ttu-id="678e1-159">要移除的實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="678e1-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="678e1-160">-StorageSizeInGB</span></span>
<span data-ttu-id="678e1-161">決定要與實例關聯的儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="678e1-161">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-162">-標記</span><span class="sxs-lookup"><span data-stu-id="678e1-162">-Tag</span></span>
<span data-ttu-id="678e1-163">要與實例關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="678e1-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="678e1-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="678e1-164">-VCore</span></span>
<span data-ttu-id="678e1-165">決定要與實例關聯多少 VCore</span><span class="sxs-lookup"><span data-stu-id="678e1-165">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678e1-166">-確認</span><span class="sxs-lookup"><span data-stu-id="678e1-166">-Confirm</span></span>
<span data-ttu-id="678e1-167">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="678e1-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678e1-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678e1-168">-WhatIf</span></span>
<span data-ttu-id="678e1-169">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="678e1-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="678e1-170">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="678e1-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="678e1-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678e1-171">CommonParameters</span></span>
<span data-ttu-id="678e1-172">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="678e1-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678e1-173">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="678e1-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678e1-174">輸入</span><span class="sxs-lookup"><span data-stu-id="678e1-174">INPUTS</span></span>

### <span data-ttu-id="678e1-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="678e1-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="678e1-176">System.String</span><span class="sxs-lookup"><span data-stu-id="678e1-176">System.String</span></span>

## <span data-ttu-id="678e1-177">輸出</span><span class="sxs-lookup"><span data-stu-id="678e1-177">OUTPUTS</span></span>

### <span data-ttu-id="678e1-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="678e1-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="678e1-179">筆記</span><span class="sxs-lookup"><span data-stu-id="678e1-179">NOTES</span></span>

## <span data-ttu-id="678e1-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="678e1-180">RELATED LINKS</span></span>
