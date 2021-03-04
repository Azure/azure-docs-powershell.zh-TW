---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: be1f2fc5c0aa2abda5f036580e377f05b26c2eb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907998"
---
# <span data-ttu-id="b8709-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="b8709-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8709-102">SYNOPSIS</span></span>
<span data-ttu-id="b8709-103">此命令會建立一個新的 Azure SQL 資料庫容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="b8709-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="b8709-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8709-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8709-105">描述</span><span class="sxs-lookup"><span data-stu-id="b8709-105">DESCRIPTION</span></span>
<span data-ttu-id="b8709-106">為指定的伺服器建立新的 Azure SQL 資料庫容錯移轉群組。</span><span class="sxs-lookup"><span data-stu-id="b8709-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="b8709-107">在 FailoverGroupName.SqlDatabaseDnsSuffix (建立兩個 Azure SQL Database TDS 端點，例如 FailoverGroupName.database.windows.net) 和 FailoverGroupName.secondary.SqlDatabaseDnsSuffix。</span><span class="sxs-lookup"><span data-stu-id="b8709-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="b8709-108">這些端點可能分別用來連接到容錯移轉群組中的主要和次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="b8709-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="b8709-109">如果主伺服器受到中斷影響，端點和資料庫的自動容錯移轉就會根據容錯移轉群組的容錯移轉政策與寬限期所指示而觸發。</span><span class="sxs-lookup"><span data-stu-id="b8709-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="b8709-110">新建立容錯移轉群組不包含任何資料庫。</span><span class="sxs-lookup"><span data-stu-id="b8709-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="b8709-111">若要控制容錯移轉群組中的資料庫集合，請使用 'Add-AzSqlDatabaseToFailoverGroup'和 'Remove-AzSqlDatabaseFromFailoverGroup' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8709-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="b8709-112">'-GracePeriodWithDataLossHours' 參數只支援大於或等於 1 小時的值。</span><span class="sxs-lookup"><span data-stu-id="b8709-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="b8709-113">例子</span><span class="sxs-lookup"><span data-stu-id="b8709-113">EXAMPLES</span></span>

### <span data-ttu-id="b8709-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="b8709-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="b8709-115">此命令會針對同一個資源群組中的兩個伺服器，建立一個新的容錯移轉群組，其容錯移轉策略為"自動」。</span><span class="sxs-lookup"><span data-stu-id="b8709-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="b8709-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="b8709-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="b8709-117">此命令會針對不同資源群組中的兩個伺服器，建立一個新的容錯移轉群組，其容錯移轉策略為'手動」。</span><span class="sxs-lookup"><span data-stu-id="b8709-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="b8709-118">參數</span><span class="sxs-lookup"><span data-stu-id="b8709-118">PARAMETERS</span></span>

### <span data-ttu-id="b8709-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="b8709-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="b8709-120">次要伺服器的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="b8709-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="b8709-121">目前尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="b8709-121">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8709-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8709-122">-DefaultProfile</span></span>
<span data-ttu-id="b8709-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b8709-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8709-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b8709-124">-FailoverGroupName</span></span>
<span data-ttu-id="b8709-125">要建立之 Azure SQL 資料庫容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8709-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="b8709-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b8709-126">-FailoverPolicy</span></span>
<span data-ttu-id="b8709-127">Azure SQL 資料庫容錯移轉群組的容錯移轉策略。</span><span class="sxs-lookup"><span data-stu-id="b8709-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8709-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="b8709-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="b8709-129">如果主伺服器上發生中斷，且無法在不遺失資料的情況下完成容錯移轉，則自動容錯移轉啟動前的間隔。</span><span class="sxs-lookup"><span data-stu-id="b8709-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8709-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8709-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b8709-131">Azure SQL 資料庫容錯移轉群組的次要資源組名。</span><span class="sxs-lookup"><span data-stu-id="b8709-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b8709-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="b8709-132">-PartnerServerName</span></span>
<span data-ttu-id="b8709-133">Azure SQL 資料庫容錯移轉群組的次要伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b8709-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b8709-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8709-134">-ResourceGroupName</span></span>
<span data-ttu-id="b8709-135">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8709-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8709-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8709-136">-ServerName</span></span>
<span data-ttu-id="b8709-137">容錯移轉群組的主要 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="b8709-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8709-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8709-138">CommonParameters</span></span>
<span data-ttu-id="b8709-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8709-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8709-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8709-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8709-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b8709-141">INPUTS</span></span>

### <span data-ttu-id="b8709-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b8709-142">System.String</span></span>

## <span data-ttu-id="b8709-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b8709-143">OUTPUTS</span></span>

### <span data-ttu-id="b8709-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b8709-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="b8709-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b8709-145">NOTES</span></span>

## <span data-ttu-id="b8709-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8709-146">RELATED LINKS</span></span>

[<span data-ttu-id="b8709-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8709-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8709-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b8709-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="b8709-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8709-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b8709-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b8709-153">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b8709-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
