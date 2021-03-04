---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914321"
---
# <span data-ttu-id="78843-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="78843-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="78843-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78843-102">SYNOPSIS</span></span>
<span data-ttu-id="78843-103">會返回 Azure SQL Managed Instance 資料庫的重複備份相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78843-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="78843-104">語法</span><span class="sxs-lookup"><span data-stu-id="78843-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78843-105">描述</span><span class="sxs-lookup"><span data-stu-id="78843-105">DESCRIPTION</span></span>
<span data-ttu-id="78843-106">**Get-AzSqlInstanceDatabaseGeoBackup** Cmdlet 會從 Azure SQL Database Managed 實例取得一或多個 Azure SQL 資料庫的重複備份。</span><span class="sxs-lookup"><span data-stu-id="78843-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="78843-107">例子</span><span class="sxs-lookup"><span data-stu-id="78843-107">EXAMPLES</span></span>

### <span data-ttu-id="78843-108">範例 1：取得實例上的所有資料庫重複備份</span><span class="sxs-lookup"><span data-stu-id="78843-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="78843-109">此命令會為 managedInstance1 實例上的所有資料庫重複備份。</span><span class="sxs-lookup"><span data-stu-id="78843-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="78843-110">範例 2：在 Managed 實例上根據名稱取得資料庫多餘的備份</span><span class="sxs-lookup"><span data-stu-id="78843-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="78843-111">此命令會從名為 managedInstance1 的實例獲得名為 managedDatabase1 的資料庫多餘的備份。</span><span class="sxs-lookup"><span data-stu-id="78843-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="78843-112">範例 3：使用篩選在實例上取得所有資料庫多餘的備份</span><span class="sxs-lookup"><span data-stu-id="78843-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="78843-113">此命令會獲得名為 managedInstance1 之實例上以 "managedDatabase" 做為開始的所有資料庫多餘的備份。</span><span class="sxs-lookup"><span data-stu-id="78843-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="78843-114">參數</span><span class="sxs-lookup"><span data-stu-id="78843-114">PARAMETERS</span></span>

### <span data-ttu-id="78843-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78843-115">-DefaultProfile</span></span>
<span data-ttu-id="78843-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78843-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78843-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="78843-117">-InstanceName</span></span>
<span data-ttu-id="78843-118">實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="78843-118">The name of the instance.</span></span>

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

### <span data-ttu-id="78843-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="78843-119">-Name</span></span>
<span data-ttu-id="78843-120">要取取的實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="78843-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78843-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78843-121">-ResourceGroupName</span></span>
<span data-ttu-id="78843-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78843-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78843-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78843-123">CommonParameters</span></span>
<span data-ttu-id="78843-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78843-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78843-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78843-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78843-126">輸入</span><span class="sxs-lookup"><span data-stu-id="78843-126">INPUTS</span></span>

### <span data-ttu-id="78843-127">沒有</span><span class="sxs-lookup"><span data-stu-id="78843-127">None</span></span>

## <span data-ttu-id="78843-128">輸出</span><span class="sxs-lookup"><span data-stu-id="78843-128">OUTPUTS</span></span>

### <span data-ttu-id="78843-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="78843-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="78843-130">筆記</span><span class="sxs-lookup"><span data-stu-id="78843-130">NOTES</span></span>

## <span data-ttu-id="78843-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="78843-131">RELATED LINKS</span></span>
