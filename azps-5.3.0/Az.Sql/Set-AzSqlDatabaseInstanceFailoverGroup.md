---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434986"
---
# <span data-ttu-id="a5ada-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a5ada-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="a5ada-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5ada-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ada-103">修改實例容錯移轉群組的配置。</span><span class="sxs-lookup"><span data-stu-id="a5ada-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="a5ada-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5ada-104">SYNTAX</span></span>

### <span data-ttu-id="a5ada-105">SetInstanceFailoverGroupDefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a5ada-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ada-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a5ada-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ada-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="a5ada-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ada-108">說明</span><span class="sxs-lookup"><span data-stu-id="a5ada-108">DESCRIPTION</span></span>
<span data-ttu-id="a5ada-109">這個命令會修改實例容錯移轉群組的配置。</span><span class="sxs-lookup"><span data-stu-id="a5ada-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="a5ada-110">應使用實例容錯移轉群組的主要區域來執行命令。</span><span class="sxs-lookup"><span data-stu-id="a5ada-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="a5ada-111">在實例容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="a5ada-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="a5ada-112">示例</span><span class="sxs-lookup"><span data-stu-id="a5ada-112">EXAMPLES</span></span>

### <span data-ttu-id="a5ada-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a5ada-113">Example 1</span></span>
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

<span data-ttu-id="a5ada-114">透過 [容錯移轉] 群組中的管道，將實例容錯移轉群組的容錯移轉原則設定為「手動」。</span><span class="sxs-lookup"><span data-stu-id="a5ada-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="a5ada-115">參數</span><span class="sxs-lookup"><span data-stu-id="a5ada-115">PARAMETERS</span></span>

### <span data-ttu-id="a5ada-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="a5ada-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="a5ada-117">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="a5ada-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="a5ada-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ada-118">-DefaultProfile</span></span>
<span data-ttu-id="a5ada-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5ada-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ada-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="a5ada-120">-FailoverPolicy</span></span>
<span data-ttu-id="a5ada-121">實例容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="a5ada-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="a5ada-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="a5ada-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="a5ada-123">啟動自動容錯移轉前的間隔如果主伺服器發生停機，而容錯移轉無法在不遺失資料的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="a5ada-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="a5ada-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5ada-124">-InputObject</span></span>
<span data-ttu-id="a5ada-125">要設定的實例容錯移轉群組物件</span><span class="sxs-lookup"><span data-stu-id="a5ada-125">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="a5ada-126">-位置</span><span class="sxs-lookup"><span data-stu-id="a5ada-126">-Location</span></span>
<span data-ttu-id="a5ada-127">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a5ada-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="a5ada-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5ada-128">-Name</span></span>
<span data-ttu-id="a5ada-129">實例容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ada-129">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="a5ada-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ada-130">-ResourceGroupName</span></span>
<span data-ttu-id="a5ada-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5ada-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5ada-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ada-132">-ResourceId</span></span>
<span data-ttu-id="a5ada-133">要設定之實例容錯移轉群組的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5ada-133">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="a5ada-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a5ada-134">-Confirm</span></span>
<span data-ttu-id="a5ada-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5ada-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ada-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ada-136">-WhatIf</span></span>
<span data-ttu-id="a5ada-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5ada-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ada-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5ada-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ada-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ada-139">CommonParameters</span></span>
<span data-ttu-id="a5ada-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5ada-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ada-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5ada-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ada-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a5ada-142">INPUTS</span></span>

### <span data-ttu-id="a5ada-143">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="a5ada-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="a5ada-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a5ada-144">System.String</span></span>

## <span data-ttu-id="a5ada-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a5ada-145">OUTPUTS</span></span>

### <span data-ttu-id="a5ada-146">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="a5ada-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="a5ada-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a5ada-147">NOTES</span></span>

## <span data-ttu-id="a5ada-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5ada-148">RELATED LINKS</span></span>
