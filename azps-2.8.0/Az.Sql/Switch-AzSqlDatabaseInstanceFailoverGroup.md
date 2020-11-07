---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792871"
---
# <span data-ttu-id="b2794-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b2794-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="b2794-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2794-102">SYNOPSIS</span></span>
<span data-ttu-id="b2794-103">執行實例容錯移轉群組的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b2794-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="b2794-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2794-104">SYNTAX</span></span>

### <span data-ttu-id="b2794-105">SwitchIFGDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="b2794-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2794-106">從資源識別碼切換實例容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="b2794-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2794-107">從 AzureSqlInstanceFailoverGroupModel 實例定義切換實例容錯移轉群組</span><span class="sxs-lookup"><span data-stu-id="b2794-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2794-108">說明</span><span class="sxs-lookup"><span data-stu-id="b2794-108">DESCRIPTION</span></span>
<span data-ttu-id="b2794-109">這個命令會將範例容錯移轉群組中受管理實例的角色，移至指定的次要區域，使其成為新的主要區域。</span><span class="sxs-lookup"><span data-stu-id="b2794-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="b2794-110">所有連到主要端點的新 TDS 會話，都會自動重新路由到新的主要區域。</span><span class="sxs-lookup"><span data-stu-id="b2794-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="b2794-111">示例</span><span class="sxs-lookup"><span data-stu-id="b2794-111">EXAMPLES</span></span>

### <span data-ttu-id="b2794-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b2794-112">Example 1</span></span>
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

<span data-ttu-id="b2794-113">在實例容錯移轉群組中，以管道方式發出容錯移轉作業，以使資料遺失。</span><span class="sxs-lookup"><span data-stu-id="b2794-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="b2794-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b2794-114">Example 2</span></span>
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

<span data-ttu-id="b2794-115">在不遺失資料或失敗與回滾的情況下，發出最佳的成功容錯移轉作業。</span><span class="sxs-lookup"><span data-stu-id="b2794-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="b2794-116">參數</span><span class="sxs-lookup"><span data-stu-id="b2794-116">PARAMETERS</span></span>

### <span data-ttu-id="b2794-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="b2794-117">-AllowDataLoss</span></span>
<span data-ttu-id="b2794-118">完成容錯移轉，即使這樣做可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="b2794-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="b2794-119">這可讓容錯移轉即使在主要資料庫無法使用時仍能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="b2794-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="b2794-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2794-120">-DefaultProfile</span></span>
<span data-ttu-id="b2794-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2794-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2794-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2794-122">-InputObject</span></span>
<span data-ttu-id="b2794-123">要切換的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="b2794-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2794-124">-位置</span><span class="sxs-lookup"><span data-stu-id="b2794-124">-Location</span></span>
<span data-ttu-id="b2794-125">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="b2794-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2794-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2794-126">-Name</span></span>
<span data-ttu-id="b2794-127">實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2794-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2794-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2794-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2794-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2794-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2794-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2794-130">-ResourceId</span></span>
<span data-ttu-id="b2794-131">要切換之實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2794-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2794-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b2794-132">-Confirm</span></span>
<span data-ttu-id="b2794-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2794-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2794-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2794-134">-WhatIf</span></span>
<span data-ttu-id="b2794-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2794-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2794-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2794-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2794-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2794-137">CommonParameters</span></span>
<span data-ttu-id="b2794-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2794-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2794-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b2794-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2794-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b2794-140">INPUTS</span></span>

### <span data-ttu-id="b2794-141">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="b2794-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="b2794-142">System.object</span><span class="sxs-lookup"><span data-stu-id="b2794-142">System.String</span></span>

## <span data-ttu-id="b2794-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b2794-143">OUTPUTS</span></span>

### <span data-ttu-id="b2794-144">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="b2794-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="b2794-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b2794-145">NOTES</span></span>

## <span data-ttu-id="b2794-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2794-146">RELATED LINKS</span></span>
