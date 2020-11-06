---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: ad98b764eac08c9fb1f6d3dd367d78ca1b5d45d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614714"
---
# <span data-ttu-id="0e2a6-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e2a6-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="0e2a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e2a6-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2a6-103">設定 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="0e2a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e2a6-104">SYNTAX</span></span>

### <span data-ttu-id="0e2a6-105">SetInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="0e2a6-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e2a6-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="0e2a6-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e2a6-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0e2a6-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e2a6-108">說明</span><span class="sxs-lookup"><span data-stu-id="0e2a6-108">DESCRIPTION</span></span>
<span data-ttu-id="0e2a6-109">**AzSqlInstance** Cmdlet 會修改 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="0e2a6-110">示例</span><span class="sxs-lookup"><span data-stu-id="0e2a6-110">EXAMPLES</span></span>

### <span data-ttu-id="0e2a6-111">範例1：使用新的值（AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore）來設定現有實例</span><span class="sxs-lookup"><span data-stu-id="0e2a6-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
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
```

<span data-ttu-id="0e2a6-112">這個命令會使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值來設定現有實例。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="0e2a6-113">參數</span><span class="sxs-lookup"><span data-stu-id="0e2a6-113">PARAMETERS</span></span>

### <span data-ttu-id="0e2a6-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="0e2a6-114">-AdministratorPassword</span></span>
<span data-ttu-id="0e2a6-115">該實例的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-115">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="0e2a6-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0e2a6-116">-AssignIdentity</span></span>
<span data-ttu-id="0e2a6-117">針對此實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0e2a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2a6-118">-DefaultProfile</span></span>
<span data-ttu-id="0e2a6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e2a6-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="0e2a6-120">-Edition</span></span>
<span data-ttu-id="0e2a6-121">要指派給實例的版本。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-121">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="0e2a6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0e2a6-122">-Force</span></span>
<span data-ttu-id="0e2a6-123">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="0e2a6-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0e2a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e2a6-124">-InputObject</span></span>
<span data-ttu-id="0e2a6-125">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="0e2a6-125">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="0e2a6-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0e2a6-126">-LicenseType</span></span>
<span data-ttu-id="0e2a6-127">決定要使用哪一種授權類型。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-127">Determines which License Type to use.</span></span> <span data-ttu-id="0e2a6-128">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="0e2a6-128">Possible values are:</span></span>
- <span data-ttu-id="0e2a6-129">BasePrice-Azure 混合式福利 () AHB 現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-129">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="0e2a6-130">系統會針對現有的 SQL Server 授權擁有者，將折扣提供給受管理的實例服務價格。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-130">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="0e2a6-131">LicenseIncluded-Azure 混合式福利 () AHB 不會套用現有 SQL Server 授權擁有者的折扣價格。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-131">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="0e2a6-132">受管理的實例服務價格將包含新的 SQL Server 授權成本。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-132">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="0e2a6-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e2a6-133">-Name</span></span>
<span data-ttu-id="0e2a6-134">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-134">Instance name.</span></span>

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

### <span data-ttu-id="0e2a6-135">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="0e2a6-135">-ProxyOverride</span></span>
<span data-ttu-id="0e2a6-136">用來連接至實例的連線類型。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-136">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="0e2a6-137">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="0e2a6-137">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="0e2a6-138">是否已針對實例啟用公用資料端點。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-138">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="0e2a6-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e2a6-139">-ResourceGroupName</span></span>
<span data-ttu-id="0e2a6-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e2a6-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e2a6-141">-ResourceId</span></span>
<span data-ttu-id="0e2a6-142">要移除之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0e2a6-142">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="0e2a6-143">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0e2a6-143">-StorageSizeInGB</span></span>
<span data-ttu-id="0e2a6-144">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="0e2a6-144">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="0e2a6-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e2a6-145">-Tag</span></span>
<span data-ttu-id="0e2a6-146">要與實例建立關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-146">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="0e2a6-147">-VCore</span><span class="sxs-lookup"><span data-stu-id="0e2a6-147">-VCore</span></span>
<span data-ttu-id="0e2a6-148">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="0e2a6-148">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="0e2a6-149">-確認</span><span class="sxs-lookup"><span data-stu-id="0e2a6-149">-Confirm</span></span>
<span data-ttu-id="0e2a6-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e2a6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2a6-151">-WhatIf</span></span>
<span data-ttu-id="0e2a6-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e2a6-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e2a6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2a6-154">CommonParameters</span></span>
<span data-ttu-id="0e2a6-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2a6-156">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0e2a6-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2a6-157">輸入</span><span class="sxs-lookup"><span data-stu-id="0e2a6-157">INPUTS</span></span>

### <span data-ttu-id="0e2a6-158">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="0e2a6-158">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="0e2a6-159">System.object</span><span class="sxs-lookup"><span data-stu-id="0e2a6-159">System.String</span></span>

## <span data-ttu-id="0e2a6-160">輸出</span><span class="sxs-lookup"><span data-stu-id="0e2a6-160">OUTPUTS</span></span>

### <span data-ttu-id="0e2a6-161">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="0e2a6-161">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="0e2a6-162">筆記</span><span class="sxs-lookup"><span data-stu-id="0e2a6-162">NOTES</span></span>

## <span data-ttu-id="0e2a6-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e2a6-163">RELATED LINKS</span></span>
