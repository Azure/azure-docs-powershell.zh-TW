---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: ccd716b493640afef7b5adea0b2e834c10893c3c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437100"
---
# <span data-ttu-id="04afe-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="04afe-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="04afe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04afe-102">SYNOPSIS</span></span>
<span data-ttu-id="04afe-103">取得 (s) 的長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="04afe-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="04afe-104">句法</span><span class="sxs-lookup"><span data-stu-id="04afe-104">SYNTAX</span></span>

### <span data-ttu-id="04afe-105">預設)  (位置</span><span class="sxs-lookup"><span data-stu-id="04afe-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afe-106">實例</span><span class="sxs-lookup"><span data-stu-id="04afe-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afe-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04afe-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afe-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="04afe-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afe-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="04afe-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afe-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="04afe-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afe-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="04afe-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04afe-112">說明</span><span class="sxs-lookup"><span data-stu-id="04afe-112">DESCRIPTION</span></span>
<span data-ttu-id="04afe-113">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="04afe-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="04afe-114">示例</span><span class="sxs-lookup"><span data-stu-id="04afe-114">EXAMPLES</span></span>

### <span data-ttu-id="04afe-115">範例1</span><span class="sxs-lookup"><span data-stu-id="04afe-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="04afe-116">針對特定資料庫取得所有長字保留期間備份。</span><span class="sxs-lookup"><span data-stu-id="04afe-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="04afe-117">[資源群組] 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="04afe-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="04afe-118">參數</span><span class="sxs-lookup"><span data-stu-id="04afe-118">PARAMETERS</span></span>

### <span data-ttu-id="04afe-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="04afe-119">-BackupName</span></span>
<span data-ttu-id="04afe-120">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="04afe-120">The name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="04afe-121">-DatabaseName</span></span>
<span data-ttu-id="04afe-122">備份所在之受管理資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="04afe-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="04afe-123">-DatabaseState</span></span>
<span data-ttu-id="04afe-124">您想要尋找、[活]、[刪除] 或 [全部] 備份之資料庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="04afe-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="04afe-125">預設為 [全部]</span><span class="sxs-lookup"><span data-stu-id="04afe-125">Defaults to All</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04afe-126">-DefaultProfile</span></span>
<span data-ttu-id="04afe-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04afe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04afe-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04afe-128">-InputObject</span></span>
<span data-ttu-id="04afe-129">要取得備份的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="04afe-129">The database object to get backups for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="04afe-130">-InstanceName</span></span>
<span data-ttu-id="04afe-131">備份所在之受管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="04afe-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: System.String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-132">-位置</span><span class="sxs-lookup"><span data-stu-id="04afe-132">-Location</span></span>
<span data-ttu-id="04afe-133">備份來源管理實例的位置。</span><span class="sxs-lookup"><span data-stu-id="04afe-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="04afe-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="04afe-135">是否只取得每個資料庫的最新備份。</span><span class="sxs-lookup"><span data-stu-id="04afe-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="04afe-136">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="04afe-136">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04afe-137">-ResourceGroupName</span></span>
<span data-ttu-id="04afe-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04afe-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04afe-139">-ResourceId</span></span>
<span data-ttu-id="04afe-140">要取得備份的資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="04afe-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-141">-確認</span><span class="sxs-lookup"><span data-stu-id="04afe-141">-Confirm</span></span>
<span data-ttu-id="04afe-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04afe-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04afe-143">-WhatIf</span></span>
<span data-ttu-id="04afe-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04afe-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04afe-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04afe-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04afe-146">CommonParameters</span></span>
<span data-ttu-id="04afe-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04afe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04afe-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04afe-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04afe-149">輸入</span><span class="sxs-lookup"><span data-stu-id="04afe-149">INPUTS</span></span>

### <span data-ttu-id="04afe-150">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="04afe-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="04afe-151">System.object</span><span class="sxs-lookup"><span data-stu-id="04afe-151">System.String</span></span>

## <span data-ttu-id="04afe-152">輸出</span><span class="sxs-lookup"><span data-stu-id="04afe-152">OUTPUTS</span></span>

### <span data-ttu-id="04afe-153">AzureSqlManagedDatabaseLongTermRetentionBackupModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="04afe-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="04afe-154">筆記</span><span class="sxs-lookup"><span data-stu-id="04afe-154">NOTES</span></span>

## <span data-ttu-id="04afe-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="04afe-155">RELATED LINKS</span></span>

[<span data-ttu-id="04afe-156">移除-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="04afe-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="04afe-157">AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04afe-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="04afe-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="04afe-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="04afe-159">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="04afe-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)