---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 825d6f367fb4fbace53fccdb8798d17a915fc2bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129834"
---
# <span data-ttu-id="897c9-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="897c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="897c9-102">SYNOPSIS</span></span>
<span data-ttu-id="897c9-103">修改 Azure SQL Database 容錯移轉群組的設定。</span><span class="sxs-lookup"><span data-stu-id="897c9-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="897c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="897c9-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="897c9-105">說明</span><span class="sxs-lookup"><span data-stu-id="897c9-105">DESCRIPTION</span></span>
<span data-ttu-id="897c9-106">這個命令會修改 Azure SQL Database 容錯移轉群組的設定。</span><span class="sxs-lookup"><span data-stu-id="897c9-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="897c9-107">應使用容錯移轉群組的主要伺服器來執行命令。</span><span class="sxs-lookup"><span data-stu-id="897c9-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="897c9-108">若要控制群組中的一組資料庫，請改用 [Add-AzSqlDatabaseToFailoverGroup] 和 [Remove-AzSqlDatabaseFromFailoverGroup]。</span><span class="sxs-lookup"><span data-stu-id="897c9-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="897c9-109">在容錯移轉群組功能的預覽期間，"-GracePeriodWithDataLossHours" 參數只支援大於或等於1小時的值。</span><span class="sxs-lookup"><span data-stu-id="897c9-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="897c9-110">示例</span><span class="sxs-lookup"><span data-stu-id="897c9-110">EXAMPLES</span></span>

### <span data-ttu-id="897c9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="897c9-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="897c9-112">將容錯移轉群組的容錯移轉原則設定為「自動」。</span><span class="sxs-lookup"><span data-stu-id="897c9-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="897c9-113">範例2</span><span class="sxs-lookup"><span data-stu-id="897c9-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="897c9-114">透過 [轉移] 群組中的管道，將容錯移轉群組的容錯移轉原則設定為「手動」。</span><span class="sxs-lookup"><span data-stu-id="897c9-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="897c9-115">參數</span><span class="sxs-lookup"><span data-stu-id="897c9-115">PARAMETERS</span></span>

### <span data-ttu-id="897c9-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="897c9-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="897c9-117">在次要伺服器上的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="897c9-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="897c9-118">尚不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="897c9-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="897c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="897c9-119">-DefaultProfile</span></span>
<span data-ttu-id="897c9-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="897c9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="897c9-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="897c9-121">-FailoverGroupName</span></span>
<span data-ttu-id="897c9-122">Azure SQL Database 容錯移轉群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="897c9-122">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="897c9-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="897c9-123">-FailoverPolicy</span></span>
<span data-ttu-id="897c9-124">Azure SQL Database 容錯移轉群組的容錯移轉原則。</span><span class="sxs-lookup"><span data-stu-id="897c9-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="897c9-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="897c9-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="897c9-126">如果主要伺服器發生停機，就會啟動自動容錯移轉前的間隔。</span><span class="sxs-lookup"><span data-stu-id="897c9-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="897c9-127">這表示 Azure SQL 資料庫將不會在寬限期到期前啟動自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="897c9-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="897c9-128">請注意，使用 AllowDataLoss 選項的容錯移轉作業可能會因非同步同步處理的性質而導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="897c9-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="897c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="897c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="897c9-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="897c9-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="897c9-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="897c9-131">-ServerName</span></span>
<span data-ttu-id="897c9-132">容錯移轉群組之主要 Azure SQL Database 伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="897c9-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="897c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="897c9-133">CommonParameters</span></span>
<span data-ttu-id="897c9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="897c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="897c9-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="897c9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="897c9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="897c9-136">INPUTS</span></span>

### <span data-ttu-id="897c9-137">System.object</span><span class="sxs-lookup"><span data-stu-id="897c9-137">System.String</span></span>

## <span data-ttu-id="897c9-138">輸出</span><span class="sxs-lookup"><span data-stu-id="897c9-138">OUTPUTS</span></span>

### <span data-ttu-id="897c9-139">AzureSqlFailoverGroupModel 中的 [FailoverGroup]</span><span class="sxs-lookup"><span data-stu-id="897c9-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="897c9-140">筆記</span><span class="sxs-lookup"><span data-stu-id="897c9-140">NOTES</span></span>

## <span data-ttu-id="897c9-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="897c9-141">RELATED LINKS</span></span>

[<span data-ttu-id="897c9-142">新-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-142">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="897c9-143">AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-143">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="897c9-144">附加 AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-144">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="897c9-145">移除-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-145">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="897c9-146">切換 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-146">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="897c9-147">移除-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="897c9-147">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="897c9-148">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="897c9-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
