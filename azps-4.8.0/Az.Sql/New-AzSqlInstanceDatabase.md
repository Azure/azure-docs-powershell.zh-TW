---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970090"
---
# <span data-ttu-id="70c62-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="70c62-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="70c62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70c62-102">SYNOPSIS</span></span>
<span data-ttu-id="70c62-103">建立 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="70c62-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="70c62-104">句法</span><span class="sxs-lookup"><span data-stu-id="70c62-104">SYNTAX</span></span>

### <span data-ttu-id="70c62-105">CreateNewInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="70c62-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c62-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="70c62-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c62-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="70c62-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70c62-108">說明</span><span class="sxs-lookup"><span data-stu-id="70c62-108">DESCRIPTION</span></span>
<span data-ttu-id="70c62-109">**新的-AzSqlInstanceDatabase** Cmdlet 會建立 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="70c62-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="70c62-110">示例</span><span class="sxs-lookup"><span data-stu-id="70c62-110">EXAMPLES</span></span>

### <span data-ttu-id="70c62-111">範例1：在指定的實例上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="70c62-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
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

<span data-ttu-id="70c62-112">這個命令會在 instance managedInstance1 上建立名為 Database01 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="70c62-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="70c62-113">參數</span><span class="sxs-lookup"><span data-stu-id="70c62-113">PARAMETERS</span></span>

### <span data-ttu-id="70c62-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70c62-114">-AsJob</span></span>
<span data-ttu-id="70c62-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70c62-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-116">-排序規則</span><span class="sxs-lookup"><span data-stu-id="70c62-116">-Collation</span></span>
<span data-ttu-id="70c62-117">要使用之 Azure SQL 實例資料庫排序規則的排序規則。</span><span class="sxs-lookup"><span data-stu-id="70c62-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c62-118">-DefaultProfile</span></span>
<span data-ttu-id="70c62-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70c62-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c62-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="70c62-120">-InstanceName</span></span>
<span data-ttu-id="70c62-121">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="70c62-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="70c62-122">-InstanceObject</span></span>
<span data-ttu-id="70c62-123">實例物件</span><span class="sxs-lookup"><span data-stu-id="70c62-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="70c62-124">-InstanceResourceId</span></span>
<span data-ttu-id="70c62-125">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="70c62-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="70c62-126">-Name</span></span>
<span data-ttu-id="70c62-127">要建立之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c62-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c62-128">-ResourceGroupName</span></span>
<span data-ttu-id="70c62-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c62-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="70c62-130">-Tag</span></span>
<span data-ttu-id="70c62-131">要與 Azure Sql 實例資料庫建立關聯的標籤</span><span class="sxs-lookup"><span data-stu-id="70c62-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c62-132">-確認</span><span class="sxs-lookup"><span data-stu-id="70c62-132">-Confirm</span></span>
<span data-ttu-id="70c62-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70c62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c62-134">-WhatIf</span></span>
<span data-ttu-id="70c62-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70c62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c62-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70c62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c62-137">CommonParameters</span></span>
<span data-ttu-id="70c62-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70c62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c62-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70c62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c62-140">輸入</span><span class="sxs-lookup"><span data-stu-id="70c62-140">INPUTS</span></span>

### <span data-ttu-id="70c62-141">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="70c62-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="70c62-142">System.object</span><span class="sxs-lookup"><span data-stu-id="70c62-142">System.String</span></span>

## <span data-ttu-id="70c62-143">輸出</span><span class="sxs-lookup"><span data-stu-id="70c62-143">OUTPUTS</span></span>

### <span data-ttu-id="70c62-144">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="70c62-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="70c62-145">筆記</span><span class="sxs-lookup"><span data-stu-id="70c62-145">NOTES</span></span>

## <span data-ttu-id="70c62-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="70c62-146">RELATED LINKS</span></span>
