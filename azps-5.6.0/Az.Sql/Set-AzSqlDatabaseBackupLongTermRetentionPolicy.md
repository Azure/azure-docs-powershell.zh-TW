---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 9726d945b4e0fada340d06e780008f1921fb6f1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913053"
---
# <span data-ttu-id="ca15a-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca15a-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="ca15a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ca15a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca15a-103">設定伺服器長期保留政策。</span><span class="sxs-lookup"><span data-stu-id="ca15a-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="ca15a-104">語法</span><span class="sxs-lookup"><span data-stu-id="ca15a-104">SYNTAX</span></span>

### <span data-ttu-id="ca15a-105">WeeklyRetentionRequired (預設) </span><span class="sxs-lookup"><span data-stu-id="ca15a-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca15a-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="ca15a-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca15a-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="ca15a-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca15a-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="ca15a-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca15a-109">描述</span><span class="sxs-lookup"><span data-stu-id="ca15a-109">DESCRIPTION</span></span>
<span data-ttu-id="ca15a-110">**Set-AzSqlDatabaseBackupLongTermRetentionPolidlet** 會設定已登錄至此資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="ca15a-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="ca15a-111">此策略是 Azure 備份資源，用來定義備份儲存策略。</span><span class="sxs-lookup"><span data-stu-id="ca15a-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="ca15a-112">例子</span><span class="sxs-lookup"><span data-stu-id="ca15a-112">EXAMPLES</span></span>

### <span data-ttu-id="ca15a-113">範例 1：設定目前長期保留政策版本的每週保留</span><span class="sxs-lookup"><span data-stu-id="ca15a-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="ca15a-114">這會設定資料庫01 的長期保留原則，將每週完整備份儲存 2 周</span><span class="sxs-lookup"><span data-stu-id="ca15a-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="ca15a-115">範例 2：設定目前長期保留政策版本的每月保留</span><span class="sxs-lookup"><span data-stu-id="ca15a-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="ca15a-116">這會設定資料庫01 的長期保留政策，將每個月的第一次完整備份儲存 5 年</span><span class="sxs-lookup"><span data-stu-id="ca15a-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="ca15a-117">範例 3：設定目前長期保留政策版本的每年保留</span><span class="sxs-lookup"><span data-stu-id="ca15a-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="ca15a-118">這會設定資料庫01 的長期保留政策，以將一年的第 26 周所執行的完整備份儲存 10 年</span><span class="sxs-lookup"><span data-stu-id="ca15a-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="ca15a-119">範例 4：針對目前版本的長期保留政策設定每個保留</span><span class="sxs-lookup"><span data-stu-id="ca15a-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="ca15a-120">這會設定資料庫01 的長期保留原則，將每個完整備份儲存 14 天、每個月的第一次完整備份為 24 周，以及 10 年一年的第 26 周執行完整備份</span><span class="sxs-lookup"><span data-stu-id="ca15a-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="ca15a-121">範例 5：移除長期保留政策</span><span class="sxs-lookup"><span data-stu-id="ca15a-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="ca15a-122">移除資料庫01 的策略，如此一來就不會再存下任何長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="ca15a-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="ca15a-123">這不會影響已採取的備份</span><span class="sxs-lookup"><span data-stu-id="ca15a-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="ca15a-124">範例 6：移除長期保留政策</span><span class="sxs-lookup"><span data-stu-id="ca15a-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="ca15a-125">這是移除資料庫01 之策略的另一種方式，因此不會再節省任何長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="ca15a-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="ca15a-126">這不會影響已採取的備份</span><span class="sxs-lookup"><span data-stu-id="ca15a-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="ca15a-127">參數</span><span class="sxs-lookup"><span data-stu-id="ca15a-127">PARAMETERS</span></span>

### <span data-ttu-id="ca15a-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca15a-128">-DatabaseName</span></span>
<span data-ttu-id="ca15a-129">要使用的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="ca15a-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="ca15a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca15a-130">-DefaultProfile</span></span>
<span data-ttu-id="ca15a-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca15a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca15a-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="ca15a-132">-MonthlyRetention</span></span>
<span data-ttu-id="ca15a-133">每月保留。</span><span class="sxs-lookup"><span data-stu-id="ca15a-133">The Monthly Retention.</span></span>
<span data-ttu-id="ca15a-134">如果只傳遞數位而非 ISO 8601 字串，則天數會假設為單位。</span><span class="sxs-lookup"><span data-stu-id="ca15a-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="ca15a-135">最短為 7 天，最多 10 年。</span><span class="sxs-lookup"><span data-stu-id="ca15a-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="ca15a-136">-RemovePolicy</span></span>
<span data-ttu-id="ca15a-137">如果提供，將會移除資料庫的這個策略。</span><span class="sxs-lookup"><span data-stu-id="ca15a-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca15a-138">-ResourceGroupName</span></span>
<span data-ttu-id="ca15a-139">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca15a-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca15a-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ca15a-140">-ServerName</span></span>
<span data-ttu-id="ca15a-141">資料庫位於中的 Azure SQL Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="ca15a-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="ca15a-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="ca15a-142">-WeeklyRetention</span></span>
<span data-ttu-id="ca15a-143">每週保留。</span><span class="sxs-lookup"><span data-stu-id="ca15a-143">The Weekly Retention.</span></span>
<span data-ttu-id="ca15a-144">如果只傳遞數位而非 ISO 8601 字串，則天數會假設為單位。</span><span class="sxs-lookup"><span data-stu-id="ca15a-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="ca15a-145">最短為 7 天，最多 10 年。</span><span class="sxs-lookup"><span data-stu-id="ca15a-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="ca15a-146">-WeekOfYear</span></span>
<span data-ttu-id="ca15a-147">一年中的 1 到 52 周，以儲存為每年保留。</span><span class="sxs-lookup"><span data-stu-id="ca15a-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="ca15a-148">-YearlyRetention</span></span>
<span data-ttu-id="ca15a-149">每年保留。</span><span class="sxs-lookup"><span data-stu-id="ca15a-149">The Yearly Retention.</span></span>
<span data-ttu-id="ca15a-150">如果只傳遞數位而非 ISO 8601 字串，則天數會假設為單位。</span><span class="sxs-lookup"><span data-stu-id="ca15a-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="ca15a-151">最短為 7 天，最多 10 年。</span><span class="sxs-lookup"><span data-stu-id="ca15a-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-152">-確認</span><span class="sxs-lookup"><span data-stu-id="ca15a-152">-Confirm</span></span>
<span data-ttu-id="ca15a-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ca15a-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca15a-154">-WhatIf</span></span>
<span data-ttu-id="ca15a-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca15a-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca15a-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca15a-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca15a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca15a-157">CommonParameters</span></span>
<span data-ttu-id="ca15a-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ca15a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca15a-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca15a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca15a-160">輸入</span><span class="sxs-lookup"><span data-stu-id="ca15a-160">INPUTS</span></span>

### <span data-ttu-id="ca15a-161">System.String</span><span class="sxs-lookup"><span data-stu-id="ca15a-161">System.String</span></span>

### <span data-ttu-id="ca15a-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ca15a-162">System.Int32</span></span>

## <span data-ttu-id="ca15a-163">輸出</span><span class="sxs-lookup"><span data-stu-id="ca15a-163">OUTPUTS</span></span>

### <span data-ttu-id="ca15a-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ca15a-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="ca15a-165">筆記</span><span class="sxs-lookup"><span data-stu-id="ca15a-165">NOTES</span></span>

## <span data-ttu-id="ca15a-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca15a-166">RELATED LINKS</span></span>

[<span data-ttu-id="ca15a-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ca15a-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="ca15a-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ca15a-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ca15a-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="ca15a-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="ca15a-170">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="ca15a-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)