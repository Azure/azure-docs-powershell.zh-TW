---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434994"
---
# <span data-ttu-id="cef6f-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cef6f-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="cef6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cef6f-102">SYNOPSIS</span></span>
<span data-ttu-id="cef6f-103">設定伺服器的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="cef6f-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="cef6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="cef6f-104">SYNTAX</span></span>

### <span data-ttu-id="cef6f-105">WeeklyRetentionRequired (預設) </span><span class="sxs-lookup"><span data-stu-id="cef6f-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef6f-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="cef6f-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cef6f-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="cef6f-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef6f-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="cef6f-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cef6f-109">說明</span><span class="sxs-lookup"><span data-stu-id="cef6f-109">DESCRIPTION</span></span>
<span data-ttu-id="cef6f-110">**AzSqlDatabaseBackupLongTermRetentionPolicy** Cmdlet 會設定已登錄到此資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="cef6f-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="cef6f-111">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="cef6f-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="cef6f-112">示例</span><span class="sxs-lookup"><span data-stu-id="cef6f-112">EXAMPLES</span></span>

### <span data-ttu-id="cef6f-113">範例1：針對目前版本的長期保留原則設定每週保留期</span><span class="sxs-lookup"><span data-stu-id="cef6f-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="cef6f-114">這會設定 database01 的長期保留原則，將每週完整備份儲存兩周</span><span class="sxs-lookup"><span data-stu-id="cef6f-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="cef6f-115">範例2：針對目前版本的長期保留原則設定每月保留期</span><span class="sxs-lookup"><span data-stu-id="cef6f-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="cef6f-116">這會設定 database01 的長期保留原則，以將每個月的第一次完整備份儲存5年</span><span class="sxs-lookup"><span data-stu-id="cef6f-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="cef6f-117">範例3：針對目前版本的長期保留原則設定每年保留。</span><span class="sxs-lookup"><span data-stu-id="cef6f-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="cef6f-118">這會設定 database01 的長期保留原則，以將一年中的一周完整備份儲存10年</span><span class="sxs-lookup"><span data-stu-id="cef6f-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="cef6f-119">範例4：針對目前版本的長期保留原則設定每個保留期</span><span class="sxs-lookup"><span data-stu-id="cef6f-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="cef6f-120">這會設定 database01 的長期保留原則，以將每個完整備份儲存14天、24周的第一次完整備份，以及在一年的十周內執行完整備份（10年）</span><span class="sxs-lookup"><span data-stu-id="cef6f-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="cef6f-121">範例5：移除長期保留原則</span><span class="sxs-lookup"><span data-stu-id="cef6f-121">Example 5: Remove the long term retention policy</span></span>
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

<span data-ttu-id="cef6f-122">移除 database01 原則，讓它不再儲存任何長期保留期備份。</span><span class="sxs-lookup"><span data-stu-id="cef6f-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="cef6f-123">這不會影響已採取的備份</span><span class="sxs-lookup"><span data-stu-id="cef6f-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="cef6f-124">範例6：移除長期保留原則</span><span class="sxs-lookup"><span data-stu-id="cef6f-124">Example 6: Remove the long term retention policy</span></span>
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

<span data-ttu-id="cef6f-125">這是移除 database01 原則的另一種方式，因此它不會再儲存任何長期保留期備份。</span><span class="sxs-lookup"><span data-stu-id="cef6f-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="cef6f-126">這不會影響已採取的備份</span><span class="sxs-lookup"><span data-stu-id="cef6f-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="cef6f-127">參數</span><span class="sxs-lookup"><span data-stu-id="cef6f-127">PARAMETERS</span></span>

### <span data-ttu-id="cef6f-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cef6f-128">-DatabaseName</span></span>
<span data-ttu-id="cef6f-129">要使用之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cef6f-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="cef6f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef6f-130">-DefaultProfile</span></span>
<span data-ttu-id="cef6f-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cef6f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cef6f-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="cef6f-132">-MonthlyRetention</span></span>
<span data-ttu-id="cef6f-133">每月保留。</span><span class="sxs-lookup"><span data-stu-id="cef6f-133">The Monthly Retention.</span></span>
<span data-ttu-id="cef6f-134">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="cef6f-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="cef6f-135">最少7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="cef6f-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="cef6f-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="cef6f-136">-RemovePolicy</span></span>
<span data-ttu-id="cef6f-137">如果有提供，資料庫的原則將會移除。</span><span class="sxs-lookup"><span data-stu-id="cef6f-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="cef6f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef6f-138">-ResourceGroupName</span></span>
<span data-ttu-id="cef6f-139">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cef6f-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="cef6f-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cef6f-140">-ServerName</span></span>
<span data-ttu-id="cef6f-141">資料庫所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cef6f-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="cef6f-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="cef6f-142">-WeeklyRetention</span></span>
<span data-ttu-id="cef6f-143">每週保留。</span><span class="sxs-lookup"><span data-stu-id="cef6f-143">The Weekly Retention.</span></span>
<span data-ttu-id="cef6f-144">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="cef6f-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="cef6f-145">最少7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="cef6f-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="cef6f-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="cef6f-146">-WeekOfYear</span></span>
<span data-ttu-id="cef6f-147">要儲存每年保留的年（1到52）的周。</span><span class="sxs-lookup"><span data-stu-id="cef6f-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="cef6f-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="cef6f-148">-YearlyRetention</span></span>
<span data-ttu-id="cef6f-149">每年保留。</span><span class="sxs-lookup"><span data-stu-id="cef6f-149">The Yearly Retention.</span></span>
<span data-ttu-id="cef6f-150">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="cef6f-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="cef6f-151">最少7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="cef6f-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="cef6f-152">-確認</span><span class="sxs-lookup"><span data-stu-id="cef6f-152">-Confirm</span></span>
<span data-ttu-id="cef6f-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cef6f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef6f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef6f-154">-WhatIf</span></span>
<span data-ttu-id="cef6f-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cef6f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef6f-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cef6f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef6f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef6f-157">CommonParameters</span></span>
<span data-ttu-id="cef6f-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cef6f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef6f-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cef6f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef6f-160">輸入</span><span class="sxs-lookup"><span data-stu-id="cef6f-160">INPUTS</span></span>

### <span data-ttu-id="cef6f-161">System.object</span><span class="sxs-lookup"><span data-stu-id="cef6f-161">System.String</span></span>

### <span data-ttu-id="cef6f-162">System.object</span><span class="sxs-lookup"><span data-stu-id="cef6f-162">System.Int32</span></span>

## <span data-ttu-id="cef6f-163">輸出</span><span class="sxs-lookup"><span data-stu-id="cef6f-163">OUTPUTS</span></span>

### <span data-ttu-id="cef6f-164">AzureSqlDatabaseBackupLongTermRetentionPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="cef6f-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="cef6f-165">筆記</span><span class="sxs-lookup"><span data-stu-id="cef6f-165">NOTES</span></span>

## <span data-ttu-id="cef6f-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="cef6f-166">RELATED LINKS</span></span>

[<span data-ttu-id="cef6f-167">AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cef6f-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cef6f-168">AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cef6f-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="cef6f-169">移除-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cef6f-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="cef6f-170">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cef6f-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)