---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8ac386eba93f2d9083c086c1ff2b1ab3faca6be4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906490"
---
# <span data-ttu-id="55755-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="55755-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="55755-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55755-102">SYNOPSIS</span></span>
<span data-ttu-id="55755-103">此命令會建立一個新的 Azure SQL 資料庫實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="55755-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="55755-104">語法</span><span class="sxs-lookup"><span data-stu-id="55755-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55755-105">描述</span><span class="sxs-lookup"><span data-stu-id="55755-105">DESCRIPTION</span></span>
<span data-ttu-id="55755-106">使用指定的受管理實例組，在指定的區域之間建立新的 Azure SQL 資料庫實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="55755-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="55755-107">在 Name.SqlDatabaseDnsSuffix (建立兩個 Azure SQL Database TDS 端點，例如 Name.database.windows.net) 和 Name.secondary.SqlDatabaseDnsSuffix。</span><span class="sxs-lookup"><span data-stu-id="55755-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="55755-108">這些端點可能分別用來連接容錯移轉群組的主要和次要區域。</span><span class="sxs-lookup"><span data-stu-id="55755-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="55755-109">如果主要區域受到中斷影響，端點和資料庫的自動容錯移轉就會根據實例容錯移轉群組的容錯移轉政策與寬限期所指示來觸發。</span><span class="sxs-lookup"><span data-stu-id="55755-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="55755-110">在實例容錯移轉群組功能預覽期間，'-GracePeriodWithDataLossHours'參數僅支援大於或等於 1 小時的值。</span><span class="sxs-lookup"><span data-stu-id="55755-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="55755-111">例子</span><span class="sxs-lookup"><span data-stu-id="55755-111">EXAMPLES</span></span>

### <span data-ttu-id="55755-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="55755-112">Example 1</span></span>
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

<span data-ttu-id="55755-113">此命令會針對受管理的實例組建立一個新的實例容錯移轉群組，其容錯移轉策略為 '自動'。</span><span class="sxs-lookup"><span data-stu-id="55755-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="55755-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="55755-114">Example 2</span></span>
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

<span data-ttu-id="55755-115">此命令會建立一個新的實例容錯移轉群組，並針對受管理的實例組使用容錯移轉策略的'手動'。</span><span class="sxs-lookup"><span data-stu-id="55755-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="55755-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="55755-116">Example 3</span></span>

<span data-ttu-id="55755-117">此命令會建立一個新的 Azure SQL 資料庫實例容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="55755-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="55755-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="55755-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="55755-119">參數</span><span class="sxs-lookup"><span data-stu-id="55755-119">PARAMETERS</span></span>

### <span data-ttu-id="55755-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="55755-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="55755-121">次要伺服器的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="55755-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="55755-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55755-122">-DefaultProfile</span></span>
<span data-ttu-id="55755-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55755-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55755-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="55755-124">-FailoverPolicy</span></span>
<span data-ttu-id="55755-125">實例容錯移轉群組的容錯移轉策略。</span><span class="sxs-lookup"><span data-stu-id="55755-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="55755-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="55755-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="55755-127">如果主伺服器上發生中斷，且無法在不遺失資料的情況下完成容錯移轉，則自動容錯移轉啟動前的間隔。</span><span class="sxs-lookup"><span data-stu-id="55755-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="55755-128">-位置</span><span class="sxs-lookup"><span data-stu-id="55755-128">-Location</span></span>
<span data-ttu-id="55755-129">要從其中取回實例容錯移轉群組的當地地區名稱。</span><span class="sxs-lookup"><span data-stu-id="55755-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="55755-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="55755-130">-Name</span></span>
<span data-ttu-id="55755-131">要建立之 Azure SQL 資料庫容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55755-131">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="55755-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="55755-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="55755-133">合作夥伴地區中要新增到實例容錯移轉群組的受管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="55755-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="55755-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="55755-134">-PartnerRegion</span></span>
<span data-ttu-id="55755-135">實例容錯移轉群組的合作夥伴區功能變數名稱稱。</span><span class="sxs-lookup"><span data-stu-id="55755-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="55755-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55755-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="55755-137">實例容錯移轉群組次要資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55755-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="55755-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55755-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="55755-139">實例容錯移轉群組次要受管理實例的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="55755-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="55755-140">此參數僅適用于跨訂閱設定</span><span class="sxs-lookup"><span data-stu-id="55755-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="55755-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="55755-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="55755-142">要新增到實例容錯移轉群組之本地地區的受管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="55755-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="55755-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55755-143">-ResourceGroupName</span></span>
<span data-ttu-id="55755-144">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55755-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="55755-145">-確認</span><span class="sxs-lookup"><span data-stu-id="55755-145">-Confirm</span></span>
<span data-ttu-id="55755-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55755-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55755-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55755-147">-WhatIf</span></span>
<span data-ttu-id="55755-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55755-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55755-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55755-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55755-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55755-150">CommonParameters</span></span>
<span data-ttu-id="55755-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55755-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55755-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55755-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55755-153">輸入</span><span class="sxs-lookup"><span data-stu-id="55755-153">INPUTS</span></span>

### <span data-ttu-id="55755-154">System.String</span><span class="sxs-lookup"><span data-stu-id="55755-154">System.String</span></span>

## <span data-ttu-id="55755-155">輸出</span><span class="sxs-lookup"><span data-stu-id="55755-155">OUTPUTS</span></span>

### <span data-ttu-id="55755-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="55755-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="55755-157">筆記</span><span class="sxs-lookup"><span data-stu-id="55755-157">NOTES</span></span>

## <span data-ttu-id="55755-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="55755-158">RELATED LINKS</span></span>
