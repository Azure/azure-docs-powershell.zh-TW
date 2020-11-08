---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796977"
---
# <span data-ttu-id="aedbf-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="aedbf-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="aedbf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aedbf-102">SYNOPSIS</span></span>
<span data-ttu-id="aedbf-103">建立新的 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="aedbf-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="aedbf-104">句法</span><span class="sxs-lookup"><span data-stu-id="aedbf-104">SYNTAX</span></span>

### <span data-ttu-id="aedbf-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aedbf-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aedbf-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aedbf-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aedbf-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aedbf-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aedbf-108">說明</span><span class="sxs-lookup"><span data-stu-id="aedbf-108">DESCRIPTION</span></span>
<span data-ttu-id="aedbf-109">New-AzDataMigrationProject Cmdlet 會建立新的 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="aedbf-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="aedbf-110">這個 Cmdlet 會在所有必要的參數（例如 Azure 資源群組的名稱、要在其中建立新專案的 Azure 資料移轉服務的名稱、建立專案的區域、來源和目標連線物件）以及目標型別物件（作為要遷移之資料庫的清單輸入）中採用。</span><span class="sxs-lookup"><span data-stu-id="aedbf-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="aedbf-111">使用 New-AzDataMigrationConnectionInfo Cmdlet 為來源和目標連線建立新的 ConnectionInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="aedbf-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="aedbf-112">所選資料庫的 DataMigration 應該是 DatabaseInfo 的清單，而您可以使用 New-AzDataMigrationDatabaseInfo Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="aedbf-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="aedbf-113">示例</span><span class="sxs-lookup"><span data-stu-id="aedbf-113">EXAMPLES</span></span>

### <span data-ttu-id="aedbf-114">範例1</span><span class="sxs-lookup"><span data-stu-id="aedbf-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="aedbf-115">上述範例示範如何在名為 TestService 的 Azure 資料庫移轉服務實例下，建立名為 MyDMSProject 的新專案。</span><span class="sxs-lookup"><span data-stu-id="aedbf-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="aedbf-116">參數</span><span class="sxs-lookup"><span data-stu-id="aedbf-116">PARAMETERS</span></span>

### <span data-ttu-id="aedbf-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="aedbf-117">-DatabaseInfo</span></span>
<span data-ttu-id="aedbf-118">資料庫資料。</span><span class="sxs-lookup"><span data-stu-id="aedbf-118">Database Infos.</span></span>

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

### <span data-ttu-id="aedbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedbf-119">-DefaultProfile</span></span>
<span data-ttu-id="aedbf-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aedbf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aedbf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aedbf-121">-InputObject</span></span>
<span data-ttu-id="aedbf-122">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="aedbf-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="aedbf-123">-位置</span><span class="sxs-lookup"><span data-stu-id="aedbf-123">-Location</span></span>
<span data-ttu-id="aedbf-124">Azure 資料庫移轉服務實例的位置。</span><span class="sxs-lookup"><span data-stu-id="aedbf-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="aedbf-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="aedbf-125">-Name</span></span>
<span data-ttu-id="aedbf-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="aedbf-126">The name of the project.</span></span>

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

### <span data-ttu-id="aedbf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aedbf-127">-ResourceGroupName</span></span>
<span data-ttu-id="aedbf-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aedbf-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="aedbf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aedbf-129">-ResourceId</span></span>
<span data-ttu-id="aedbf-130">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="aedbf-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="aedbf-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aedbf-131">-ServiceName</span></span>
<span data-ttu-id="aedbf-132">Azure 資料庫移轉服務實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="aedbf-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="aedbf-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="aedbf-133">-SourceConnection</span></span>
<span data-ttu-id="aedbf-134">來源連結資訊。</span><span class="sxs-lookup"><span data-stu-id="aedbf-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="aedbf-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="aedbf-135">-SourceType</span></span>
<span data-ttu-id="aedbf-136">Project 的來源平臺類型。</span><span class="sxs-lookup"><span data-stu-id="aedbf-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="aedbf-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="aedbf-137">-TargetConnection</span></span>
<span data-ttu-id="aedbf-138">目標連線資訊。</span><span class="sxs-lookup"><span data-stu-id="aedbf-138">Target connection information.</span></span>

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

### <span data-ttu-id="aedbf-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="aedbf-139">-TargetType</span></span>
<span data-ttu-id="aedbf-140">Project 的目標平臺類型。</span><span class="sxs-lookup"><span data-stu-id="aedbf-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="aedbf-141">-確認</span><span class="sxs-lookup"><span data-stu-id="aedbf-141">-Confirm</span></span>
<span data-ttu-id="aedbf-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aedbf-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aedbf-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aedbf-143">-WhatIf</span></span>
<span data-ttu-id="aedbf-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aedbf-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aedbf-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aedbf-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aedbf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedbf-146">CommonParameters</span></span>
<span data-ttu-id="aedbf-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aedbf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedbf-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aedbf-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedbf-149">輸入</span><span class="sxs-lookup"><span data-stu-id="aedbf-149">INPUTS</span></span>

### <span data-ttu-id="aedbf-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="aedbf-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="aedbf-151">System.object</span><span class="sxs-lookup"><span data-stu-id="aedbf-151">System.String</span></span>

## <span data-ttu-id="aedbf-152">輸出</span><span class="sxs-lookup"><span data-stu-id="aedbf-152">OUTPUTS</span></span>

### <span data-ttu-id="aedbf-153">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="aedbf-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="aedbf-154">筆記</span><span class="sxs-lookup"><span data-stu-id="aedbf-154">NOTES</span></span>

## <span data-ttu-id="aedbf-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="aedbf-155">RELATED LINKS</span></span>