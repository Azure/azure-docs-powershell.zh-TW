---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: a20f2196b6052befb74cd74366c96bf262cdd325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912277"
---
# <span data-ttu-id="45a84-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="45a84-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="45a84-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45a84-102">SYNOPSIS</span></span>
<span data-ttu-id="45a84-103">執行實例容錯移轉群組的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="45a84-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="45a84-104">語法</span><span class="sxs-lookup"><span data-stu-id="45a84-104">SYNTAX</span></span>

### <span data-ttu-id="45a84-105">SwitchInstanceFailoverGroupDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="45a84-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45a84-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="45a84-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45a84-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45a84-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45a84-108">描述</span><span class="sxs-lookup"><span data-stu-id="45a84-108">DESCRIPTION</span></span>
<span data-ttu-id="45a84-109">此命令會容錯移轉到指定的次要區域，以交換實例容錯移轉群組中受管理實例的角色，使其成為新的主要區域。</span><span class="sxs-lookup"><span data-stu-id="45a84-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="45a84-110">所有連接到主要端點的新 TDS 會話都會自動重新路由至新的主要區域。</span><span class="sxs-lookup"><span data-stu-id="45a84-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="45a84-111">例子</span><span class="sxs-lookup"><span data-stu-id="45a84-111">EXAMPLES</span></span>

### <span data-ttu-id="45a84-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="45a84-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="45a84-113">在實例容錯移轉群組中發行允許資料遺失的容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="45a84-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="45a84-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="45a84-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="45a84-115">發出最佳嘗試容錯移轉作業，該作業可能會成功而不會失去資料，或失敗並回復。</span><span class="sxs-lookup"><span data-stu-id="45a84-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="45a84-116">參數</span><span class="sxs-lookup"><span data-stu-id="45a84-116">PARAMETERS</span></span>

### <span data-ttu-id="45a84-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="45a84-117">-AllowDataLoss</span></span>
<span data-ttu-id="45a84-118">即使執行此操作可能會導致資料遺失，也請完成容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="45a84-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="45a84-119">這樣即使主資料庫無法使用，也允許容錯移轉繼續進行。</span><span class="sxs-lookup"><span data-stu-id="45a84-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="45a84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a84-120">-DefaultProfile</span></span>
<span data-ttu-id="45a84-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45a84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45a84-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45a84-122">-InputObject</span></span>
<span data-ttu-id="45a84-123">要切換的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="45a84-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45a84-124">-位置</span><span class="sxs-lookup"><span data-stu-id="45a84-124">-Location</span></span>
<span data-ttu-id="45a84-125">要從其中取回實例容錯移轉群組的當地地區名稱。</span><span class="sxs-lookup"><span data-stu-id="45a84-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a84-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="45a84-126">-Name</span></span>
<span data-ttu-id="45a84-127">實例容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45a84-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a84-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a84-128">-ResourceGroupName</span></span>
<span data-ttu-id="45a84-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45a84-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a84-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45a84-130">-ResourceId</span></span>
<span data-ttu-id="45a84-131">要切換的實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="45a84-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45a84-132">-確認</span><span class="sxs-lookup"><span data-stu-id="45a84-132">-Confirm</span></span>
<span data-ttu-id="45a84-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="45a84-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a84-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a84-134">-WhatIf</span></span>
<span data-ttu-id="45a84-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45a84-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45a84-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45a84-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a84-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a84-137">CommonParameters</span></span>
<span data-ttu-id="45a84-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45a84-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a84-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45a84-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a84-140">輸入</span><span class="sxs-lookup"><span data-stu-id="45a84-140">INPUTS</span></span>

### <span data-ttu-id="45a84-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="45a84-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="45a84-142">System.String</span><span class="sxs-lookup"><span data-stu-id="45a84-142">System.String</span></span>

## <span data-ttu-id="45a84-143">輸出</span><span class="sxs-lookup"><span data-stu-id="45a84-143">OUTPUTS</span></span>

### <span data-ttu-id="45a84-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="45a84-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="45a84-145">筆記</span><span class="sxs-lookup"><span data-stu-id="45a84-145">NOTES</span></span>

## <span data-ttu-id="45a84-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="45a84-146">RELATED LINKS</span></span>
