---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: be2e9342407cea6ba3da0bf239ee73e7b726dd82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959137"
---
# <span data-ttu-id="8548f-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8548f-101">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="8548f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8548f-102">SYNOPSIS</span></span>
<span data-ttu-id="8548f-103">刪除長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="8548f-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="8548f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8548f-104">SYNTAX</span></span>

### <span data-ttu-id="8548f-105">RemoveBackupDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="8548f-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8548f-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="8548f-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8548f-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="8548f-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8548f-108">說明</span><span class="sxs-lookup"><span data-stu-id="8548f-108">DESCRIPTION</span></span>
<span data-ttu-id="8548f-109">**AzSqlDatabaseLongTermRetentionBackup** Cmdlet 會刪除指定的備份。</span><span class="sxs-lookup"><span data-stu-id="8548f-109">The **Remove-AzSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="8548f-110">示例</span><span class="sxs-lookup"><span data-stu-id="8548f-110">EXAMPLES</span></span>

### <span data-ttu-id="8548f-111">範例1：使用資源群組刪除單一備份</span><span class="sxs-lookup"><span data-stu-id="8548f-111">Example 1: Delete a single backup with resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000" -ResourceGrouName resourcegroup01


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

<span data-ttu-id="8548f-112">刪除名稱為601061b7-d10b-46e0-bf77-a2bfb16a6add 的備份; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="8548f-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8548f-113">範例2：刪除不含資源群組的單一備份</span><span class="sxs-lookup"><span data-stu-id="8548f-113">Example 2: Delete a single backup without resource group</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server02 -DatabaseName database02 -BackupName "55970792-164c-4a4a-88e5-7158d092d503;131656309980000000"


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

<span data-ttu-id="8548f-114">刪除名稱為601061b7-d10b-46e0-bf77-a2bfb16a6add 的備份; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="8548f-114">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="8548f-115">範例3：刪除某個位置的所有備份</span><span class="sxs-lookup"><span data-stu-id="8548f-115">Example 3: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzSqlDatabaseLongTermRetentionBackup


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

<span data-ttu-id="8548f-116">這個命令會刪除 northeurope 位置的所有長時間保留備份。</span><span class="sxs-lookup"><span data-stu-id="8548f-116">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="8548f-117">參數</span><span class="sxs-lookup"><span data-stu-id="8548f-117">PARAMETERS</span></span>

### <span data-ttu-id="8548f-118">-BackupName</span><span class="sxs-lookup"><span data-stu-id="8548f-118">-BackupName</span></span>
<span data-ttu-id="8548f-119">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="8548f-119">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8548f-120">-DatabaseName</span></span>
<span data-ttu-id="8548f-121">備份所在之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8548f-121">The name of the Azure SQL Database the backup is from.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8548f-122">-DefaultProfile</span></span>
<span data-ttu-id="8548f-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8548f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8548f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8548f-124">-Force</span></span>
<span data-ttu-id="8548f-125">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="8548f-125">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8548f-126">-InputObject</span></span>
<span data-ttu-id="8548f-127">要移除的資料庫長期保留備份物件。</span><span class="sxs-lookup"><span data-stu-id="8548f-127">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-128">-位置</span><span class="sxs-lookup"><span data-stu-id="8548f-128">-Location</span></span>
<span data-ttu-id="8548f-129">備份源伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="8548f-129">The location of the backups' source server.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8548f-130">-ResourceGroupName</span></span>
<span data-ttu-id="8548f-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8548f-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8548f-132">-ResourceId</span></span>
<span data-ttu-id="8548f-133">要移除之 [長期保留] 備份的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8548f-133">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-134">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8548f-134">-ServerName</span></span>
<span data-ttu-id="8548f-135">備份所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8548f-135">The name of the Azure SQL Server the backup is under.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8548f-136">-確認</span><span class="sxs-lookup"><span data-stu-id="8548f-136">-Confirm</span></span>
<span data-ttu-id="8548f-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8548f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8548f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8548f-138">-WhatIf</span></span>
<span data-ttu-id="8548f-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8548f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8548f-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8548f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8548f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8548f-141">CommonParameters</span></span>
<span data-ttu-id="8548f-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8548f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8548f-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8548f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8548f-144">輸入</span><span class="sxs-lookup"><span data-stu-id="8548f-144">INPUTS</span></span>

### <span data-ttu-id="8548f-145">System.object</span><span class="sxs-lookup"><span data-stu-id="8548f-145">System.String</span></span>

## <span data-ttu-id="8548f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="8548f-146">OUTPUTS</span></span>

### <span data-ttu-id="8548f-147">AzureSqlDatabaseLongTermRetentionBackupModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="8548f-147">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="8548f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="8548f-148">NOTES</span></span>

## <span data-ttu-id="8548f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="8548f-149">RELATED LINKS</span></span>

[<span data-ttu-id="8548f-150">AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="8548f-150">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="8548f-151">AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8548f-151">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8548f-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8548f-152">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="8548f-153">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="8548f-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)