---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c5450ea3ffdcc8c76fa88c8721902b8f8ae77794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447586"
---
# <span data-ttu-id="c6947-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6947-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="c6947-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6947-102">SYNOPSIS</span></span>
<span data-ttu-id="c6947-103">設定伺服器的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="c6947-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6947-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6947-104">SYNTAX</span></span>

### <span data-ttu-id="c6947-105">WeeklyRetentionRequired (預設) </span><span class="sxs-lookup"><span data-stu-id="c6947-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6947-106">型</span><span class="sxs-lookup"><span data-stu-id="c6947-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6947-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c6947-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6947-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c6947-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>] [-MonthlyRetention] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6947-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c6947-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>]
 [[-MonthlyRetention] <String>] [-YearlyRetention] <String> [-WeekOfYear] <Int32> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6947-110">說明</span><span class="sxs-lookup"><span data-stu-id="c6947-110">DESCRIPTION</span></span>
<span data-ttu-id="c6947-111">**AzureRmSqlDatabaseBackupLongTermRetentionPolicy** Cmdlet 會設定已登錄到此資料庫的長期保留原則。</span><span class="sxs-lookup"><span data-stu-id="c6947-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="c6947-112">原則是用來定義備份儲存原則的 Azure 備份資源。</span><span class="sxs-lookup"><span data-stu-id="c6947-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="c6947-113">示例</span><span class="sxs-lookup"><span data-stu-id="c6947-113">EXAMPLES</span></span>

### <span data-ttu-id="c6947-114">範例1：針對目前版本的長期保留原則設定每週保留期</span><span class="sxs-lookup"><span data-stu-id="c6947-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c6947-115">這會設定 database01 的長期保留原則，將每週完整備份儲存兩周</span><span class="sxs-lookup"><span data-stu-id="c6947-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="c6947-116">範例2：針對目前版本的長期保留原則設定每月保留期</span><span class="sxs-lookup"><span data-stu-id="c6947-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c6947-117">這會設定 database01 的長期保留原則，以將每個月的第一次完整備份儲存5年</span><span class="sxs-lookup"><span data-stu-id="c6947-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="c6947-118">範例3：針對目前版本的長期保留原則設定每年保留。</span><span class="sxs-lookup"><span data-stu-id="c6947-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c6947-119">這會設定 database01 的長期保留原則，以將一年中的一周完整備份儲存10年</span><span class="sxs-lookup"><span data-stu-id="c6947-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="c6947-120">範例4：針對目前版本的長期保留原則設定每個保留期</span><span class="sxs-lookup"><span data-stu-id="c6947-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c6947-121">這會設定 database01 的長期保留原則，以將每個完整備份儲存14天、24周的第一次完整備份，以及在一年的十周內執行完整備份（10年）</span><span class="sxs-lookup"><span data-stu-id="c6947-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="c6947-122">範例4：移除長期保留原則</span><span class="sxs-lookup"><span data-stu-id="c6947-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c6947-123">移除 database01 原則，讓它不再儲存任何長期保留期備份。</span><span class="sxs-lookup"><span data-stu-id="c6947-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="c6947-124">這不會影響已採取的備份</span><span class="sxs-lookup"><span data-stu-id="c6947-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="c6947-125">範例4：移除長期保留原則</span><span class="sxs-lookup"><span data-stu-id="c6947-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c6947-126">這是移除 database01 原則的另一種方式，因此它不會再儲存任何長期保留期備份。</span><span class="sxs-lookup"><span data-stu-id="c6947-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="c6947-127">這不會影響已採取的備份</span><span class="sxs-lookup"><span data-stu-id="c6947-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="c6947-128">參數</span><span class="sxs-lookup"><span data-stu-id="c6947-128">PARAMETERS</span></span>

### <span data-ttu-id="c6947-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6947-129">-DatabaseName</span></span>
<span data-ttu-id="c6947-130">要使用之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6947-130">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6947-131">-DefaultProfile</span></span>
<span data-ttu-id="c6947-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6947-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6947-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="c6947-133">-MonthlyRetention</span></span>
<span data-ttu-id="c6947-134">每月保留。</span><span class="sxs-lookup"><span data-stu-id="c6947-134">The Monthly Retention.</span></span>
<span data-ttu-id="c6947-135">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="c6947-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c6947-136">最小是7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="c6947-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c6947-137">-RemovePolicy</span></span>
<span data-ttu-id="c6947-138">如果有提供，資料庫的原則將會移除。</span><span class="sxs-lookup"><span data-stu-id="c6947-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6947-139">-ResourceGroupName</span></span>
<span data-ttu-id="c6947-140">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6947-140">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6947-141">-ResourceId</span></span>
<span data-ttu-id="c6947-142">備份長期保留原則的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6947-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6947-143">-ServerName</span></span>
<span data-ttu-id="c6947-144">資料庫所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6947-144">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-145">-State</span><span class="sxs-lookup"><span data-stu-id="c6947-145">-State</span></span>
<span data-ttu-id="c6947-146">長期保留備份原則的狀態為「已啟用」或「已停用」</span><span class="sxs-lookup"><span data-stu-id="c6947-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="c6947-147">-WeeklyRetention</span></span>
<span data-ttu-id="c6947-148">每週保留。</span><span class="sxs-lookup"><span data-stu-id="c6947-148">The Weekly Retention.</span></span>
<span data-ttu-id="c6947-149">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="c6947-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c6947-150">最小是7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="c6947-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="c6947-151">-WeekOfYear</span></span>
<span data-ttu-id="c6947-152">要儲存每年保留的年（1到52）的周。</span><span class="sxs-lookup"><span data-stu-id="c6947-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="c6947-153">-YearlyRetention</span></span>
<span data-ttu-id="c6947-154">每年保留。</span><span class="sxs-lookup"><span data-stu-id="c6947-154">The Yearly Retention.</span></span>
<span data-ttu-id="c6947-155">如果只傳遞數位而不是 ISO 8601 字串，則會將天數視為單位。</span><span class="sxs-lookup"><span data-stu-id="c6947-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c6947-156">最小是7天，最多10年。</span><span class="sxs-lookup"><span data-stu-id="c6947-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-157">-確認</span><span class="sxs-lookup"><span data-stu-id="c6947-157">-Confirm</span></span>
<span data-ttu-id="c6947-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6947-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6947-159">-WhatIf</span></span>
<span data-ttu-id="c6947-160">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6947-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6947-161">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6947-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6947-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6947-162">CommonParameters</span></span>
<span data-ttu-id="c6947-163">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6947-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c6947-164">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6947-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6947-165">輸入</span><span class="sxs-lookup"><span data-stu-id="c6947-165">INPUTS</span></span>

### <span data-ttu-id="c6947-166">所有</span><span class="sxs-lookup"><span data-stu-id="c6947-166">None</span></span>
<span data-ttu-id="c6947-167">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c6947-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6947-168">輸出</span><span class="sxs-lookup"><span data-stu-id="c6947-168">OUTPUTS</span></span>

### <span data-ttu-id="c6947-169">AzureSqlDatabaseBackupLongTermRetentionPolicyModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="c6947-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c6947-170">筆記</span><span class="sxs-lookup"><span data-stu-id="c6947-170">NOTES</span></span>

## <span data-ttu-id="c6947-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6947-171">RELATED LINKS</span></span>

[<span data-ttu-id="c6947-172">AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6947-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c6947-173">AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c6947-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c6947-174">移除-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c6947-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c6947-175">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="c6947-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
