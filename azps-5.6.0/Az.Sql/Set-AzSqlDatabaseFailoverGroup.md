---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 94f4448816bc7cf60272f602caafbf5be6f1a3f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913026"
---
# <span data-ttu-id="c5840-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c5840-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5840-102">SYNOPSIS</span></span>
<span data-ttu-id="c5840-103">修改 Azure SQL 資料庫容錯移轉群組的群組原則。</span><span class="sxs-lookup"><span data-stu-id="c5840-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="c5840-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5840-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5840-105">描述</span><span class="sxs-lookup"><span data-stu-id="c5840-105">DESCRIPTION</span></span>
<span data-ttu-id="c5840-106">此命令會修改 Azure SQL 資料庫容錯移轉群組的群組原則。</span><span class="sxs-lookup"><span data-stu-id="c5840-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="c5840-107">容錯移轉群組的主伺服器應該用來執行命令。</span><span class="sxs-lookup"><span data-stu-id="c5840-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="c5840-108">若要控制群組中的資料庫集，請改為使用 "Add-AzSqlDatabaseToFailoverGroup" 和 'Remove-AzSqlDatabaseFromFailoverGroup'。</span><span class="sxs-lookup"><span data-stu-id="c5840-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="c5840-109">在預覽容錯移轉群組功能期間，'-GracePeriodWithDataLossHours'參數僅支援大於或等於 1 小時的值。</span><span class="sxs-lookup"><span data-stu-id="c5840-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="c5840-110">例子</span><span class="sxs-lookup"><span data-stu-id="c5840-110">EXAMPLES</span></span>

### <span data-ttu-id="c5840-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c5840-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="c5840-112">將容錯移轉群組的容錯移轉策略設定為'自動'。</span><span class="sxs-lookup"><span data-stu-id="c5840-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="c5840-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="c5840-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="c5840-114">在容錯移轉群組中設定點子，將容錯移轉群組的容錯移轉策略設定為'手動'。</span><span class="sxs-lookup"><span data-stu-id="c5840-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="c5840-115">參數</span><span class="sxs-lookup"><span data-stu-id="c5840-115">PARAMETERS</span></span>

### <span data-ttu-id="c5840-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="c5840-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="c5840-117">次要伺服器的中斷是否應該觸發唯讀端點的自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c5840-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="c5840-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5840-118">-DefaultProfile</span></span>
<span data-ttu-id="c5840-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c5840-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5840-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c5840-120">-FailoverGroupName</span></span>
<span data-ttu-id="c5840-121">Azure SQL 資料庫容錯移轉組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5840-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="c5840-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c5840-122">-FailoverPolicy</span></span>
<span data-ttu-id="c5840-123">Azure SQL 資料庫容錯移轉群組的容錯移轉策略。</span><span class="sxs-lookup"><span data-stu-id="c5840-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="c5840-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="c5840-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="c5840-125">如果主伺服器上發生中斷，自動容錯移轉啟動前的間隔。</span><span class="sxs-lookup"><span data-stu-id="c5840-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="c5840-126">這表示 Azure SQL Database 不會在寬限期到期之前啟動自動容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c5840-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="c5840-127">請注意，由於非同步同步處理的性質，使用 AllowDataLoss 選項執行容錯移轉作業可能會導致資料遺失。</span><span class="sxs-lookup"><span data-stu-id="c5840-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="c5840-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5840-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5840-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5840-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5840-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c5840-130">-ServerName</span></span>
<span data-ttu-id="c5840-131">容錯移轉群組的主要 Azure SQL 資料庫伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="c5840-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c5840-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5840-132">CommonParameters</span></span>
<span data-ttu-id="c5840-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5840-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5840-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5840-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5840-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c5840-135">INPUTS</span></span>

### <span data-ttu-id="c5840-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c5840-136">System.String</span></span>

## <span data-ttu-id="c5840-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c5840-137">OUTPUTS</span></span>

### <span data-ttu-id="c5840-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c5840-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c5840-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c5840-139">NOTES</span></span>

## <span data-ttu-id="c5840-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5840-140">RELATED LINKS</span></span>

[<span data-ttu-id="c5840-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c5840-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c5840-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c5840-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c5840-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c5840-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c5840-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c5840-147">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c5840-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
