---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 19f73cf6f2d1906e9390f082bbce7e8000d48515
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614830"
---
# <span data-ttu-id="4cbef-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4cbef-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="4cbef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cbef-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbef-103">建立 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="4cbef-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="4cbef-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cbef-104">SYNTAX</span></span>

### <span data-ttu-id="4cbef-105">CreateNewInstanceDatabaseFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="4cbef-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbef-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="4cbef-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbef-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="4cbef-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cbef-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cbef-108">DESCRIPTION</span></span>
<span data-ttu-id="4cbef-109">**新的-AzSqlInstanceDatabase** Cmdlet 會建立 Azure SQL Managed 實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="4cbef-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="4cbef-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cbef-110">EXAMPLES</span></span>

### <span data-ttu-id="4cbef-111">範例1：在指定的實例上建立資料庫</span><span class="sxs-lookup"><span data-stu-id="4cbef-111">Example 1: Create a database on a specified instance</span></span>
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

<span data-ttu-id="4cbef-112">這個命令會在 instance managedInstance1 上建立名為 Database01 的實例資料庫。</span><span class="sxs-lookup"><span data-stu-id="4cbef-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="4cbef-113">參數</span><span class="sxs-lookup"><span data-stu-id="4cbef-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cbef-114">-AsJob</span></span>
<span data-ttu-id="4cbef-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4cbef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cbef-116">-排序規則</span><span class="sxs-lookup"><span data-stu-id="4cbef-116">-Collation</span></span>
<span data-ttu-id="4cbef-117">要使用之 Azure SQL 實例資料庫排序規則的排序規則。</span><span class="sxs-lookup"><span data-stu-id="4cbef-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="4cbef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbef-118">-DefaultProfile</span></span>
<span data-ttu-id="4cbef-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cbef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cbef-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4cbef-120">-InstanceName</span></span>
<span data-ttu-id="4cbef-121">實例名稱。</span><span class="sxs-lookup"><span data-stu-id="4cbef-121">The instance name.</span></span>

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

### <span data-ttu-id="4cbef-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="4cbef-122">-InstanceObject</span></span>
<span data-ttu-id="4cbef-123">實例物件</span><span class="sxs-lookup"><span data-stu-id="4cbef-123">The instance object</span></span>

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

### <span data-ttu-id="4cbef-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="4cbef-124">-InstanceResourceId</span></span>
<span data-ttu-id="4cbef-125">實例資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4cbef-125">The instance resource id</span></span>

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

### <span data-ttu-id="4cbef-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cbef-126">-Name</span></span>
<span data-ttu-id="4cbef-127">要建立之 Azure SQL 實例資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cbef-127">The name of the Azure SQL Instance Database to create.</span></span>

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

### <span data-ttu-id="4cbef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cbef-128">-ResourceGroupName</span></span>
<span data-ttu-id="4cbef-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cbef-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="4cbef-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cbef-130">-Tag</span></span>
<span data-ttu-id="4cbef-131">要與 Azure Sql 實例資料庫建立關聯的標籤</span><span class="sxs-lookup"><span data-stu-id="4cbef-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="4cbef-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4cbef-132">-Confirm</span></span>
<span data-ttu-id="4cbef-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cbef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbef-134">-WhatIf</span></span>
<span data-ttu-id="4cbef-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cbef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cbef-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cbef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbef-137">CommonParameters</span></span>
<span data-ttu-id="4cbef-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cbef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbef-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4cbef-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbef-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4cbef-140">INPUTS</span></span>

### <span data-ttu-id="4cbef-141">AzureSqlManagedInstanceModel 中的 [ManagedInstance]</span><span class="sxs-lookup"><span data-stu-id="4cbef-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="4cbef-142">System.object</span><span class="sxs-lookup"><span data-stu-id="4cbef-142">System.String</span></span>

## <span data-ttu-id="4cbef-143">輸出</span><span class="sxs-lookup"><span data-stu-id="4cbef-143">OUTPUTS</span></span>

### <span data-ttu-id="4cbef-144">AzureSqlManagedDatabaseModel 中的 [ManagedDatabase]</span><span class="sxs-lookup"><span data-stu-id="4cbef-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="4cbef-145">筆記</span><span class="sxs-lookup"><span data-stu-id="4cbef-145">NOTES</span></span>

## <span data-ttu-id="4cbef-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cbef-146">RELATED LINKS</span></span>