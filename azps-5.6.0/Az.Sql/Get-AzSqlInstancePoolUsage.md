---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: 07a7e8c656fb028b9db813201ac2628da294209b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906857"
---
# <span data-ttu-id="9aeb4-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="9aeb4-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="9aeb4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9aeb4-102">SYNOPSIS</span></span>
<span data-ttu-id="9aeb4-103">會返回 Azure SQL 實例資料庫使用方式相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="9aeb4-104">語法</span><span class="sxs-lookup"><span data-stu-id="9aeb4-104">SYNTAX</span></span>

### <span data-ttu-id="9aeb4-105">InstancePoolUsageDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9aeb4-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aeb4-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aeb4-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aeb4-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aeb4-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aeb4-108">描述</span><span class="sxs-lookup"><span data-stu-id="9aeb4-108">DESCRIPTION</span></span>
<span data-ttu-id="9aeb4-109">**Get-AzSqlInstancePoolUsage Cmdlet** 會傳回 Azure SQL 實例資料庫使用方式的資訊。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="9aeb4-110">例子</span><span class="sxs-lookup"><span data-stu-id="9aeb4-110">EXAMPLES</span></span>

### <span data-ttu-id="9aeb4-111">範例 1：使用 Azure SQL 實例資料庫</span><span class="sxs-lookup"><span data-stu-id="9aeb4-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="9aeb4-112">獲得 Azure SQL 實例資料庫實例幕後處理0 的使用量。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="9aeb4-113">範例 2：使用實例資料庫物件來使用 Azure SQL Instance 資料庫</span><span class="sxs-lookup"><span data-stu-id="9aeb4-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="9aeb4-114">使用實例資料庫物件來使用 Azure SQL 實例資料庫實例幕後處理0 的使用量。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="9aeb4-115">範例 3：使用實例資料庫資源識別碼來使用 Azure SQL 實例資料庫</span><span class="sxs-lookup"><span data-stu-id="9aeb4-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="9aeb4-116">使用實例資料庫資源識別碼，獲得 Azure SQL 實例資料庫實例幕後處理0 的使用狀況。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="9aeb4-117">範例 3：使用 Azure SQL 實例資料庫的使用方式，以及該資料庫中受管理實例使用量的明細。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="9aeb4-118">獲得 Azure SQL 實例資料庫實例幕後處理0 的使用狀況，以及實例多工緩衝處理程式0 中受管理實例的使用狀況。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="9aeb4-119">參數</span><span class="sxs-lookup"><span data-stu-id="9aeb4-119">PARAMETERS</span></span>

### <span data-ttu-id="9aeb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aeb4-120">-DefaultProfile</span></span>
<span data-ttu-id="9aeb4-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aeb4-122">-Expand以</span><span class="sxs-lookup"><span data-stu-id="9aeb4-122">-ExpandChildren</span></span>
<span data-ttu-id="9aeb4-123">指出是否要將此實例資料庫的使用量及其子女使用量展開的旗標。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="9aeb4-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="9aeb4-124">-InstancePool</span></span>
<span data-ttu-id="9aeb4-125">父實例資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aeb4-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9aeb4-126">-Name</span></span>
<span data-ttu-id="9aeb4-127">受管理的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aeb4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aeb4-128">-ResourceGroupName</span></span>
<span data-ttu-id="9aeb4-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aeb4-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aeb4-130">-ResourceId</span></span>
<span data-ttu-id="9aeb4-131">父資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aeb4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aeb4-132">CommonParameters</span></span>
<span data-ttu-id="9aeb4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9aeb4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aeb4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9aeb4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aeb4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9aeb4-135">INPUTS</span></span>

### <span data-ttu-id="9aeb4-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="9aeb4-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="9aeb4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9aeb4-137">System.String</span></span>

## <span data-ttu-id="9aeb4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9aeb4-138">OUTPUTS</span></span>

### <span data-ttu-id="9aeb4-139">Microsoft.Azure.Commands.sql.usages.models.AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="9aeb4-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="9aeb4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9aeb4-140">NOTES</span></span>

## <span data-ttu-id="9aeb4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9aeb4-141">RELATED LINKS</span></span>
