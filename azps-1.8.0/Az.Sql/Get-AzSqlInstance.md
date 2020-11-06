---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620425"
---
# <span data-ttu-id="56a1b-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="56a1b-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="56a1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="56a1b-103">傳回有關 Azure SQL Managed 資料庫實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="56a1b-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="56a1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="56a1b-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56a1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="56a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="56a1b-106">**AzSqlInstance** Cmdlet 會傳回一或多個 Azure SQL 管理實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56a1b-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="56a1b-107">指定實例的名稱，只查看該實例的資訊。</span><span class="sxs-lookup"><span data-stu-id="56a1b-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="56a1b-108">示例</span><span class="sxs-lookup"><span data-stu-id="56a1b-108">EXAMPLES</span></span>

### <span data-ttu-id="56a1b-109">範例1：取得指派給資源群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="56a1b-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="56a1b-110">這個命令會取得指派給資源群組 ResourceGroup01 的所有實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56a1b-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="56a1b-111">範例2：取得實例的相關資訊</span><span class="sxs-lookup"><span data-stu-id="56a1b-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="56a1b-112">這個命令會取得名為 managedInstance1 之實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56a1b-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="56a1b-113">範例3：使用篩選來取得指派給資源群組的所有實例</span><span class="sxs-lookup"><span data-stu-id="56a1b-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
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

<span data-ttu-id="56a1b-114">這個命令會取得指派給以「managedInstance」開頭之資源群組 ResourceGroup01 之所有實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="56a1b-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="56a1b-115">參數</span><span class="sxs-lookup"><span data-stu-id="56a1b-115">PARAMETERS</span></span>

### <span data-ttu-id="56a1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a1b-116">-DefaultProfile</span></span>
<span data-ttu-id="56a1b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56a1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56a1b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="56a1b-118">-Name</span></span>
<span data-ttu-id="56a1b-119">SQL 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="56a1b-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="56a1b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a1b-120">-ResourceGroupName</span></span>
<span data-ttu-id="56a1b-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56a1b-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="56a1b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a1b-122">CommonParameters</span></span>
<span data-ttu-id="56a1b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56a1b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a1b-124">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56a1b-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a1b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="56a1b-125">INPUTS</span></span>

### <span data-ttu-id="56a1b-126">所有</span><span class="sxs-lookup"><span data-stu-id="56a1b-126">None</span></span>

## <span data-ttu-id="56a1b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="56a1b-127">OUTPUTS</span></span>

### <span data-ttu-id="56a1b-128">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="56a1b-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="56a1b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="56a1b-129">NOTES</span></span>

## <span data-ttu-id="56a1b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="56a1b-130">RELATED LINKS</span></span>
