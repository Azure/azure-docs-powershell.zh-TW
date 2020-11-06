---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451012"
---
# <span data-ttu-id="46d86-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46d86-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="46d86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46d86-102">SYNOPSIS</span></span>
<span data-ttu-id="46d86-103">傳回有關 Azure SQL Managed 資料庫實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="46d86-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46d86-104">句法</span><span class="sxs-lookup"><span data-stu-id="46d86-104">SYNTAX</span></span>

### <span data-ttu-id="46d86-105">GetInstanceByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="46d86-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46d86-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46d86-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d86-107">說明</span><span class="sxs-lookup"><span data-stu-id="46d86-107">DESCRIPTION</span></span>
<span data-ttu-id="46d86-108">**AzureRmSqlInstance** Cmdlet 會傳回一或多個 Azure SQL 管理實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46d86-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="46d86-109">指定實例的名稱，只查看該實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="46d86-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="46d86-110">示例</span><span class="sxs-lookup"><span data-stu-id="46d86-110">EXAMPLES</span></span>

### <span data-ttu-id="46d86-111">範例1：取得指派給資源群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="46d86-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="46d86-112">這個命令會取得指派給資源群組 ResourceGroup01 的所有實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46d86-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="46d86-113">範例2：取得實例的相關資訊</span><span class="sxs-lookup"><span data-stu-id="46d86-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="46d86-114">這個命令會取得名為 managedInstance1 之實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46d86-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="46d86-115">參數</span><span class="sxs-lookup"><span data-stu-id="46d86-115">PARAMETERS</span></span>

### <span data-ttu-id="46d86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d86-116">-DefaultProfile</span></span>
<span data-ttu-id="46d86-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46d86-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d86-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="46d86-118">-Name</span></span>
<span data-ttu-id="46d86-119">SQL 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="46d86-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d86-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d86-120">-ResourceGroupName</span></span>
<span data-ttu-id="46d86-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46d86-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d86-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d86-122">CommonParameters</span></span>
<span data-ttu-id="46d86-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46d86-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d86-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46d86-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d86-125">輸入</span><span class="sxs-lookup"><span data-stu-id="46d86-125">INPUTS</span></span>

### <span data-ttu-id="46d86-126">所有</span><span class="sxs-lookup"><span data-stu-id="46d86-126">None</span></span>

## <span data-ttu-id="46d86-127">輸出</span><span class="sxs-lookup"><span data-stu-id="46d86-127">OUTPUTS</span></span>

### <span data-ttu-id="46d86-128">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="46d86-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="46d86-129">筆記</span><span class="sxs-lookup"><span data-stu-id="46d86-129">NOTES</span></span>

## <span data-ttu-id="46d86-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="46d86-130">RELATED LINKS</span></span>
