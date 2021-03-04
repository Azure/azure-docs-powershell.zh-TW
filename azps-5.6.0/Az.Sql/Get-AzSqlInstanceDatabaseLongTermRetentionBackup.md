---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 464334aa67be554a20c7d1b15e7d591a25979809
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907494"
---
# <span data-ttu-id="b068d-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b068d-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="b068d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b068d-102">SYNOPSIS</span></span>
<span data-ttu-id="b068d-103">獲得長期保留備份 (備份) 。</span><span class="sxs-lookup"><span data-stu-id="b068d-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="b068d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b068d-104">SYNTAX</span></span>

### <span data-ttu-id="b068d-105">位置 (預設) </span><span class="sxs-lookup"><span data-stu-id="b068d-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b068d-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="b068d-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b068d-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b068d-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b068d-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="b068d-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b068d-109">GetBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="b068d-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b068d-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="b068d-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b068d-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="b068d-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b068d-112">描述</span><span class="sxs-lookup"><span data-stu-id="b068d-112">DESCRIPTION</span></span>
<span data-ttu-id="b068d-113">{{ 填寫描述 }}</span><span class="sxs-lookup"><span data-stu-id="b068d-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="b068d-114">例子</span><span class="sxs-lookup"><span data-stu-id="b068d-114">EXAMPLES</span></span>

### <span data-ttu-id="b068d-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="b068d-115">Example 1</span></span>
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

<span data-ttu-id="b068d-116">為特定資料庫獲取所有長期保留備份。</span><span class="sxs-lookup"><span data-stu-id="b068d-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="b068d-117">資源群組為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b068d-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="b068d-118">參數</span><span class="sxs-lookup"><span data-stu-id="b068d-118">PARAMETERS</span></span>

### <span data-ttu-id="b068d-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="b068d-119">-BackupName</span></span>
<span data-ttu-id="b068d-120">備份的名稱。</span><span class="sxs-lookup"><span data-stu-id="b068d-120">The name of the backup.</span></span>

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

### <span data-ttu-id="b068d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b068d-121">-DatabaseName</span></span>
<span data-ttu-id="b068d-122">備份下的受管理資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b068d-122">The name of the Managed Database the backups are under.</span></span>

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

### <span data-ttu-id="b068d-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="b068d-123">-DatabaseState</span></span>
<span data-ttu-id="b068d-124">您想要尋找其備份、活動、已刪除或全部的資料庫狀態。</span><span class="sxs-lookup"><span data-stu-id="b068d-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="b068d-125">預設值為全部</span><span class="sxs-lookup"><span data-stu-id="b068d-125">Defaults to All</span></span>

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

### <span data-ttu-id="b068d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b068d-126">-DefaultProfile</span></span>
<span data-ttu-id="b068d-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b068d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b068d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b068d-128">-InputObject</span></span>
<span data-ttu-id="b068d-129">要取得備份的資料庫物件。</span><span class="sxs-lookup"><span data-stu-id="b068d-129">The database object to get backups for.</span></span>

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

### <span data-ttu-id="b068d-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b068d-130">-InstanceName</span></span>
<span data-ttu-id="b068d-131">備份下的受管理實例名稱。</span><span class="sxs-lookup"><span data-stu-id="b068d-131">The name of the Managed Instance the backups are under.</span></span>

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

### <span data-ttu-id="b068d-132">-位置</span><span class="sxs-lookup"><span data-stu-id="b068d-132">-Location</span></span>
<span data-ttu-id="b068d-133">備份來源受管理實例的位置。</span><span class="sxs-lookup"><span data-stu-id="b068d-133">The location of the backups' source Managed Instance.</span></span>

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

### <span data-ttu-id="b068d-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="b068d-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="b068d-135">是否只取得每個資料庫的最新備份。</span><span class="sxs-lookup"><span data-stu-id="b068d-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="b068d-136">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="b068d-136">Defaults to false.</span></span>

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

### <span data-ttu-id="b068d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b068d-137">-ResourceGroupName</span></span>
<span data-ttu-id="b068d-138">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b068d-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="b068d-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b068d-139">-ResourceId</span></span>
<span data-ttu-id="b068d-140">要取得備份的資料庫資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b068d-140">The database Resource ID to get backups for.</span></span>

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

### <span data-ttu-id="b068d-141">-確認</span><span class="sxs-lookup"><span data-stu-id="b068d-141">-Confirm</span></span>
<span data-ttu-id="b068d-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b068d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b068d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b068d-143">-WhatIf</span></span>
<span data-ttu-id="b068d-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b068d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b068d-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b068d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b068d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b068d-146">CommonParameters</span></span>
<span data-ttu-id="b068d-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b068d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b068d-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b068d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b068d-149">輸入</span><span class="sxs-lookup"><span data-stu-id="b068d-149">INPUTS</span></span>

### <span data-ttu-id="b068d-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b068d-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="b068d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="b068d-151">System.String</span></span>

## <span data-ttu-id="b068d-152">輸出</span><span class="sxs-lookup"><span data-stu-id="b068d-152">OUTPUTS</span></span>

### <span data-ttu-id="b068d-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="b068d-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="b068d-154">筆記</span><span class="sxs-lookup"><span data-stu-id="b068d-154">NOTES</span></span>

## <span data-ttu-id="b068d-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b068d-155">RELATED LINKS</span></span>

[<span data-ttu-id="b068d-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b068d-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b068d-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b068d-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b068d-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b068d-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b068d-159">SQL 資料庫檔</span><span class="sxs-lookup"><span data-stu-id="b068d-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)