---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 3031878e30307cd5ff733de6177bc3c65c61a5bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905754"
---
# <span data-ttu-id="f729b-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f729b-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="f729b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f729b-102">SYNOPSIS</span></span>
<span data-ttu-id="f729b-103">修改實例容錯移轉群組的群組原則。</span><span class="sxs-lookup"><span data-stu-id="f729b-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="f729b-104">語法</span><span class="sxs-lookup"><span data-stu-id="f729b-104">SYNTAX</span></span>

### <span data-ttu-id="f729b-105">SetInstanceFailoverGroupDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f729b-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f729b-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f729b-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f729b-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="f729b-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f729b-108">描述</span><span class="sxs-lookup"><span data-stu-id="f729b-108">DESCRIPTION</span></span>
<span data-ttu-id="f729b-109">此命令會修改實例容錯移轉群組的群組原則。</span><span class="sxs-lookup"><span data-stu-id="f729b-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="f729b-110">實例容錯移轉群組的主要區域應該用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="f729b-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="f729b-111">在實例容錯移轉群組功能預覽期間，'-GracePeriodWithDataLossHours'參數僅支援大於或等於 1 小時的值。</span><span class="sxs-lookup"><span data-stu-id="f729b-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f729b-112">例子</span><span class="sxs-lookup"><span data-stu-id="f729b-112">EXAMPLES</span></span>

### <span data-ttu-id="f729b-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f729b-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="f729b-114">在容錯移轉群組中設定點子，將實例容錯移轉群組的容錯移轉策略設定為'手動'。</span><span class="sxs-lookup"><span data-stu-id="f729b-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="f729b-115">參數</span><span class="sxs-lookup"><span data-stu-id="f729b-115">PARAMETERS</span></span>

### <span data-ttu-id="f729b-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f729b-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f729b-117">次要伺服器的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="f729b-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f729b-118">-DefaultProfile</span></span>
<span data-ttu-id="f729b-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f729b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f729b-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f729b-120">-FailoverPolicy</span></span>
<span data-ttu-id="f729b-121">實例容錯移轉群組的容錯移轉策略。</span><span class="sxs-lookup"><span data-stu-id="f729b-121">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f729b-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f729b-123">如果主伺服器上發生中斷，且無法在不遺失資料的情況下完成容錯移轉，則自動容錯移轉啟動前的間隔。</span><span class="sxs-lookup"><span data-stu-id="f729b-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f729b-124">-InputObject</span></span>
<span data-ttu-id="f729b-125">要設定的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="f729b-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-126">-位置</span><span class="sxs-lookup"><span data-stu-id="f729b-126">-Location</span></span>
<span data-ttu-id="f729b-127">要從其中取回實例容錯移轉群組的當地地區名稱。</span><span class="sxs-lookup"><span data-stu-id="f729b-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f729b-128">-Name</span></span>
<span data-ttu-id="f729b-129">實例容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f729b-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f729b-130">-ResourceGroupName</span></span>
<span data-ttu-id="f729b-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f729b-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f729b-132">-ResourceId</span></span>
<span data-ttu-id="f729b-133">要設定的實例容錯移轉群組資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f729b-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f729b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="f729b-134">-Confirm</span></span>
<span data-ttu-id="f729b-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f729b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f729b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f729b-136">-WhatIf</span></span>
<span data-ttu-id="f729b-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f729b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f729b-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f729b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f729b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f729b-139">CommonParameters</span></span>
<span data-ttu-id="f729b-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f729b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f729b-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f729b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f729b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="f729b-142">INPUTS</span></span>

### <span data-ttu-id="f729b-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f729b-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="f729b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f729b-144">System.String</span></span>

## <span data-ttu-id="f729b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f729b-145">OUTPUTS</span></span>

### <span data-ttu-id="f729b-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f729b-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="f729b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f729b-147">NOTES</span></span>

## <span data-ttu-id="f729b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f729b-148">RELATED LINKS</span></span>
