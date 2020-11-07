---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792724"
---
# <span data-ttu-id="f8129-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f8129-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="f8129-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8129-102">SYNOPSIS</span></span>
<span data-ttu-id="f8129-103">這個命令會建立新的 Azure SQL 資料庫實例 [容錯移轉] 群組。</span><span class="sxs-lookup"><span data-stu-id="f8129-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="f8129-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8129-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8129-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8129-105">DESCRIPTION</span></span>
<span data-ttu-id="f8129-106">在指定區域（具有已記下的受管理實例對）之間建立新的 Azure SQL 資料庫實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="f8129-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="f8129-107">在 Name 中建立兩個 Azure SQL Database TDS 端點 SqlDatabaseDnsSuffix (例如，Name.database.windows.net) 和 Name. SqlDatabaseDnsSuffix。</span><span class="sxs-lookup"><span data-stu-id="f8129-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="f8129-108">這些端點可用來連接至容錯移轉群組的主要和次要區域。</span><span class="sxs-lookup"><span data-stu-id="f8129-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="f8129-109">如果主要區域受中斷所影響，端點和資料庫的自動容錯移轉會根據實例容錯移轉群組的容錯移轉原則和寬限期來觸發。</span><span class="sxs-lookup"><span data-stu-id="f8129-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="f8129-110">在實例容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="f8129-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="f8129-111">示例</span><span class="sxs-lookup"><span data-stu-id="f8129-111">EXAMPLES</span></span>

### <span data-ttu-id="f8129-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f8129-112">Example 1</span></span>
```
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

<span data-ttu-id="f8129-113">這個命令會針對受管理的實例對，建立一個新的實例容錯移轉群組，其中包含容錯移轉原則「自動」。</span><span class="sxs-lookup"><span data-stu-id="f8129-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="f8129-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f8129-114">Example 2</span></span>
```
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

<span data-ttu-id="f8129-115">這個命令會針對受管理的實例對，建立具有容錯移轉原則「手動」的新實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="f8129-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="f8129-116">參數</span><span class="sxs-lookup"><span data-stu-id="f8129-116">PARAMETERS</span></span>

### <span data-ttu-id="f8129-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="f8129-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="f8129-118">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="f8129-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="f8129-119">尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="f8129-119">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8129-120">-DefaultProfile</span></span>
<span data-ttu-id="f8129-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8129-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8129-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="f8129-122">-FailoverPolicy</span></span>
<span data-ttu-id="f8129-123">實例容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="f8129-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="f8129-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="f8129-125">啟動自動容錯移轉前的間隔如果主伺服器發生停機，而容錯移轉無法在不遺失資料的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="f8129-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-126">-位置</span><span class="sxs-lookup"><span data-stu-id="f8129-126">-Location</span></span>
<span data-ttu-id="f8129-127">要從中取得實例容錯移轉群組的本機區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f8129-128">-Name</span></span>
<span data-ttu-id="f8129-129">要建立之 Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-130">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="f8129-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="f8129-131">要新增至 [實例容錯移轉] 群組之夥伴區域中之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="f8129-132">-PartnerRegion</span></span>
<span data-ttu-id="f8129-133">實例容錯移轉群組之夥伴區域的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8129-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f8129-135">[實例容錯移轉] 群組之次要資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-136">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8129-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="f8129-137">實例容錯移轉群組之次要管理實例的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8129-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="f8129-138">只有跨訂閱設定才需要此參數</span><span class="sxs-lookup"><span data-stu-id="f8129-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="f8129-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="f8129-140">要新增至實例容錯移轉群組之本機區域中之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8129-141">-ResourceGroupName</span></span>
<span data-ttu-id="f8129-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8129-142">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8129-143">-確認</span><span class="sxs-lookup"><span data-stu-id="f8129-143">-Confirm</span></span>
<span data-ttu-id="f8129-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f8129-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8129-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8129-145">-WhatIf</span></span>
<span data-ttu-id="f8129-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8129-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8129-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8129-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8129-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8129-148">CommonParameters</span></span>
<span data-ttu-id="f8129-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8129-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8129-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8129-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8129-151">輸入</span><span class="sxs-lookup"><span data-stu-id="f8129-151">INPUTS</span></span>

### <span data-ttu-id="f8129-152">System.object</span><span class="sxs-lookup"><span data-stu-id="f8129-152">System.String</span></span>

## <span data-ttu-id="f8129-153">輸出</span><span class="sxs-lookup"><span data-stu-id="f8129-153">OUTPUTS</span></span>

### <span data-ttu-id="f8129-154">AzureSqlInstanceFailoverGroupModel 中的 [InstanceFailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="f8129-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="f8129-155">筆記</span><span class="sxs-lookup"><span data-stu-id="f8129-155">NOTES</span></span>

## <span data-ttu-id="f8129-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8129-156">RELATED LINKS</span></span>
