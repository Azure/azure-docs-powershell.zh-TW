---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ad44b9dcec002a76581a583eb75de430454f4d59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907497"
---
# <span data-ttu-id="f0944-101">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f0944-101">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="f0944-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0944-102">SYNOPSIS</span></span>
<span data-ttu-id="f0944-103">進行一或多個長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="f0944-103">Gets one or more long term retention backups.</span></span>

## <span data-ttu-id="f0944-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0944-104">SYNTAX</span></span>

### <span data-ttu-id="f0944-105">位置 (預設) </span><span class="sxs-lookup"><span data-stu-id="f0944-105">Location (Default)</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0944-106">ServerName</span><span class="sxs-lookup"><span data-stu-id="f0944-106">ServerName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> [-DatabaseName <String>]
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0944-107">BackupName</span><span class="sxs-lookup"><span data-stu-id="f0944-107">BackupName</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String> -DatabaseName <String>
 [-BackupName] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0944-108">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0944-108">GetBackupByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0944-109">GetBackupsByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0944-109">GetBackupsByResourceId</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0944-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0944-110">GetBackupByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-BackupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0944-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0944-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseModel> [-OnlyLatestPerDatabase]
 [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0944-112">描述</span><span class="sxs-lookup"><span data-stu-id="f0944-112">DESCRIPTION</span></span>
<span data-ttu-id="f0944-113">**Get-AzSqlDatabaseLongTermRetentionBackup** Cmdlet 會取得位置、伺服器或資料庫的所有長期保留備份，或取得特定的長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="f0944-113">The **Get-AzSqlDatabaseLongTermRetentionBackup** cmdlet gets all long term retention backups for a location, server, or database or gets a specific long term retention backup.</span></span>

## <span data-ttu-id="f0944-114">例子</span><span class="sxs-lookup"><span data-stu-id="f0944-114">EXAMPLES</span></span>

### <span data-ttu-id="f0944-115">範例 1：取得位置的所有備份</span><span class="sxs-lookup"><span data-stu-id="f0944-115">Example 1: Get all backups for a location</span></span>
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

<span data-ttu-id="f0944-116">此命令會針對所有資料庫進行所有長期保留備份 (這些資料庫在 northeurope 中可能為) ，只有在伺服器為線上時，資源群組才能設定。</span><span class="sxs-lookup"><span data-stu-id="f0944-116">This command gets all long term retention backups for all databases (which may be alive or deleted) in northeurope, resource group will be set only if server is live.</span></span>

### <span data-ttu-id="f0944-117">範例 2：取得資源群組下位置的所有備份</span><span class="sxs-lookup"><span data-stu-id="f0944-117">Example 2: Get all backups for a location under a resource group</span></span>
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

<span data-ttu-id="f0944-118">此命令會針對所有資料庫檔案 (保留備份，這些資料庫在 northeurope) 資源群組下可能為活動狀態或刪除。</span><span class="sxs-lookup"><span data-stu-id="f0944-118">This command gets all long term retention backups for all databases (which may be alive or deleted) under a resource group in northeurope.</span></span>

### <span data-ttu-id="f0944-119">範例 3：取得特定的長期保留備份</span><span class="sxs-lookup"><span data-stu-id="f0944-119">Example 3: Get a specific long term retention backup</span></span>
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

<span data-ttu-id="f0944-120">此命令會以名稱 601061b7-d10b-46e0-bf77-a2bfb16a6add;1316556655000000</span><span class="sxs-lookup"><span data-stu-id="f0944-120">This command gets the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="f0944-121">範例 4：取得資料庫的所有長期保留備份</span><span class="sxs-lookup"><span data-stu-id="f0944-121">Example 4: Get all long term retention backups for a database</span></span>
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

<span data-ttu-id="f0944-122">此命令會針對資料庫進行所有長期保留備份</span><span class="sxs-lookup"><span data-stu-id="f0944-122">This command gets all long term retention backups for database01</span></span>

### <span data-ttu-id="f0944-123">範例 5：使用篩選取得長期保留備份</span><span class="sxs-lookup"><span data-stu-id="f0944-123">Example 5: Get long term retention backups using filtering</span></span>
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

<span data-ttu-id="f0944-124">此命令會以名稱開頭為 "601061b7" 的所有備份</span><span class="sxs-lookup"><span data-stu-id="f0944-124">This command gets all backups with name that starts with "601061b7"</span></span>

## <span data-ttu-id="f0944-125">參數</span><span class="sxs-lookup"><span data-stu-id="f0944-125">PARAMETERS</span></span>

### <span data-ttu-id="f0944-126">-BackupName</span><span class="sxs-lookup"><span data-stu-id="f0944-126">-BackupName</span></span>
<span data-ttu-id="f0944-127">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0944-127">The name of the backup.</span></span>

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

### <span data-ttu-id="f0944-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f0944-128">-DatabaseName</span></span>
<span data-ttu-id="f0944-129">備份的 Azure SQL 資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f0944-129">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="f0944-130">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="f0944-130">-DatabaseState</span></span>
<span data-ttu-id="f0944-131">您想要尋找其備份、活動、已刪除或全部的資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="f0944-131">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="f0944-132">預設值為全部</span><span class="sxs-lookup"><span data-stu-id="f0944-132">Defaults to All</span></span>

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

### <span data-ttu-id="f0944-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0944-133">-DefaultProfile</span></span>
<span data-ttu-id="f0944-134">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0944-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0944-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0944-135">-InputObject</span></span>
<span data-ttu-id="f0944-136">要取得備份的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="f0944-136">The database object to get backups for.</span></span>

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

### <span data-ttu-id="f0944-137">-位置</span><span class="sxs-lookup"><span data-stu-id="f0944-137">-Location</span></span>
<span data-ttu-id="f0944-138">備份來源伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="f0944-138">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="f0944-139">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="f0944-139">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="f0944-140">是否只取得每個資料庫的最新備份。</span><span class="sxs-lookup"><span data-stu-id="f0944-140">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="f0944-141">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="f0944-141">Defaults to false.</span></span>

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

### <span data-ttu-id="f0944-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0944-142">-ResourceGroupName</span></span>
<span data-ttu-id="f0944-143">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0944-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="f0944-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0944-144">-ResourceId</span></span>
<span data-ttu-id="f0944-145">要取得備份的資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0944-145">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="f0944-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f0944-146">-ServerName</span></span>
<span data-ttu-id="f0944-147">備份的 Azure SQL Server 名稱在</span><span class="sxs-lookup"><span data-stu-id="f0944-147">The name of the Azure SQL Server the backups are under.</span></span>

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

### <span data-ttu-id="f0944-148">-確認</span><span class="sxs-lookup"><span data-stu-id="f0944-148">-Confirm</span></span>
<span data-ttu-id="f0944-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f0944-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0944-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0944-150">-WhatIf</span></span>
<span data-ttu-id="f0944-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0944-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0944-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0944-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0944-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0944-153">CommonParameters</span></span>
<span data-ttu-id="f0944-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0944-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0944-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0944-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0944-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f0944-156">INPUTS</span></span>

### <span data-ttu-id="f0944-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f0944-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="f0944-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f0944-158">System.String</span></span>

## <span data-ttu-id="f0944-159">輸出</span><span class="sxs-lookup"><span data-stu-id="f0944-159">OUTPUTS</span></span>

### <span data-ttu-id="f0944-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="f0944-160">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="f0944-161">筆記</span><span class="sxs-lookup"><span data-stu-id="f0944-161">NOTES</span></span>

## <span data-ttu-id="f0944-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0944-162">RELATED LINKS</span></span>

[<span data-ttu-id="f0944-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f0944-163">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f0944-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f0944-164">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f0944-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f0944-165">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f0944-166">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="f0944-166">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)