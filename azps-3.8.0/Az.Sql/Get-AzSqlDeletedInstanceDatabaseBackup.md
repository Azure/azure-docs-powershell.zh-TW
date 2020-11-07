---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: bee6bd373c6b9c67afa8c70385c397d9334b733e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957458"
---
# <span data-ttu-id="7f65a-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="7f65a-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="7f65a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f65a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f65a-103">取得您可以還原的已刪除資料庫。</span><span class="sxs-lookup"><span data-stu-id="7f65a-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="7f65a-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f65a-104">SYNTAX</span></span>

### <span data-ttu-id="7f65a-105">DeletedDatabaseList (預設) </span><span class="sxs-lookup"><span data-stu-id="7f65a-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f65a-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="7f65a-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f65a-107">說明</span><span class="sxs-lookup"><span data-stu-id="7f65a-107">DESCRIPTION</span></span>
<span data-ttu-id="7f65a-108">**AzSqlDeletedInstanceDatabaseBackup** Cmdlet 會取得您可以還原的指定已刪除 SQL 實例資料庫備份，或您可以還原的所有已刪除備份。</span><span class="sxs-lookup"><span data-stu-id="7f65a-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="7f65a-109">Azure 上的 SQL 實例延伸資料庫服務也支援這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f65a-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="7f65a-110">示例</span><span class="sxs-lookup"><span data-stu-id="7f65a-110">EXAMPLES</span></span>

### <span data-ttu-id="7f65a-111">範例1：在伺服器上取得所有已刪除的資料庫備份</span><span class="sxs-lookup"><span data-stu-id="7f65a-111">Example 1: Get all deleted database backups on a server</span></span>
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

<span data-ttu-id="7f65a-112">這個命令會在伺服器上取得所有已刪除的資料庫備份。</span><span class="sxs-lookup"><span data-stu-id="7f65a-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="7f65a-113">範例2：取得指定的已刪除資料庫備份</span><span class="sxs-lookup"><span data-stu-id="7f65a-113">Example 2: Get a specified deleted database backup</span></span>
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

## <span data-ttu-id="7f65a-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f65a-114">PARAMETERS</span></span>

### <span data-ttu-id="7f65a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7f65a-115">-DatabaseName</span></span>
<span data-ttu-id="7f65a-116">要為其檢索備份之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f65a-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="7f65a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f65a-117">-DefaultProfile</span></span>
<span data-ttu-id="7f65a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f65a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f65a-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="7f65a-119">-DeletionDate</span></span>
<span data-ttu-id="7f65a-120">要為其檢索備份的 Azure SQL 實例資料庫的刪除日期，以毫秒為單位 (（例如 2016-02-23T00：21： 22.847 Z) </span><span class="sxs-lookup"><span data-stu-id="7f65a-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="7f65a-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7f65a-121">-InstanceName</span></span>
<span data-ttu-id="7f65a-122">資料庫所在之 Azure SQL 託管實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f65a-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="7f65a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f65a-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f65a-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f65a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="7f65a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f65a-125">CommonParameters</span></span>
<span data-ttu-id="7f65a-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f65a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f65a-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f65a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f65a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7f65a-128">INPUTS</span></span>

### <span data-ttu-id="7f65a-129">所有</span><span class="sxs-lookup"><span data-stu-id="7f65a-129">None</span></span>

## <span data-ttu-id="7f65a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7f65a-130">OUTPUTS</span></span>

### <span data-ttu-id="7f65a-131">AzureSqlDeletedManagedDatabaseBackupModel 中的 [ManagedDatabaseBackup]</span><span class="sxs-lookup"><span data-stu-id="7f65a-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="7f65a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7f65a-132">NOTES</span></span>

## <span data-ttu-id="7f65a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f65a-133">RELATED LINKS</span></span>
