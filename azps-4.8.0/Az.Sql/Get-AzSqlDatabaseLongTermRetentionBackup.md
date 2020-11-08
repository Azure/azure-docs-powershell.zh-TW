---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: e97143f282bc01bbdd9c5d6186f0ccb5532b1df1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127305"
---
# <span data-ttu-id="cdedd-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cdedd-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="cdedd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdedd-102">SYNOPSIS</span></span>
<span data-ttu-id="cdedd-103">取得一或多個長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="cdedd-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="cdedd-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdedd-104">SYNTAX</span></span>

### <span data-ttu-id="cdedd-105">預設)  (位置</span><span class="sxs-lookup"><span data-stu-id="cdedd-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-106">名稱</span><span class="sxs-lookup"><span data-stu-id="cdedd-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="cdedd-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdedd-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="cdedd-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="cdedd-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedd-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="cdedd-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdedd-112">說明</span><span class="sxs-lookup"><span data-stu-id="cdedd-112">DESCRIPTION</span></span>
<span data-ttu-id="cdedd-113">**AzSqlDatabaseLongTermRetentionBackup** Cmdlet 會取得位置、伺服器或資料庫的所有長期保留期備份，或取得特定的長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="cdedd-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="cdedd-114">示例</span><span class="sxs-lookup"><span data-stu-id="cdedd-114">EXAMPLES</span></span>

### <span data-ttu-id="cdedd-115">範例1：取得某個位置的所有備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-115">Example 1: Get all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM
```

<span data-ttu-id="cdedd-116">這個命令會針對所有 (資料庫（在 northeurope 中可能是動態或) 刪除），取得所有長時間保留期間備份，只有在伺服器為 [使用中] 時，才會設定資源群組。</span><span class="sxs-lookup"><span data-stu-id="cdedd-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="cdedd-117">範例2：取得資源群組下某個位置的所有備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-117">Example 2: Get all backups for a location under a resource group</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ResourceGroup resourceGroup01


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="cdedd-118">這個命令會在 northeurope 中的資源群組底下，為所有資料庫取得所有長時間保留備份， (可能是使用中或刪除的) 。</span><span class="sxs-lookup"><span data-stu-id="cdedd-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="cdedd-119">範例3：取得特定的長期保留備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-119">Example 3: Get a specific long term retention backup</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="cdedd-120">這個命令會取得名為 601061b7-d10b-46e0-bf77-a2bfb16a6add; 131655666550000000 的備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="cdedd-121">範例4：取得資料庫的所有長期保留備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-121">Example 4: Get all long term retention backups for a database</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="cdedd-122">這個命令會取得 database01 的所有長時間保留備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="cdedd-123">範例5：使用篩選來取得長期保留備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-123">Example 5: Get long term retention backups using filtering</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7*"

BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database02/longTermRetentionBackups/601061b7-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server01
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/resourceGroups/resourcegroup01/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="cdedd-124">這個命令會取得名稱開頭為 "601061b7" 的所有備份</span><span class="sxs-lookup"><span data-stu-id="cdedd-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="cdedd-125">參數</span><span class="sxs-lookup"><span data-stu-id="cdedd-125">PARAMETERS</span></span>

### <span data-ttu-id="cdedd-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="cdedd-126">-BackupName</span></span>
<span data-ttu-id="cdedd-127">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdedd-127">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByResourceId, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cdedd-128">-DatabaseName</span></span>
<span data-ttu-id="cdedd-129">備份所在之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdedd-129">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BackupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="cdedd-130">-DatabaseState</span></span>
<span data-ttu-id="cdedd-131">您想要尋找、[活]、[刪除] 或 [全部] 備份之資料庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="cdedd-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="cdedd-132">預設為 [全部]</span><span class="sxs-lookup"><span data-stu-id="cdedd-132">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdedd-133">-DefaultProfile</span></span>
<span data-ttu-id="cdedd-134">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdedd-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdedd-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdedd-135">-InputObject</span></span>
<span data-ttu-id="cdedd-136">要取得備份的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="cdedd-136">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-137">-位置</span><span class="sxs-lookup"><span data-stu-id="cdedd-137">-Location</span></span>
<span data-ttu-id="cdedd-138">備份源伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="cdedd-138">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName, GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="cdedd-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="cdedd-140">是否只取得每個資料庫的最新備份。</span><span class="sxs-lookup"><span data-stu-id="cdedd-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="cdedd-141">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="cdedd-141">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, ServerName, GetBackupsByResourceId, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdedd-142">-ResourceGroupName</span></span>
<span data-ttu-id="cdedd-143">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdedd-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, ServerName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdedd-144">-ResourceId</span></span>
<span data-ttu-id="cdedd-145">要取得備份的資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdedd-145">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId, GetBackupsByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cdedd-146">-ServerName</span></span>
<span data-ttu-id="cdedd-147">備份所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdedd-147">The name of the Azure SQL Server the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedd-148">-確認</span><span class="sxs-lookup"><span data-stu-id="cdedd-148">-Confirm</span></span>
<span data-ttu-id="cdedd-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cdedd-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdedd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdedd-150">-WhatIf</span></span>
<span data-ttu-id="cdedd-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdedd-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdedd-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdedd-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdedd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdedd-153">CommonParameters</span></span>
<span data-ttu-id="cdedd-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdedd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdedd-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cdedd-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdedd-156">輸入</span><span class="sxs-lookup"><span data-stu-id="cdedd-156">INPUTS</span></span>

### <span data-ttu-id="cdedd-157">AzureSqlDatabaseModel （.Sql）的。</span><span class="sxs-lookup"><span data-stu-id="cdedd-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="cdedd-158">System.object</span><span class="sxs-lookup"><span data-stu-id="cdedd-158">System.String</span></span>

## <span data-ttu-id="cdedd-159">輸出</span><span class="sxs-lookup"><span data-stu-id="cdedd-159">OUTPUTS</span></span>

### <span data-ttu-id="cdedd-160">AzureSqlDatabaseLongTermRetentionBackupModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="cdedd-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="cdedd-161">筆記</span><span class="sxs-lookup"><span data-stu-id="cdedd-161">NOTES</span></span>

## <span data-ttu-id="cdedd-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdedd-162">RELATED LINKS</span></span>

[<span data-ttu-id="cdedd-163">移除-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="cdedd-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="cdedd-164">AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cdedd-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cdedd-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cdedd-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="cdedd-166">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="cdedd-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)