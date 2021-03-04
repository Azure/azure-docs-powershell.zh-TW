---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: 158ae87c636f0ecf8b8c78d2a6d380640ff49677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906930"
---
# <span data-ttu-id="2c4bc-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2c4bc-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="2c4bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4bc-103">建立新的 Azure 資料庫移移服務專案。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="2c4bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c4bc-104">SYNTAX</span></span>

### <span data-ttu-id="2c4bc-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2c4bc-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4bc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c4bc-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4bc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c4bc-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c4bc-108">描述</span><span class="sxs-lookup"><span data-stu-id="2c4bc-108">DESCRIPTION</span></span>
<span data-ttu-id="2c4bc-109">此New-AzDataMigrationProject Cmdlet 會建立一個新的 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="2c4bc-110">此 Cmdlet 會採用所有必要的參數，例如 Azure 資源組的名稱、要建立新專案的 Azure 資料移轉服務名稱、要建立專案的區域、新專案的唯一名稱、來源和目標連線物件，以及目標型別物件，做為要移轉之資料庫清單的輸入。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="2c4bc-111">使用 New-AzDataMigrationConnectionInfo Cmdlet 為來源和目標連結建立新 ConnectionInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="2c4bc-112">Microsoft.Azure.management.DataMigration.Models.DatabaseInfo 清單預計適用于所選資料庫;此物件可以使用 Cmdlet New-AzDataMigrationDatabaseInfo建立。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="2c4bc-113">例子</span><span class="sxs-lookup"><span data-stu-id="2c4bc-113">EXAMPLES</span></span>

### <span data-ttu-id="2c4bc-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c4bc-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="2c4bc-115">上述範例顯示如何建立名為 MyDMSProject 的新專案，位於美國中地區，名為 TestService 的 Azure 資料庫移移服務實例下。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="2c4bc-116">參數</span><span class="sxs-lookup"><span data-stu-id="2c4bc-116">PARAMETERS</span></span>

### <span data-ttu-id="2c4bc-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2c4bc-117">-DatabaseInfo</span></span>
<span data-ttu-id="2c4bc-118">資料庫資訊。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4bc-119">-DefaultProfile</span></span>
<span data-ttu-id="2c4bc-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c4bc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c4bc-121">-InputObject</span></span>
<span data-ttu-id="2c4bc-122">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-123">-位置</span><span class="sxs-lookup"><span data-stu-id="2c4bc-123">-Location</span></span>
<span data-ttu-id="2c4bc-124">Azure 資料庫移移服務實例的位置。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c4bc-125">-Name</span></span>
<span data-ttu-id="2c4bc-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c4bc-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4bc-129">-ResourceId</span></span>
<span data-ttu-id="2c4bc-130">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2c4bc-131">-ServiceName</span></span>
<span data-ttu-id="2c4bc-132">Azure 資料庫移移服務實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="2c4bc-133">-SourceConnection</span></span>
<span data-ttu-id="2c4bc-134">來源連接資訊。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="2c4bc-135">-SourceType</span></span>
<span data-ttu-id="2c4bc-136">專案的來源平臺類型。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="2c4bc-137">-TargetConnection</span></span>
<span data-ttu-id="2c4bc-138">目標連接資訊。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="2c4bc-139">-TargetType</span></span>
<span data-ttu-id="2c4bc-140">專案的目標平臺類型。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4bc-141">-確認</span><span class="sxs-lookup"><span data-stu-id="2c4bc-141">-Confirm</span></span>
<span data-ttu-id="2c4bc-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4bc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4bc-143">-WhatIf</span></span>
<span data-ttu-id="2c4bc-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c4bc-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4bc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4bc-146">CommonParameters</span></span>
<span data-ttu-id="2c4bc-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4bc-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2c4bc-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4bc-149">輸入</span><span class="sxs-lookup"><span data-stu-id="2c4bc-149">INPUTS</span></span>

### <span data-ttu-id="2c4bc-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2c4bc-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="2c4bc-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2c4bc-151">System.String</span></span>

## <span data-ttu-id="2c4bc-152">輸出</span><span class="sxs-lookup"><span data-stu-id="2c4bc-152">OUTPUTS</span></span>

### <span data-ttu-id="2c4bc-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="2c4bc-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="2c4bc-154">筆記</span><span class="sxs-lookup"><span data-stu-id="2c4bc-154">NOTES</span></span>

## <span data-ttu-id="2c4bc-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c4bc-155">RELATED LINKS</span></span>
