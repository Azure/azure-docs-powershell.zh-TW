---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455939"
---
# <span data-ttu-id="5df67-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5df67-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="5df67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5df67-102">SYNOPSIS</span></span>
<span data-ttu-id="5df67-103">建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="5df67-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5df67-104">句法</span><span class="sxs-lookup"><span data-stu-id="5df67-104">SYNTAX</span></span>

### <span data-ttu-id="5df67-105">NewByEditionAndComputeGenerationParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5df67-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5df67-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="5df67-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df67-107">說明</span><span class="sxs-lookup"><span data-stu-id="5df67-107">DESCRIPTION</span></span>
<span data-ttu-id="5df67-108">**新的-AzureRmSqlInstance** Cmdlet 會建立 Azure SQL Database Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="5df67-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="5df67-109">示例</span><span class="sxs-lookup"><span data-stu-id="5df67-109">EXAMPLES</span></span>

### <span data-ttu-id="5df67-110">範例1：建立新的實例</span><span class="sxs-lookup"><span data-stu-id="5df67-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="5df67-111">這個命令會使用 Edition 及 ComputeGeneration 參數建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="5df67-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="5df67-112">範例2：建立新的實例</span><span class="sxs-lookup"><span data-stu-id="5df67-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="5df67-113">這個命令會使用 Edition 與 ComputeGeneration 參數來建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="5df67-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="5df67-114">參數</span><span class="sxs-lookup"><span data-stu-id="5df67-114">PARAMETERS</span></span>

### <span data-ttu-id="5df67-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="5df67-115">-AdministratorCredential</span></span>
<span data-ttu-id="5df67-116">實例的 SQL 驗證認證。</span><span class="sxs-lookup"><span data-stu-id="5df67-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5df67-117">-AsJob</span></span>
<span data-ttu-id="5df67-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5df67-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5df67-119">-AssignIdentity</span></span>
<span data-ttu-id="5df67-120">針對此受管理的實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="5df67-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5df67-121">-ComputeGeneration</span></span>
<span data-ttu-id="5df67-122">該實例的計算產生。</span><span class="sxs-lookup"><span data-stu-id="5df67-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df67-123">-DefaultProfile</span></span>
<span data-ttu-id="5df67-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5df67-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="5df67-125">-Edition</span></span>
<span data-ttu-id="5df67-126">實例的版本。</span><span class="sxs-lookup"><span data-stu-id="5df67-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5df67-127">-LicenseType</span></span>
<span data-ttu-id="5df67-128">決定要使用哪一種類型的實例</span><span class="sxs-lookup"><span data-stu-id="5df67-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-129">-位置</span><span class="sxs-lookup"><span data-stu-id="5df67-129">-Location</span></span>
<span data-ttu-id="5df67-130">建立實例的位置</span><span class="sxs-lookup"><span data-stu-id="5df67-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="5df67-131">-Name</span></span>
<span data-ttu-id="5df67-132">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="5df67-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df67-133">-ResourceGroupName</span></span>
<span data-ttu-id="5df67-134">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5df67-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5df67-135">-SkuName</span></span>
<span data-ttu-id="5df67-136">實例的 SKU 名稱（例如 "GP_Gen4"，"BC_Gen4"）。</span><span class="sxs-lookup"><span data-stu-id="5df67-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="5df67-137">-StorageSizeInGB</span></span>
<span data-ttu-id="5df67-138">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="5df67-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5df67-139">-SubnetId</span></span>
<span data-ttu-id="5df67-140">要用於建立實例的子網識別碼</span><span class="sxs-lookup"><span data-stu-id="5df67-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="5df67-141">-Tag</span></span>
<span data-ttu-id="5df67-142">要與實例關聯的標記</span><span class="sxs-lookup"><span data-stu-id="5df67-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="5df67-143">-VCore</span></span>
<span data-ttu-id="5df67-144">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="5df67-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-145">-確認</span><span class="sxs-lookup"><span data-stu-id="5df67-145">-Confirm</span></span>
<span data-ttu-id="5df67-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5df67-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df67-147">-WhatIf</span></span>
<span data-ttu-id="5df67-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5df67-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5df67-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5df67-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5df67-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df67-150">CommonParameters</span></span>
<span data-ttu-id="5df67-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5df67-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df67-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5df67-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df67-153">輸入</span><span class="sxs-lookup"><span data-stu-id="5df67-153">INPUTS</span></span>

### <span data-ttu-id="5df67-154">所有</span><span class="sxs-lookup"><span data-stu-id="5df67-154">None</span></span>

## <span data-ttu-id="5df67-155">輸出</span><span class="sxs-lookup"><span data-stu-id="5df67-155">OUTPUTS</span></span>

### <span data-ttu-id="5df67-156">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="5df67-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="5df67-157">筆記</span><span class="sxs-lookup"><span data-stu-id="5df67-157">NOTES</span></span>

## <span data-ttu-id="5df67-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="5df67-158">RELATED LINKS</span></span>
