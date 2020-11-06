---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453603"
---
# <span data-ttu-id="168ea-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="168ea-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="168ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="168ea-102">SYNOPSIS</span></span>
<span data-ttu-id="168ea-103">設定 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="168ea-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="168ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="168ea-104">SYNTAX</span></span>

### <span data-ttu-id="168ea-105">SetInstanceFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="168ea-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="168ea-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="168ea-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="168ea-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="168ea-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="168ea-108">說明</span><span class="sxs-lookup"><span data-stu-id="168ea-108">DESCRIPTION</span></span>
<span data-ttu-id="168ea-109">**AzureRmSqlInstance** Cmdlet 會修改 Azure SQL Database Managed 實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="168ea-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="168ea-110">示例</span><span class="sxs-lookup"><span data-stu-id="168ea-110">EXAMPLES</span></span>

### <span data-ttu-id="168ea-111">範例1：使用新的值（AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore）來設定現有實例</span><span class="sxs-lookup"><span data-stu-id="168ea-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="168ea-112">這個命令會使用 AdministratorPassword、-LicenseType、-StorageSizeInGB 和-VCore 的新值來設定現有實例。</span><span class="sxs-lookup"><span data-stu-id="168ea-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="168ea-113">參數</span><span class="sxs-lookup"><span data-stu-id="168ea-113">PARAMETERS</span></span>

### <span data-ttu-id="168ea-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="168ea-114">-AdministratorPassword</span></span>
<span data-ttu-id="168ea-115">該實例的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="168ea-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="168ea-116">-AssignIdentity</span></span>
<span data-ttu-id="168ea-117">針對此實例產生並指派 Azure Active Directory 身分識別，以搭配 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="168ea-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="168ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168ea-118">-DefaultProfile</span></span>
<span data-ttu-id="168ea-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="168ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="168ea-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="168ea-120">-Edition</span></span>
<span data-ttu-id="168ea-121">要指派給實例的版本。</span><span class="sxs-lookup"><span data-stu-id="168ea-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-122">-Force</span><span class="sxs-lookup"><span data-stu-id="168ea-122">-Force</span></span>
<span data-ttu-id="168ea-123">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="168ea-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="168ea-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="168ea-124">-InputObject</span></span>
<span data-ttu-id="168ea-125">要移除的 AzureSqlManagedInstanceModel 物件</span><span class="sxs-lookup"><span data-stu-id="168ea-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="168ea-126">-LicenseType</span></span>
<span data-ttu-id="168ea-127">決定要使用哪一種類型的實例</span><span class="sxs-lookup"><span data-stu-id="168ea-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="168ea-128">-Name</span></span>
<span data-ttu-id="168ea-129">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="168ea-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168ea-130">-ResourceGroupName</span></span>
<span data-ttu-id="168ea-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="168ea-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="168ea-132">-ResourceId</span></span>
<span data-ttu-id="168ea-133">要移除之實例的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="168ea-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="168ea-134">-StorageSizeInGB</span></span>
<span data-ttu-id="168ea-135">決定要與實例建立多少儲存空間大小</span><span class="sxs-lookup"><span data-stu-id="168ea-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="168ea-136">-Tag</span></span>
<span data-ttu-id="168ea-137">要與實例建立關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="168ea-137">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="168ea-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="168ea-138">-VCore</span></span>
<span data-ttu-id="168ea-139">決定要與實例相關聯的 VCore 數量</span><span class="sxs-lookup"><span data-stu-id="168ea-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="168ea-140">-確認</span><span class="sxs-lookup"><span data-stu-id="168ea-140">-Confirm</span></span>
<span data-ttu-id="168ea-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="168ea-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="168ea-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="168ea-142">-WhatIf</span></span>
<span data-ttu-id="168ea-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="168ea-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="168ea-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="168ea-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="168ea-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168ea-145">CommonParameters</span></span>
<span data-ttu-id="168ea-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="168ea-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168ea-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="168ea-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168ea-148">輸入</span><span class="sxs-lookup"><span data-stu-id="168ea-148">INPUTS</span></span>

### <span data-ttu-id="168ea-149">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="168ea-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="168ea-150">System.object</span><span class="sxs-lookup"><span data-stu-id="168ea-150">System.String</span></span>

## <span data-ttu-id="168ea-151">輸出</span><span class="sxs-lookup"><span data-stu-id="168ea-151">OUTPUTS</span></span>

### <span data-ttu-id="168ea-152">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="168ea-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="168ea-153">筆記</span><span class="sxs-lookup"><span data-stu-id="168ea-153">NOTES</span></span>

## <span data-ttu-id="168ea-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="168ea-154">RELATED LINKS</span></span>
