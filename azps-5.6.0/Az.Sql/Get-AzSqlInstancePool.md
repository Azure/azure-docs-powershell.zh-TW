---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 524d9ff479355f511b9039e1ea64a8234e37e021
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914285"
---
# <span data-ttu-id="27441-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="27441-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="27441-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27441-102">SYNOPSIS</span></span>
<span data-ttu-id="27441-103">會返回 Azure SQL 實例資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="27441-104">語法</span><span class="sxs-lookup"><span data-stu-id="27441-104">SYNTAX</span></span>

### <span data-ttu-id="27441-105">ListBySubOrResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="27441-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27441-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="27441-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27441-107">GetInstancePoolByStancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="27441-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27441-108">描述</span><span class="sxs-lookup"><span data-stu-id="27441-108">DESCRIPTION</span></span>
<span data-ttu-id="27441-109">**Get-AzSqlInstancePool** Cmdlet 會傳回一或多個 Azure SQL 實例資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="27441-110">指定實例資料庫的名稱，只查看該實例資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="27441-111">例子</span><span class="sxs-lookup"><span data-stu-id="27441-111">EXAMPLES</span></span>

### <span data-ttu-id="27441-112">範例 1：跨客戶訂閱取得所有實例資料庫</span><span class="sxs-lookup"><span data-stu-id="27441-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="27441-113">此命令會獲得客戶訂閱內所有實例資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="27441-114">範例 2：跨資源群組取得所有實例資料庫</span><span class="sxs-lookup"><span data-stu-id="27441-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="27441-115">此命令會獲得資源群組資源群組01 內所有實例資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="27441-116">範例 3：取得實例資料庫相關資訊</span><span class="sxs-lookup"><span data-stu-id="27441-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="27441-117">此命令會獲得實例資料庫實例Pool0 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="27441-118">範例 4：使用實例資料庫資源識別碼取得實例資料庫相關資訊</span><span class="sxs-lookup"><span data-stu-id="27441-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="27441-119">此命令會包含其資源識別碼的實例資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="27441-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="27441-120">參數</span><span class="sxs-lookup"><span data-stu-id="27441-120">PARAMETERS</span></span>

### <span data-ttu-id="27441-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27441-121">-DefaultProfile</span></span>
<span data-ttu-id="27441-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27441-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27441-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="27441-123">-Name</span></span>
<span data-ttu-id="27441-124">實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="27441-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27441-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27441-125">-ResourceGroupName</span></span>
<span data-ttu-id="27441-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="27441-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27441-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27441-127">-ResourceId</span></span>
<span data-ttu-id="27441-128">實例資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="27441-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27441-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27441-129">CommonParameters</span></span>
<span data-ttu-id="27441-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27441-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27441-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27441-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27441-132">輸入</span><span class="sxs-lookup"><span data-stu-id="27441-132">INPUTS</span></span>

### <span data-ttu-id="27441-133">沒有</span><span class="sxs-lookup"><span data-stu-id="27441-133">None</span></span>

## <span data-ttu-id="27441-134">輸出</span><span class="sxs-lookup"><span data-stu-id="27441-134">OUTPUTS</span></span>

### <span data-ttu-id="27441-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="27441-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="27441-136">筆記</span><span class="sxs-lookup"><span data-stu-id="27441-136">NOTES</span></span>

## <span data-ttu-id="27441-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="27441-137">RELATED LINKS</span></span>
