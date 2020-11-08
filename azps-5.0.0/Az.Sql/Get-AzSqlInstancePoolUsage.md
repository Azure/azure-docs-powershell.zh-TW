---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138433"
---
# <span data-ttu-id="732fb-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="732fb-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="732fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="732fb-102">SYNOPSIS</span></span>
<span data-ttu-id="732fb-103">傳回有關 Azure SQL 實例池用法的資訊。</span><span class="sxs-lookup"><span data-stu-id="732fb-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="732fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="732fb-104">SYNTAX</span></span>

### <span data-ttu-id="732fb-105">InstancePoolUsageDefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="732fb-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732fb-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="732fb-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="732fb-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="732fb-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="732fb-108">說明</span><span class="sxs-lookup"><span data-stu-id="732fb-108">DESCRIPTION</span></span>
<span data-ttu-id="732fb-109">**AzSqlInstancePoolUsage** Cmdlet 會傳回有關 Azure SQL 實例池用法的資訊。</span><span class="sxs-lookup"><span data-stu-id="732fb-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="732fb-110">示例</span><span class="sxs-lookup"><span data-stu-id="732fb-110">EXAMPLES</span></span>

### <span data-ttu-id="732fb-111">範例1：取得 Azure SQL 實例池的使用方式</span><span class="sxs-lookup"><span data-stu-id="732fb-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
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

<span data-ttu-id="732fb-112">取得 Azure SQL 實例池 instancepool0 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="732fb-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="732fb-113">範例2：使用實例池物件取得 Azure SQL 實例池的使用方式</span><span class="sxs-lookup"><span data-stu-id="732fb-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
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

<span data-ttu-id="732fb-114">使用實例池物件取得 Azure SQL 實例池 instancepool0 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="732fb-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="732fb-115">範例3：使用實例池資源識別碼取得 Azure SQL 實例池的使用方式</span><span class="sxs-lookup"><span data-stu-id="732fb-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
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

<span data-ttu-id="732fb-116">使用實例池資源識別碼取得 Azure SQL 實例池 instancepool0 的使用方式。</span><span class="sxs-lookup"><span data-stu-id="732fb-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="732fb-117">範例3：取得對池中的受管理實例使用方式進行細目分類的 Azure SQL 實例池的使用方式。</span><span class="sxs-lookup"><span data-stu-id="732fb-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
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

<span data-ttu-id="732fb-118">取得 Azure SQL 實例池 instancepool0 的用法，以及 instancepool0 中受管理實例的使用方式。</span><span class="sxs-lookup"><span data-stu-id="732fb-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="732fb-119">參數</span><span class="sxs-lookup"><span data-stu-id="732fb-119">PARAMETERS</span></span>

### <span data-ttu-id="732fb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732fb-120">-DefaultProfile</span></span>
<span data-ttu-id="732fb-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="732fb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732fb-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="732fb-122">-ExpandChildren</span></span>
<span data-ttu-id="732fb-123">此標記指出是否要將這個實例池的使用方式與其孩子的使用方式展開。</span><span class="sxs-lookup"><span data-stu-id="732fb-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="732fb-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="732fb-124">-InstancePool</span></span>
<span data-ttu-id="732fb-125">父實例池物件。</span><span class="sxs-lookup"><span data-stu-id="732fb-125">The parent instance pool object.</span></span>

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

### <span data-ttu-id="732fb-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="732fb-126">-Name</span></span>
<span data-ttu-id="732fb-127">受管理的實例池名稱。</span><span class="sxs-lookup"><span data-stu-id="732fb-127">The managed instance pool name.</span></span>

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

### <span data-ttu-id="732fb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="732fb-128">-ResourceGroupName</span></span>
<span data-ttu-id="732fb-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="732fb-129">The resource group name.</span></span>

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

### <span data-ttu-id="732fb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="732fb-130">-ResourceId</span></span>
<span data-ttu-id="732fb-131">[父資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="732fb-131">The parent resource id.</span></span>

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

### <span data-ttu-id="732fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732fb-132">CommonParameters</span></span>
<span data-ttu-id="732fb-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="732fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732fb-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="732fb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732fb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="732fb-135">INPUTS</span></span>

### <span data-ttu-id="732fb-136">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="732fb-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="732fb-137">System.object</span><span class="sxs-lookup"><span data-stu-id="732fb-137">System.String</span></span>

## <span data-ttu-id="732fb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="732fb-138">OUTPUTS</span></span>

### <span data-ttu-id="732fb-139">AzureSqlUsageModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="732fb-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="732fb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="732fb-140">NOTES</span></span>

## <span data-ttu-id="732fb-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="732fb-141">RELATED LINKS</span></span>
