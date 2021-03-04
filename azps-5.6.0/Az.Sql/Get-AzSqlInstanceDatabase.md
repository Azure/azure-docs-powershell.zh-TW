---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4385b231a5346af6b49ad3a74c6c984f2f94c416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914329"
---
# <span data-ttu-id="b6064-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="b6064-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="b6064-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6064-102">SYNOPSIS</span></span>
<span data-ttu-id="b6064-103">會返回 Azure SQL Managed 實例資料庫相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b6064-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="b6064-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6064-104">SYNTAX</span></span>

### <span data-ttu-id="b6064-105">GetInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="b6064-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6064-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b6064-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6064-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="b6064-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6064-108">描述</span><span class="sxs-lookup"><span data-stu-id="b6064-108">DESCRIPTION</span></span>
<span data-ttu-id="b6064-109">**Get-AzSqlInstanceDatabase** Cmdlet 會從 Azure SQL Database Managed 實例取得一或多個 Azure SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6064-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="b6064-110">例子</span><span class="sxs-lookup"><span data-stu-id="b6064-110">EXAMPLES</span></span>

### <span data-ttu-id="b6064-111">範例 1：取得實例上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="b6064-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="b6064-112">此命令會獲得名為 managedInstance1 的實例上的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6064-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="b6064-113">範例 2：在 Managed 實例上按名稱取得資料庫</span><span class="sxs-lookup"><span data-stu-id="b6064-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="b6064-114">此命令會從 managedInstance1 實例中，獲得名為 managedDatabase1 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6064-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="b6064-115">範例 3：使用篩選取得實例上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="b6064-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="b6064-116">此命令會獲得名為 managedInstance1 之實例上以 "managedDatabase" 做為開始的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6064-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="b6064-117">參數</span><span class="sxs-lookup"><span data-stu-id="b6064-117">PARAMETERS</span></span>

### <span data-ttu-id="b6064-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6064-118">-DefaultProfile</span></span>
<span data-ttu-id="b6064-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6064-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6064-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b6064-120">-InstanceName</span></span>
<span data-ttu-id="b6064-121">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="b6064-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6064-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="b6064-122">-InstanceObject</span></span>
<span data-ttu-id="b6064-123">要用於取得實例資料庫的實例物件</span><span class="sxs-lookup"><span data-stu-id="b6064-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6064-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="b6064-124">-InstanceResourceId</span></span>
<span data-ttu-id="b6064-125">要取得的實例物件資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b6064-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6064-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6064-126">-Name</span></span>
<span data-ttu-id="b6064-127">要取取的 Azure SQL 實例資料庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b6064-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6064-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6064-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6064-129">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6064-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6064-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6064-130">CommonParameters</span></span>
<span data-ttu-id="b6064-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6064-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6064-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6064-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6064-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b6064-133">INPUTS</span></span>

### <span data-ttu-id="b6064-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b6064-134">System.String</span></span>

### <span data-ttu-id="b6064-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b6064-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="b6064-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b6064-136">OUTPUTS</span></span>

### <span data-ttu-id="b6064-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b6064-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b6064-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b6064-138">NOTES</span></span>

## <span data-ttu-id="b6064-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6064-139">RELATED LINKS</span></span>
