---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141018"
---
# <span data-ttu-id="75f57-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="75f57-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="75f57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75f57-102">SYNOPSIS</span></span>
<span data-ttu-id="75f57-103">檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="75f57-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="75f57-104">句法</span><span class="sxs-lookup"><span data-stu-id="75f57-104">SYNTAX</span></span>

### <span data-ttu-id="75f57-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="75f57-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f57-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75f57-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f57-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75f57-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75f57-108">說明</span><span class="sxs-lookup"><span data-stu-id="75f57-108">DESCRIPTION</span></span>
<span data-ttu-id="75f57-109">Get-AzDataMigrationProject Cmdlet 會檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="75f57-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="75f57-110">示例</span><span class="sxs-lookup"><span data-stu-id="75f57-110">EXAMPLES</span></span>

### <span data-ttu-id="75f57-111">範例1</span><span class="sxs-lookup"><span data-stu-id="75f57-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="75f57-112">上述範例會在名為「testResourceGroup」的資源群組中檢索名為 TestProject 的 Azure 資料庫移轉專案，並在 [服務稱為 testService]</span><span class="sxs-lookup"><span data-stu-id="75f57-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="75f57-113">範例2</span><span class="sxs-lookup"><span data-stu-id="75f57-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="75f57-114">上述範例會根據傳入的 PSProject 物件輸入參數，來檢索 Azure Database 移植專案。</span><span class="sxs-lookup"><span data-stu-id="75f57-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="75f57-115">參數</span><span class="sxs-lookup"><span data-stu-id="75f57-115">PARAMETERS</span></span>

### <span data-ttu-id="75f57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f57-116">-DefaultProfile</span></span>
<span data-ttu-id="75f57-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75f57-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75f57-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75f57-118">-InputObject</span></span>
<span data-ttu-id="75f57-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="75f57-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="75f57-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="75f57-120">-Name</span></span>
<span data-ttu-id="75f57-121">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="75f57-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f57-122">-ResourceGroupName</span></span>
<span data-ttu-id="75f57-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75f57-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="75f57-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75f57-124">-ResourceId</span></span>
<span data-ttu-id="75f57-125">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="75f57-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="75f57-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="75f57-126">-ServiceName</span></span>
<span data-ttu-id="75f57-127">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="75f57-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="75f57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f57-128">CommonParameters</span></span>
<span data-ttu-id="75f57-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75f57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f57-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75f57-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f57-131">輸入</span><span class="sxs-lookup"><span data-stu-id="75f57-131">INPUTS</span></span>

### <span data-ttu-id="75f57-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="75f57-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="75f57-133">System.object</span><span class="sxs-lookup"><span data-stu-id="75f57-133">System.String</span></span>

## <span data-ttu-id="75f57-134">輸出</span><span class="sxs-lookup"><span data-stu-id="75f57-134">OUTPUTS</span></span>

### <span data-ttu-id="75f57-135">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="75f57-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="75f57-136">筆記</span><span class="sxs-lookup"><span data-stu-id="75f57-136">NOTES</span></span>

## <span data-ttu-id="75f57-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="75f57-137">RELATED LINKS</span></span>
