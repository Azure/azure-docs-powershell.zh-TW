---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136998"
---
# <span data-ttu-id="fbfe6-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="fbfe6-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="fbfe6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfe6-103">設定 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="fbfe6-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbfe6-104">SYNTAX</span></span>

### <span data-ttu-id="fbfe6-105">SetInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="fbfe6-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfe6-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="fbfe6-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbfe6-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="fbfe6-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbfe6-108">說明</span><span class="sxs-lookup"><span data-stu-id="fbfe6-108">DESCRIPTION</span></span>
<span data-ttu-id="fbfe6-109">**AzSqlInstance** Cmdlet 會修改 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="fbfe6-110">示例</span><span class="sxs-lookup"><span data-stu-id="fbfe6-110">EXAMPLES</span></span>

### <span data-ttu-id="fbfe6-111">範例1：使用新的值（AdministratorPassword、-LicenseType、-StorageSizeInGB、-VCore 及-Edition）來設定現有實例</span><span class="sxs-lookup"><span data-stu-id="fbfe6-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="fbfe6-112">範例2：使用 ComputeGeneration 的新值變更現有的實例硬體產生</span><span class="sxs-lookup"><span data-stu-id="fbfe6-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="fbfe6-113">這個命令會使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值來設定現有實例。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="fbfe6-114">範例3：使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值設定現有的實例，在實例池中</span><span class="sxs-lookup"><span data-stu-id="fbfe6-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="fbfe6-115">這個命令會使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值，為實例池中的實例設定現有的實例</span><span class="sxs-lookup"><span data-stu-id="fbfe6-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="fbfe6-116">參數</span><span class="sxs-lookup"><span data-stu-id="fbfe6-116">PARAMETERS</span></span>

### <span data-ttu-id="fbfe6-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="fbfe6-117">-AdministratorPassword</span></span>
<span data-ttu-id="fbfe6-118">該實例的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="fbfe6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbfe6-119">-AsJob</span></span>
<span data-ttu-id="fbfe6-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fbfe6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbfe6-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fbfe6-121">-AssignIdentity</span></span>
<span data-ttu-id="fbfe6-122">針對此實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="fbfe6-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="fbfe6-123">-ComputeGeneration</span></span>
<span data-ttu-id="fbfe6-124">該實例的計算產生。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="fbfe6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfe6-125">-DefaultProfile</span></span>
<span data-ttu-id="fbfe6-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbfe6-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="fbfe6-127">-Edition</span></span>
<span data-ttu-id="fbfe6-128">要指派給實例的版本。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="fbfe6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="fbfe6-129">-Force</span></span>
<span data-ttu-id="fbfe6-130">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="fbfe6-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fbfe6-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbfe6-131">-InputObject</span></span>
<span data-ttu-id="fbfe6-132">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="fbfe6-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="fbfe6-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="fbfe6-133">-InstancePoolName</span></span>
<span data-ttu-id="fbfe6-134">實例池名稱。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-134">The instance pool name.</span></span>

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

### <span data-ttu-id="fbfe6-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fbfe6-135">-LicenseType</span></span>
<span data-ttu-id="fbfe6-136">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-136">Determines which License Type to use.</span></span> <span data-ttu-id="fbfe6-137">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="fbfe6-137">Possible values are:</span></span>
- <span data-ttu-id="fbfe6-138">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="fbfe6-139">系統會針對現有的 SQL Server 授權擁有者，將折扣提供給受管理的實例服務價格。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="fbfe6-140">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="fbfe6-141">受管理的實例服務價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="fbfe6-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fbfe6-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="fbfe6-143">Sql Azure 管理實例的維護配置識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="fbfe6-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="fbfe6-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="fbfe6-145">要針對受管理的實例強制執行的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="fbfe6-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="fbfe6-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="fbfe6-146">-Name</span></span>
<span data-ttu-id="fbfe6-147">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-147">Instance name.</span></span>

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

### <span data-ttu-id="fbfe6-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="fbfe6-148">-ProxyOverride</span></span>
<span data-ttu-id="fbfe6-149">用來連接至實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="fbfe6-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="fbfe6-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="fbfe6-151">是否已針對實例啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="fbfe6-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfe6-152">-ResourceGroupName</span></span>
<span data-ttu-id="fbfe6-153">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbfe6-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbfe6-154">-ResourceId</span></span>
<span data-ttu-id="fbfe6-155">要移除之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fbfe6-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="fbfe6-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fbfe6-156">-StorageSizeInGB</span></span>
<span data-ttu-id="fbfe6-157">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="fbfe6-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="fbfe6-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbfe6-158">-Tag</span></span>
<span data-ttu-id="fbfe6-159">要與實例建立關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="fbfe6-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="fbfe6-160">-VCore</span></span>
<span data-ttu-id="fbfe6-161">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="fbfe6-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="fbfe6-162">-確認</span><span class="sxs-lookup"><span data-stu-id="fbfe6-162">-Confirm</span></span>
<span data-ttu-id="fbfe6-163">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbfe6-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbfe6-164">-WhatIf</span></span>
<span data-ttu-id="fbfe6-165">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbfe6-166">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbfe6-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfe6-167">CommonParameters</span></span>
<span data-ttu-id="fbfe6-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfe6-169">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fbfe6-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfe6-170">輸入</span><span class="sxs-lookup"><span data-stu-id="fbfe6-170">INPUTS</span></span>

### <span data-ttu-id="fbfe6-171">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="fbfe6-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="fbfe6-172">System.object</span><span class="sxs-lookup"><span data-stu-id="fbfe6-172">System.String</span></span>

## <span data-ttu-id="fbfe6-173">輸出</span><span class="sxs-lookup"><span data-stu-id="fbfe6-173">OUTPUTS</span></span>

### <span data-ttu-id="fbfe6-174">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="fbfe6-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="fbfe6-175">筆記</span><span class="sxs-lookup"><span data-stu-id="fbfe6-175">NOTES</span></span>

## <span data-ttu-id="fbfe6-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbfe6-176">RELATED LINKS</span></span>
