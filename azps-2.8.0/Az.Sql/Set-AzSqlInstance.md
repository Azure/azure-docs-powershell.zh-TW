---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792641"
---
# <span data-ttu-id="808a8-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="808a8-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="808a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="808a8-102">SYNOPSIS</span></span>
<span data-ttu-id="808a8-103">設定 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="808a8-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="808a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="808a8-104">SYNTAX</span></span>

### <span data-ttu-id="808a8-105">SetInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="808a8-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="808a8-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="808a8-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="808a8-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="808a8-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="808a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="808a8-108">DESCRIPTION</span></span>
<span data-ttu-id="808a8-109">**AzSqlInstance** Cmdlet 會修改 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="808a8-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="808a8-110">示例</span><span class="sxs-lookup"><span data-stu-id="808a8-110">EXAMPLES</span></span>

### <span data-ttu-id="808a8-111">範例1：使用新的值（AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore）來設定現有實例</span><span class="sxs-lookup"><span data-stu-id="808a8-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="808a8-112">這個命令會使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值來設定現有實例。</span><span class="sxs-lookup"><span data-stu-id="808a8-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="808a8-113">範例2：使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值設定現有的實例，在實例池中</span><span class="sxs-lookup"><span data-stu-id="808a8-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="808a8-114">這個命令會使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值，為實例池中的實例設定現有的實例</span><span class="sxs-lookup"><span data-stu-id="808a8-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="808a8-115">參數</span><span class="sxs-lookup"><span data-stu-id="808a8-115">PARAMETERS</span></span>

### <span data-ttu-id="808a8-116">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="808a8-116">-AdministratorPassword</span></span>
<span data-ttu-id="808a8-117">該實例的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="808a8-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="808a8-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="808a8-118">-AssignIdentity</span></span>
<span data-ttu-id="808a8-119">針對此實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="808a8-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="808a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808a8-120">-DefaultProfile</span></span>
<span data-ttu-id="808a8-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="808a8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808a8-122">-Edition</span><span class="sxs-lookup"><span data-stu-id="808a8-122">-Edition</span></span>
<span data-ttu-id="808a8-123">要指派給實例的版本。</span><span class="sxs-lookup"><span data-stu-id="808a8-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="808a8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="808a8-124">-Force</span></span>
<span data-ttu-id="808a8-125">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="808a8-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="808a8-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="808a8-126">-InputObject</span></span>
<span data-ttu-id="808a8-127">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="808a8-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="808a8-128">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="808a8-128">-InstancePoolName</span></span>
<span data-ttu-id="808a8-129">實例池名稱。</span><span class="sxs-lookup"><span data-stu-id="808a8-129">The instance pool name.</span></span>

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

### <span data-ttu-id="808a8-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="808a8-130">-LicenseType</span></span>
<span data-ttu-id="808a8-131">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="808a8-131">Determines which License Type to use.</span></span> <span data-ttu-id="808a8-132">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="808a8-132">Possible values are:</span></span>
- <span data-ttu-id="808a8-133">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="808a8-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="808a8-134">系統會針對現有的 SQL Server 授權擁有者，將折扣提供給受管理的實例服務價格。</span><span class="sxs-lookup"><span data-stu-id="808a8-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="808a8-135">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="808a8-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="808a8-136">受管理的實例服務價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="808a8-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="808a8-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="808a8-137">-Name</span></span>
<span data-ttu-id="808a8-138">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="808a8-138">Instance name.</span></span>

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

### <span data-ttu-id="808a8-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="808a8-139">-ProxyOverride</span></span>
<span data-ttu-id="808a8-140">用來連接至實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="808a8-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="808a8-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="808a8-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="808a8-142">是否已針對實例啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="808a8-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="808a8-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808a8-143">-ResourceGroupName</span></span>
<span data-ttu-id="808a8-144">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="808a8-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="808a8-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="808a8-145">-ResourceId</span></span>
<span data-ttu-id="808a8-146">要移除之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="808a8-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="808a8-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="808a8-147">-StorageSizeInGB</span></span>
<span data-ttu-id="808a8-148">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="808a8-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="808a8-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="808a8-149">-Tag</span></span>
<span data-ttu-id="808a8-150">要與實例建立關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="808a8-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="808a8-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="808a8-151">-VCore</span></span>
<span data-ttu-id="808a8-152">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="808a8-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="808a8-153">-確認</span><span class="sxs-lookup"><span data-stu-id="808a8-153">-Confirm</span></span>
<span data-ttu-id="808a8-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="808a8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="808a8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808a8-155">-WhatIf</span></span>
<span data-ttu-id="808a8-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="808a8-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808a8-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="808a8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="808a8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808a8-158">CommonParameters</span></span>
<span data-ttu-id="808a8-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="808a8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808a8-160">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="808a8-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808a8-161">輸入</span><span class="sxs-lookup"><span data-stu-id="808a8-161">INPUTS</span></span>

### <span data-ttu-id="808a8-162">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="808a8-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="808a8-163">System.object</span><span class="sxs-lookup"><span data-stu-id="808a8-163">System.String</span></span>

## <span data-ttu-id="808a8-164">輸出</span><span class="sxs-lookup"><span data-stu-id="808a8-164">OUTPUTS</span></span>

### <span data-ttu-id="808a8-165">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="808a8-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="808a8-166">筆記</span><span class="sxs-lookup"><span data-stu-id="808a8-166">NOTES</span></span>

## <span data-ttu-id="808a8-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="808a8-167">RELATED LINKS</span></span>
