---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7a893099a81225f165fc6fc56c6ba3fd6cfaec3a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970102"
---
# <span data-ttu-id="3c081-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="3c081-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="3c081-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c081-102">SYNOPSIS</span></span>
<span data-ttu-id="3c081-103">這個命令會建立新的 Azure SQL 資料庫實例 [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="3c081-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="3c081-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c081-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c081-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c081-105">DESCRIPTION</span></span>
<span data-ttu-id="3c081-106">在指定區域（具有已記下的受管理實例對）之間建立新的 Azure SQL 資料庫實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="3c081-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="3c081-107">在 Name 中建立兩個 Azure SQL Database TDS 端點 SqlDatabaseDnsSuffix (例如，Name.database.windows.net) 和 Name. SqlDatabaseDnsSuffix。</span><span class="sxs-lookup"><span data-stu-id="3c081-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="3c081-108">這些端點可用來連接至容錯移轉群組的主要和次要區域。</span><span class="sxs-lookup"><span data-stu-id="3c081-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="3c081-109">如果主要區域受中斷所影響，端點和資料庫的自動容錯移轉會根據實例容錯移轉群組的容錯移轉原則和寬限期來觸發。</span><span class="sxs-lookup"><span data-stu-id="3c081-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="3c081-110">在實例容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="3c081-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="3c081-111">示例</span><span class="sxs-lookup"><span data-stu-id="3c081-111">EXAMPLES</span></span>

### <span data-ttu-id="3c081-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3c081-112">Example 1</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
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

<span data-ttu-id="3c081-113">這個命令會針對受管理的實例對，建立一個新的實例容錯移轉群組，其中包含容錯移轉原則「自動」。</span><span class="sxs-lookup"><span data-stu-id="3c081-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="3c081-114">範例2</span><span class="sxs-lookup"><span data-stu-id="3c081-114">Example 2</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
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

<span data-ttu-id="3c081-115">這個命令會針對受管理的實例對，建立具有容錯移轉原則「手動」的新實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="3c081-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="3c081-116">範例3</span><span class="sxs-lookup"><span data-stu-id="3c081-116">Example 3</span></span>

<span data-ttu-id="3c081-117">這個命令會建立新的 Azure SQL 資料庫實例 [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="3c081-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="3c081-118"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="3c081-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="3c081-119">參數</span><span class="sxs-lookup"><span data-stu-id="3c081-119">PARAMETERS</span></span>

### <span data-ttu-id="3c081-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="3c081-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="3c081-121">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="3c081-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="3c081-122">尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="3c081-122">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="3c081-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c081-123">-DefaultProfile</span></span>
<span data-ttu-id="3c081-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c081-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c081-125">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="3c081-125">-FailoverPolicy</span></span>
<span data-ttu-id="3c081-126">實例容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="3c081-126">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="3c081-127">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="3c081-127">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="3c081-128">啟動自動容錯移轉前的間隔如果主伺服器發生停機，而容錯移轉無法在不遺失資料的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="3c081-128">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="3c081-129">-位置</span><span class="sxs-lookup"><span data-stu-id="3c081-129">-Location</span></span>
<span data-ttu-id="3c081-130">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-130">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c081-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c081-131">-Name</span></span>
<span data-ttu-id="3c081-132">要建立之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-132">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c081-133">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="3c081-133">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="3c081-134">要新增至 [實例容錯移轉] 群組之夥伴區域中之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-134">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c081-135">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="3c081-135">-PartnerRegion</span></span>
<span data-ttu-id="3c081-136">實例容錯移轉群組之夥伴區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-136">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c081-137">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c081-137">-PartnerResourceGroupName</span></span>
<span data-ttu-id="3c081-138">[實例容錯移轉] 群組之次要資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-138">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="3c081-139">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c081-139">-PartnerSubscriptionId</span></span>
<span data-ttu-id="3c081-140">實例容錯移轉群組之次要管理實例的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c081-140">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="3c081-141">只有跨訂閱設定才需要此參數</span><span class="sxs-lookup"><span data-stu-id="3c081-141">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="3c081-142">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="3c081-142">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="3c081-143">要新增至實例容錯移轉群組之本機區域中之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-143">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c081-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c081-144">-ResourceGroupName</span></span>
<span data-ttu-id="3c081-145">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c081-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c081-146">-確認</span><span class="sxs-lookup"><span data-stu-id="3c081-146">-Confirm</span></span>
<span data-ttu-id="3c081-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3c081-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c081-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c081-148">-WhatIf</span></span>
<span data-ttu-id="3c081-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3c081-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c081-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3c081-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c081-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c081-151">CommonParameters</span></span>
<span data-ttu-id="3c081-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c081-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c081-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3c081-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c081-154">輸入</span><span class="sxs-lookup"><span data-stu-id="3c081-154">INPUTS</span></span>

### <span data-ttu-id="3c081-155">System.object</span><span class="sxs-lookup"><span data-stu-id="3c081-155">System.String</span></span>

## <span data-ttu-id="3c081-156">輸出</span><span class="sxs-lookup"><span data-stu-id="3c081-156">OUTPUTS</span></span>

### <span data-ttu-id="3c081-157">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="3c081-157">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="3c081-158">筆記</span><span class="sxs-lookup"><span data-stu-id="3c081-158">NOTES</span></span>

## <span data-ttu-id="3c081-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c081-159">RELATED LINKS</span></span>
