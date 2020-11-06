---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatalongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 68481d49fb37fb5246021fb8daa2d53a64b5c6b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450988"
---
# <span data-ttu-id="b82b9-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b82b9-101">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="b82b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b82b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b82b9-103">刪除長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="b82b9-103">Deletes a long term retention backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b82b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="b82b9-104">SYNTAX</span></span>

### <span data-ttu-id="b82b9-105">RemoveBackupDefault (預設) </span><span class="sxs-lookup"><span data-stu-id="b82b9-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-Location] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b82b9-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="b82b9-106">RemoveBackupByInputObject</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlDatabaseLongTermRetentionBackupModel>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b82b9-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="b82b9-107">RemoveBackupByResourceId</span></span>
```
Remove-AzureRmSqlDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b82b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="b82b9-108">DESCRIPTION</span></span>
<span data-ttu-id="b82b9-109">**AzureRmSqlDatabaseLongTermRetentionBackup** Cmdlet 會刪除指定的備份。</span><span class="sxs-lookup"><span data-stu-id="b82b9-109">The **Remove-AzureRmSqlDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="b82b9-110">示例</span><span class="sxs-lookup"><span data-stu-id="b82b9-110">EXAMPLES</span></span>

### <span data-ttu-id="b82b9-111">範例1：刪除單一備份</span><span class="sxs-lookup"><span data-stu-id="b82b9-111">Example 1: Delete a single backup</span></span>
```powershell
PS C:\> Remove-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope -ServerName server01 -DatabaseName database01 -BackupName "601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000"


BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="b82b9-112">刪除名稱為601061b7-d10b-46e0-bf77-a2bfb16a6add 的備份; 131655666550000000</span><span class="sxs-lookup"><span data-stu-id="b82b9-112">Deletes the backup with name 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000</span></span>

### <span data-ttu-id="b82b9-113">範例2：刪除某個位置的所有備份</span><span class="sxs-lookup"><span data-stu-id="b82b9-113">Example 2: Delete all backups for a location</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseLongTermRetentionBackup -Location northeurope | Remove-AzureRmSqlDatabaseLongTermRetentionBackup


BackupExpirationTime : 3/22/2018 11:43:18 PM
BackupName           : 55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
BackupTime           : 3/15/2018 11:43:18 PM
DatabaseName         : database02
DatabaseDeletionTime : 3/18/2018 4:36:00 PM
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server02/longTermRetentionDatabases/database02/longTermRetentionBackups/55970792-164c-4a4a-88e5-7158d092d503;131656309980000000
ServerName           : server02
ServerCreateTime     : 2/28/2018 12:12:19 AM

BackupExpirationTime : 3/22/2018 5:50:55 AM
BackupName           : 601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
BackupTime           : 3/15/2018 5:50:55 AM
DatabaseName         : database01
DatabaseDeletionTime :
Location         : northeurope
ResourceId           : /subscriptions/371edd6d-9630-4558-a7bd-ee139498e6a1/providers/Microsoft.Sql/locations/northeurope/longTermRetentionServers/server01/longTermRetentionDatabases/database01/longTermRetentionBackups/601061b7-d10b-46e0-bf77-a2bfb16a6add;131655666550000000
ServerName           : server01
ServerCreateTime     : 2/29/2018 12:12:19 AM
```

<span data-ttu-id="b82b9-114">這個命令會刪除 northeurope 位置的所有長時間保留備份。</span><span class="sxs-lookup"><span data-stu-id="b82b9-114">This command deletes all long term retention backups for the northeurope location.</span></span>

## <span data-ttu-id="b82b9-115">參數</span><span class="sxs-lookup"><span data-stu-id="b82b9-115">PARAMETERS</span></span>

### <span data-ttu-id="b82b9-116">-BackupName</span><span class="sxs-lookup"><span data-stu-id="b82b9-116">-BackupName</span></span>
<span data-ttu-id="b82b9-117">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="b82b9-117">The name of the backup.</span></span>

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

### <span data-ttu-id="b82b9-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b82b9-118">-DatabaseName</span></span>
<span data-ttu-id="b82b9-119">備份所在之 Azure SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b82b9-119">The name of the Azure SQL Database the backup is from.</span></span>

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

### <span data-ttu-id="b82b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82b9-120">-DefaultProfile</span></span>
<span data-ttu-id="b82b9-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b82b9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b82b9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b82b9-122">-Force</span></span>
<span data-ttu-id="b82b9-123">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="b82b9-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b82b9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b82b9-124">-InputObject</span></span>
<span data-ttu-id="b82b9-125">要移除的資料庫長期保留備份物件。</span><span class="sxs-lookup"><span data-stu-id="b82b9-125">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b82b9-126">-位置</span><span class="sxs-lookup"><span data-stu-id="b82b9-126">-Location</span></span>
<span data-ttu-id="b82b9-127">備份源伺服器的位置。</span><span class="sxs-lookup"><span data-stu-id="b82b9-127">The location of the backups' source server.</span></span>

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

### <span data-ttu-id="b82b9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b82b9-128">-ResourceId</span></span>
<span data-ttu-id="b82b9-129">要移除之 [長期保留] 備份的 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="b82b9-129">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

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

### <span data-ttu-id="b82b9-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b82b9-130">-ServerName</span></span>
<span data-ttu-id="b82b9-131">備份所在之 Azure SQL Server 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b82b9-131">The name of the Azure SQL Server the backup is under.</span></span>

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

### <span data-ttu-id="b82b9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b82b9-132">-Confirm</span></span>
<span data-ttu-id="b82b9-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b82b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b82b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b82b9-134">-WhatIf</span></span>
<span data-ttu-id="b82b9-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b82b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b82b9-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b82b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b82b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82b9-137">CommonParameters</span></span>
<span data-ttu-id="b82b9-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b82b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82b9-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b82b9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82b9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b82b9-140">INPUTS</span></span>

### <span data-ttu-id="b82b9-141">System.object</span><span class="sxs-lookup"><span data-stu-id="b82b9-141">System.String</span></span>

## <span data-ttu-id="b82b9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b82b9-142">OUTPUTS</span></span>

### <span data-ttu-id="b82b9-143">AzureSqlDatabaseLongTermRetentionBackupModel 中的 [.Sql]。</span><span class="sxs-lookup"><span data-stu-id="b82b9-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="b82b9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b82b9-144">NOTES</span></span>

## <span data-ttu-id="b82b9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b82b9-145">RELATED LINKS</span></span>

[<span data-ttu-id="b82b9-146">AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b82b9-146">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b82b9-147">AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b82b9-147">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b82b9-148">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b82b9-148">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b82b9-149">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b82b9-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)