---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134502"
---
# <span data-ttu-id="ef3a5-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ef3a5-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ef3a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef3a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3a5-103">執行實例容錯移轉群組的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="ef3a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef3a5-104">SYNTAX</span></span>

### <span data-ttu-id="ef3a5-105">SwitchInstanceFailoverGroupDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ef3a5-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3a5-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef3a5-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef3a5-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef3a5-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3a5-108">說明</span><span class="sxs-lookup"><span data-stu-id="ef3a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ef3a5-109">這個命令會將範例容錯移轉群組中受管理實例的角色，移至指定的次要區域，使其成為新的主要區域。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="ef3a5-110">所有連到主要端點的新 TDS 會話，都會自動重新路由到新的主要區域。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="ef3a5-111">示例</span><span class="sxs-lookup"><span data-stu-id="ef3a5-111">EXAMPLES</span></span>

### <span data-ttu-id="ef3a5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ef3a5-112">Example 1</span></span>
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

<span data-ttu-id="ef3a5-113">在實例容錯移轉群組中，以管道方式發出容錯移轉作業，以使資料遺失。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="ef3a5-114">範例2</span><span class="sxs-lookup"><span data-stu-id="ef3a5-114">Example 2</span></span>
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

<span data-ttu-id="ef3a5-115">在不遺失資料或失敗與回滾的情況下，發出最佳的成功容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="ef3a5-116">參數</span><span class="sxs-lookup"><span data-stu-id="ef3a5-116">PARAMETERS</span></span>

### <span data-ttu-id="ef3a5-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="ef3a5-117">-AllowDataLoss</span></span>
<span data-ttu-id="ef3a5-118">完成容錯移轉，即使這樣做可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="ef3a5-119">這可讓容錯移轉即使在主要資料庫無法使用時仍能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="ef3a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3a5-120">-DefaultProfile</span></span>
<span data-ttu-id="ef3a5-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef3a5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef3a5-122">-InputObject</span></span>
<span data-ttu-id="ef3a5-123">要切換的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="ef3a5-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="ef3a5-124">-位置</span><span class="sxs-lookup"><span data-stu-id="ef3a5-124">-Location</span></span>
<span data-ttu-id="ef3a5-125">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ef3a5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef3a5-126">-Name</span></span>
<span data-ttu-id="ef3a5-127">實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ef3a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef3a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="ef3a5-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef3a5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef3a5-130">-ResourceId</span></span>
<span data-ttu-id="ef3a5-131">要切換之實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="ef3a5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ef3a5-132">-Confirm</span></span>
<span data-ttu-id="ef3a5-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3a5-134">-WhatIf</span></span>
<span data-ttu-id="ef3a5-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef3a5-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef3a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3a5-137">CommonParameters</span></span>
<span data-ttu-id="ef3a5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3a5-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef3a5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3a5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ef3a5-140">INPUTS</span></span>

### <span data-ttu-id="ef3a5-141">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="ef3a5-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="ef3a5-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ef3a5-142">System.String</span></span>

## <span data-ttu-id="ef3a5-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ef3a5-143">OUTPUTS</span></span>

### <span data-ttu-id="ef3a5-144">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="ef3a5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ef3a5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ef3a5-145">NOTES</span></span>

## <span data-ttu-id="ef3a5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef3a5-146">RELATED LINKS</span></span>
