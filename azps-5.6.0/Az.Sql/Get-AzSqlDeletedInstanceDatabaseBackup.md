---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: 1d41e42b673eccc692c317f3e9d1d20c5551da4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914373"
---
# <span data-ttu-id="19c8c-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="19c8c-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="19c8c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="19c8c-103">獲得您可以還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="19c8c-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="19c8c-104">語法</span><span class="sxs-lookup"><span data-stu-id="19c8c-104">SYNTAX</span></span>

### <span data-ttu-id="19c8c-105">DeletedDatabaseList (預設) </span><span class="sxs-lookup"><span data-stu-id="19c8c-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19c8c-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="19c8c-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19c8c-107">描述</span><span class="sxs-lookup"><span data-stu-id="19c8c-107">DESCRIPTION</span></span>
<span data-ttu-id="19c8c-108">**Get-AzSqlDeletedInstanceDatabaseBackup** Cmdlet 會取得指定的已刪除 SQL Instance 資料庫備份，您可以還原或還原所有已刪除的備份。</span><span class="sxs-lookup"><span data-stu-id="19c8c-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="19c8c-109">Azure 上的 SQL 實例延伸資料庫服務也支援此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="19c8c-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="19c8c-110">例子</span><span class="sxs-lookup"><span data-stu-id="19c8c-110">EXAMPLES</span></span>

### <span data-ttu-id="19c8c-111">範例 1：在伺服器上取得所有已刪除的資料庫備份</span><span class="sxs-lookup"><span data-stu-id="19c8c-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="19c8c-112">此命令會在伺服器上獲得所有已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="19c8c-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="19c8c-113">範例 2：取得指定的已刪除資料庫備份</span><span class="sxs-lookup"><span data-stu-id="19c8c-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="19c8c-114">參數</span><span class="sxs-lookup"><span data-stu-id="19c8c-114">PARAMETERS</span></span>

### <span data-ttu-id="19c8c-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19c8c-115">-DatabaseName</span></span>
<span data-ttu-id="19c8c-116">要取回備份的 Azure SQL 實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="19c8c-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c8c-117">-DefaultProfile</span></span>
<span data-ttu-id="19c8c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="19c8c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c8c-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="19c8c-119">-DeletionDate</span></span>
<span data-ttu-id="19c8c-120">Azure SQL 實例資料庫的刪除日期，用於以毫秒精確度 (例如 2016-02-23T00：21：22.847Z) </span><span class="sxs-lookup"><span data-stu-id="19c8c-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8c-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="19c8c-121">-InstanceName</span></span>
<span data-ttu-id="19c8c-122">資料庫位於 Azure SQL Managed 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="19c8c-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="19c8c-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="19c8c-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c8c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c8c-125">CommonParameters</span></span>
<span data-ttu-id="19c8c-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19c8c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c8c-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19c8c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c8c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="19c8c-128">INPUTS</span></span>

### <span data-ttu-id="19c8c-129">沒有</span><span class="sxs-lookup"><span data-stu-id="19c8c-129">None</span></span>

## <span data-ttu-id="19c8c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="19c8c-130">OUTPUTS</span></span>

### <span data-ttu-id="19c8c-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="19c8c-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="19c8c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="19c8c-132">NOTES</span></span>

## <span data-ttu-id="19c8c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="19c8c-133">RELATED LINKS</span></span>
