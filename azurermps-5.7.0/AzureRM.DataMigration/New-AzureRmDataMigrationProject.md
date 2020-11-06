---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455424"
---
# <span data-ttu-id="e27ff-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="e27ff-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="e27ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e27ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e27ff-103">建立新的 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="e27ff-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e27ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="e27ff-104">SYNTAX</span></span>

### <span data-ttu-id="e27ff-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e27ff-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e27ff-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27ff-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e27ff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27ff-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e27ff-108">說明</span><span class="sxs-lookup"><span data-stu-id="e27ff-108">DESCRIPTION</span></span>
<span data-ttu-id="e27ff-109">New-AzureRmDataMigrationProject Cmdlet 會建立新的 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="e27ff-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="e27ff-110">這個 Cmdlet 會在所有必要的參數（例如 Azure 資源群組的名稱、要在其中建立新專案的 Azure 資料移轉服務的名稱、建立專案的區域、來源和目標連線物件）以及目標型別物件（作為要遷移之資料庫的清單輸入）中採用。</span><span class="sxs-lookup"><span data-stu-id="e27ff-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="e27ff-111">使用 New-AzureRmDataMigrationConnectionInfo Cmdlet 為來源和目標連線建立新的 ConnectionInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="e27ff-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="e27ff-112">所選資料庫的 DataMigration 應該是 DatabaseInfo 的清單，而您可以使用 New-AzureRmDataMigrationDatabaseInfo Cmdlet 來建立此物件。</span><span class="sxs-lookup"><span data-stu-id="e27ff-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="e27ff-113">示例</span><span class="sxs-lookup"><span data-stu-id="e27ff-113">EXAMPLES</span></span>

### <span data-ttu-id="e27ff-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e27ff-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="e27ff-115">上述範例示範如何在名為 TestService 的 Azure 資料庫移轉服務實例下，建立名為 MyDMSProject 的新專案。</span><span class="sxs-lookup"><span data-stu-id="e27ff-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="e27ff-116">參數</span><span class="sxs-lookup"><span data-stu-id="e27ff-116">PARAMETERS</span></span>

### <span data-ttu-id="e27ff-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e27ff-117">-Confirm</span></span>
<span data-ttu-id="e27ff-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e27ff-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="e27ff-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="e27ff-120">資料庫資訊</span><span class="sxs-lookup"><span data-stu-id="e27ff-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27ff-121">-DefaultProfile</span></span>
<span data-ttu-id="e27ff-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e27ff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e27ff-123">-位置</span><span class="sxs-lookup"><span data-stu-id="e27ff-123">-Location</span></span>
<span data-ttu-id="e27ff-124">Azure 資料庫移轉服務實例的位置。</span><span class="sxs-lookup"><span data-stu-id="e27ff-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-125">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="e27ff-125">-ProjectName</span></span>
<span data-ttu-id="e27ff-126">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="e27ff-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="e27ff-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e27ff-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e27ff-129">-ServiceName</span></span>
<span data-ttu-id="e27ff-130">Azure 資料庫移轉服務實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="e27ff-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="e27ff-131">-SourceConnection</span></span>
<span data-ttu-id="e27ff-132">來源連結資訊。</span><span class="sxs-lookup"><span data-stu-id="e27ff-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="e27ff-133">-SourceType</span></span>
<span data-ttu-id="e27ff-134">Project 的來源平臺類型。</span><span class="sxs-lookup"><span data-stu-id="e27ff-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="e27ff-135">-TargetConnection</span></span>
<span data-ttu-id="e27ff-136">目標連線資訊。</span><span class="sxs-lookup"><span data-stu-id="e27ff-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27ff-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="e27ff-137">-TargetType</span></span>
<span data-ttu-id="e27ff-138">Project 的目標平臺類型。</span><span class="sxs-lookup"><span data-stu-id="e27ff-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="e27ff-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e27ff-139">OUTPUTS</span></span>

### <span data-ttu-id="e27ff-140">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="e27ff-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="e27ff-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e27ff-141">NOTES</span></span>

## <span data-ttu-id="e27ff-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e27ff-142">RELATED LINKS</span></span>

