---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448889"
---
# <span data-ttu-id="199c4-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="199c4-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="199c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="199c4-102">SYNOPSIS</span></span>
<span data-ttu-id="199c4-103">傳回有關 Azure SQL Managed 實例資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="199c4-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="199c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="199c4-104">SYNTAX</span></span>

### <span data-ttu-id="199c4-105">GetInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="199c4-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="199c4-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="199c4-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="199c4-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="199c4-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="199c4-108">說明</span><span class="sxs-lookup"><span data-stu-id="199c4-108">DESCRIPTION</span></span>
<span data-ttu-id="199c4-109">**AzureRmSqlInstanceDatabase** Cmdlet 會從 Azure Sql Database Managed 實例取得一個或多個 azure sql 資料庫。</span><span class="sxs-lookup"><span data-stu-id="199c4-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="199c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="199c4-110">EXAMPLES</span></span>

### <span data-ttu-id="199c4-111">範例1：取得實例上的所有資料庫</span><span class="sxs-lookup"><span data-stu-id="199c4-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="199c4-112">這個命令會取得實例名為 managedInstance1 的所有資料庫。</span><span class="sxs-lookup"><span data-stu-id="199c4-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="199c4-113">範例2：依名稱在受管理的實例上取得資料庫</span><span class="sxs-lookup"><span data-stu-id="199c4-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="199c4-114">這個命令會從名為 managedInstance1 的實例取得名為 managedDatabase1 的資料庫。</span><span class="sxs-lookup"><span data-stu-id="199c4-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="199c4-115">參數</span><span class="sxs-lookup"><span data-stu-id="199c4-115">PARAMETERS</span></span>

### <span data-ttu-id="199c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199c4-116">-DefaultProfile</span></span>
<span data-ttu-id="199c4-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="199c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199c4-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="199c4-118">-InstanceName</span></span>
<span data-ttu-id="199c4-119">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="199c4-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199c4-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="199c4-120">-InstanceObject</span></span>
<span data-ttu-id="199c4-121">要用來取得實例資料庫的實例物件</span><span class="sxs-lookup"><span data-stu-id="199c4-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="199c4-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="199c4-122">-InstanceResourceId</span></span>
<span data-ttu-id="199c4-123">要取得之實例物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="199c4-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="199c4-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="199c4-124">-Name</span></span>
<span data-ttu-id="199c4-125">要檢索之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="199c4-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="199c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="199c4-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="199c4-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199c4-128">CommonParameters</span></span>
<span data-ttu-id="199c4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="199c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199c4-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="199c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199c4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="199c4-131">INPUTS</span></span>

### <span data-ttu-id="199c4-132">System.object</span><span class="sxs-lookup"><span data-stu-id="199c4-132">System.String</span></span>
<span data-ttu-id="199c4-133">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="199c4-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="199c4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="199c4-134">OUTPUTS</span></span>

### <span data-ttu-id="199c4-135">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="199c4-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="199c4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="199c4-136">NOTES</span></span>

## <span data-ttu-id="199c4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="199c4-137">RELATED LINKS</span></span>
