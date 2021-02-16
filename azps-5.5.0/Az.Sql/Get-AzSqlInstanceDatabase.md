---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133062"
---
# <span data-ttu-id="3fd14-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3fd14-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="3fd14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fd14-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd14-103">傳回有關 Azure SQL Managed 實例資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="3fd14-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="3fd14-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fd14-104">SYNTAX</span></span>

### <span data-ttu-id="3fd14-105">GetInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="3fd14-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fd14-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd14-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fd14-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="3fd14-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd14-108">說明</span><span class="sxs-lookup"><span data-stu-id="3fd14-108">DESCRIPTION</span></span>
<span data-ttu-id="3fd14-109">**AzSqlInstanceDatabase** Cmdlet 會從 Azure Sql Database Managed 實例取得一個或多個 azure sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="3fd14-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3fd14-110">示例</span><span class="sxs-lookup"><span data-stu-id="3fd14-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd14-111">範例1：取得實例上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="3fd14-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="3fd14-112">這個命令會取得實例名為 managedInstance1 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="3fd14-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="3fd14-113">範例2：依名稱在受管理的實例上取得資料庫</span><span class="sxs-lookup"><span data-stu-id="3fd14-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="3fd14-114">這個命令會從名為 managedInstance1 的實例取得名為 managedDatabase1 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3fd14-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="3fd14-115">範例3：使用篩選取得實例上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="3fd14-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="3fd14-116">這個命令會取得名為 managedInstance1 的實例上以 "managedDatabase" 為開頭的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="3fd14-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="3fd14-117">參數</span><span class="sxs-lookup"><span data-stu-id="3fd14-117">PARAMETERS</span></span>

### <span data-ttu-id="3fd14-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd14-118">-DefaultProfile</span></span>
<span data-ttu-id="3fd14-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fd14-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd14-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3fd14-120">-InstanceName</span></span>
<span data-ttu-id="3fd14-121">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="3fd14-121">The instance name.</span></span>

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

### <span data-ttu-id="3fd14-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="3fd14-122">-InstanceObject</span></span>
<span data-ttu-id="3fd14-123">要用來取得實例資料庫的實例物件</span><span class="sxs-lookup"><span data-stu-id="3fd14-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="3fd14-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd14-124">-InstanceResourceId</span></span>
<span data-ttu-id="3fd14-125">要取得之實例物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3fd14-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="3fd14-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fd14-126">-Name</span></span>
<span data-ttu-id="3fd14-127">要檢索之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fd14-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

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

### <span data-ttu-id="3fd14-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd14-128">-ResourceGroupName</span></span>
<span data-ttu-id="3fd14-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fd14-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="3fd14-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd14-130">CommonParameters</span></span>
<span data-ttu-id="3fd14-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fd14-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd14-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3fd14-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd14-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3fd14-133">INPUTS</span></span>

### <span data-ttu-id="3fd14-134">System.object</span><span class="sxs-lookup"><span data-stu-id="3fd14-134">System.String</span></span>

### <span data-ttu-id="3fd14-135">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="3fd14-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3fd14-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3fd14-136">OUTPUTS</span></span>

### <span data-ttu-id="3fd14-137">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="3fd14-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3fd14-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3fd14-138">NOTES</span></span>

## <span data-ttu-id="3fd14-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fd14-139">RELATED LINKS</span></span>
