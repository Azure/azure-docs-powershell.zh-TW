---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614833"
---
# <span data-ttu-id="0b366-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0b366-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="0b366-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b366-102">SYNOPSIS</span></span>
<span data-ttu-id="0b366-103">建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="0b366-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="0b366-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b366-104">SYNTAX</span></span>

### <span data-ttu-id="0b366-105">NewByEditionAndComputeGenerationParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0b366-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b366-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="0b366-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b366-107">說明</span><span class="sxs-lookup"><span data-stu-id="0b366-107">DESCRIPTION</span></span>
<span data-ttu-id="0b366-108">**新的-AzSqlInstance** Cmdlet 會建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="0b366-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="0b366-109">示例</span><span class="sxs-lookup"><span data-stu-id="0b366-109">EXAMPLES</span></span>

### <span data-ttu-id="0b366-110">範例1：建立新的實例</span><span class="sxs-lookup"><span data-stu-id="0b366-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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
```

<span data-ttu-id="0b366-111">這個命令會使用 Edition 及 ComputeGeneration 參數建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="0b366-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="0b366-112">範例2：建立新的實例</span><span class="sxs-lookup"><span data-stu-id="0b366-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="0b366-113">這個命令會使用 Edition 與 ComputeGeneration 參數來建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="0b366-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="0b366-114">參數</span><span class="sxs-lookup"><span data-stu-id="0b366-114">PARAMETERS</span></span>

### <span data-ttu-id="0b366-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="0b366-115">-AdministratorCredential</span></span>
<span data-ttu-id="0b366-116">實例的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="0b366-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="0b366-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b366-117">-AsJob</span></span>
<span data-ttu-id="0b366-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0b366-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b366-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0b366-119">-AssignIdentity</span></span>
<span data-ttu-id="0b366-120">針對此受管理的實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="0b366-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0b366-121">-排序規則</span><span class="sxs-lookup"><span data-stu-id="0b366-121">-Collation</span></span>
<span data-ttu-id="0b366-122">要使用之 Azure SQL Managed 實例的排序規則。</span><span class="sxs-lookup"><span data-stu-id="0b366-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="0b366-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0b366-123">-ComputeGeneration</span></span>
<span data-ttu-id="0b366-124">該實例的計算產生。</span><span class="sxs-lookup"><span data-stu-id="0b366-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="0b366-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b366-125">-DefaultProfile</span></span>
<span data-ttu-id="0b366-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b366-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b366-127">-Edition</span><span class="sxs-lookup"><span data-stu-id="0b366-127">-Edition</span></span>
<span data-ttu-id="0b366-128">實例的版本。</span><span class="sxs-lookup"><span data-stu-id="0b366-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="0b366-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0b366-129">-LicenseType</span></span>
<span data-ttu-id="0b366-130">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="0b366-130">Determines which License Type to use.</span></span> <span data-ttu-id="0b366-131">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="0b366-131">Possible values are:</span></span>
- <span data-ttu-id="0b366-132">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="0b366-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="0b366-133">系統會針對現有的 SQL Server 授權擁有者，將折扣提供給受管理的實例服務價格。</span><span class="sxs-lookup"><span data-stu-id="0b366-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="0b366-134">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="0b366-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="0b366-135">受管理的實例服務價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="0b366-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b366-136">-位置</span><span class="sxs-lookup"><span data-stu-id="0b366-136">-Location</span></span>
<span data-ttu-id="0b366-137">建立實例的位置</span><span class="sxs-lookup"><span data-stu-id="0b366-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b366-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b366-138">-Name</span></span>
<span data-ttu-id="0b366-139">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="0b366-139">Instance name.</span></span>

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

### <span data-ttu-id="0b366-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="0b366-140">-ProxyOverride</span></span>
<span data-ttu-id="0b366-141">用來連接至實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="0b366-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="0b366-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="0b366-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="0b366-143">是否已針對實例啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="0b366-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="0b366-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b366-144">-ResourceGroupName</span></span>
<span data-ttu-id="0b366-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b366-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b366-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0b366-146">-SkuName</span></span>
<span data-ttu-id="0b366-147">實例的 SKU 名稱（例如 "GP_Gen4"，"BC_Gen4"）。</span><span class="sxs-lookup"><span data-stu-id="0b366-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="0b366-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0b366-148">-StorageSizeInGB</span></span>
<span data-ttu-id="0b366-149">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="0b366-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="0b366-150">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0b366-150">-SubnetId</span></span>
<span data-ttu-id="0b366-151">要用於建立實例的子網識別碼</span><span class="sxs-lookup"><span data-stu-id="0b366-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b366-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b366-152">-Tag</span></span>
<span data-ttu-id="0b366-153">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="0b366-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="0b366-154">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="0b366-154">-TimezoneId</span></span>
<span data-ttu-id="0b366-155">要設定之實例的時區 id。</span><span class="sxs-lookup"><span data-stu-id="0b366-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="0b366-156">時區識別碼的清單會透過 sys.time_zone_info (Transact-sql) view 公開。</span><span class="sxs-lookup"><span data-stu-id="0b366-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="0b366-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="0b366-157">-VCore</span></span>
<span data-ttu-id="0b366-158">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="0b366-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="0b366-159">-確認</span><span class="sxs-lookup"><span data-stu-id="0b366-159">-Confirm</span></span>
<span data-ttu-id="0b366-160">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b366-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b366-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b366-161">-WhatIf</span></span>
<span data-ttu-id="0b366-162">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b366-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b366-163">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b366-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b366-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b366-164">CommonParameters</span></span>
<span data-ttu-id="0b366-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b366-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b366-166">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b366-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b366-167">輸入</span><span class="sxs-lookup"><span data-stu-id="0b366-167">INPUTS</span></span>

### <span data-ttu-id="0b366-168">所有</span><span class="sxs-lookup"><span data-stu-id="0b366-168">None</span></span>

## <span data-ttu-id="0b366-169">輸出</span><span class="sxs-lookup"><span data-stu-id="0b366-169">OUTPUTS</span></span>

### <span data-ttu-id="0b366-170">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="0b366-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="0b366-171">筆記</span><span class="sxs-lookup"><span data-stu-id="0b366-171">NOTES</span></span>

## <span data-ttu-id="0b366-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b366-172">RELATED LINKS</span></span>
