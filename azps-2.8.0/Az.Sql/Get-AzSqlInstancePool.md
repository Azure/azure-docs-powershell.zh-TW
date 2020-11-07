---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 8d2d1333a10290c3a321b22cf33b527738d7ecb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792490"
---
# <span data-ttu-id="58a8d-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="58a8d-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="58a8d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="58a8d-103">傳回有關 Azure SQL 實例池的資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="58a8d-104">句法</span><span class="sxs-lookup"><span data-stu-id="58a8d-104">SYNTAX</span></span>

### <span data-ttu-id="58a8d-105">ListBySubOrResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58a8d-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58a8d-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a8d-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58a8d-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a8d-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58a8d-108">說明</span><span class="sxs-lookup"><span data-stu-id="58a8d-108">DESCRIPTION</span></span>
<span data-ttu-id="58a8d-109">**AzSqlInstancePool** Cmdlet 會傳回一或多個 Azure SQL 實例池的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="58a8d-110">指定實例池的名稱，只查看該實例池的資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="58a8d-111">示例</span><span class="sxs-lookup"><span data-stu-id="58a8d-111">EXAMPLES</span></span>

### <span data-ttu-id="58a8d-112">範例1：取得整個客戶訂閱的所有實例池</span><span class="sxs-lookup"><span data-stu-id="58a8d-112">Example 1: Get all instance pools across a customer subscription</span></span>
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

<span data-ttu-id="58a8d-113">這個命令會取得客戶訂閱中所有實例池的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="58a8d-114">範例2：取得整個資源群組的所有實例池</span><span class="sxs-lookup"><span data-stu-id="58a8d-114">Example 2: Get all instance pools across a resource group</span></span>
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

<span data-ttu-id="58a8d-115">這個命令會取得 [資源群組 resourcegroup01] 中所有實例池的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="58a8d-116">範例3：取得實例池的相關資訊</span><span class="sxs-lookup"><span data-stu-id="58a8d-116">Example 3: Get information about an instance pool</span></span>
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

<span data-ttu-id="58a8d-117">這個命令會取得實例池 instancePool0 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="58a8d-118">範例4：使用實例池資源識別碼取得實例池的相關資訊</span><span class="sxs-lookup"><span data-stu-id="58a8d-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
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

<span data-ttu-id="58a8d-119">這個命令會取得實例池及其資源識別碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="58a8d-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="58a8d-120">參數</span><span class="sxs-lookup"><span data-stu-id="58a8d-120">PARAMETERS</span></span>

### <span data-ttu-id="58a8d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a8d-121">-DefaultProfile</span></span>
<span data-ttu-id="58a8d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58a8d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a8d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="58a8d-123">-Name</span></span>
<span data-ttu-id="58a8d-124">實例池名稱。</span><span class="sxs-lookup"><span data-stu-id="58a8d-124">The instance pool name.</span></span>

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

### <span data-ttu-id="58a8d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a8d-125">-ResourceGroupName</span></span>
<span data-ttu-id="58a8d-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58a8d-126">The resource group name.</span></span>

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

### <span data-ttu-id="58a8d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a8d-127">-ResourceId</span></span>
<span data-ttu-id="58a8d-128">實例池資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="58a8d-128">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="58a8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a8d-129">CommonParameters</span></span>
<span data-ttu-id="58a8d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58a8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a8d-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58a8d-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a8d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="58a8d-132">INPUTS</span></span>

### <span data-ttu-id="58a8d-133">所有</span><span class="sxs-lookup"><span data-stu-id="58a8d-133">None</span></span>

## <span data-ttu-id="58a8d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="58a8d-134">OUTPUTS</span></span>

### <span data-ttu-id="58a8d-135">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="58a8d-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="58a8d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="58a8d-136">NOTES</span></span>

## <span data-ttu-id="58a8d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="58a8d-137">RELATED LINKS</span></span>
