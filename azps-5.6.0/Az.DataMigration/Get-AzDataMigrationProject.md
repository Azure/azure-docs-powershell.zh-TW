---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 5485693da87dbbb49b5e06e221e818de9bd222d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913214"
---
# <span data-ttu-id="d9cec-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="d9cec-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="d9cec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9cec-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cec-103">會取回 Azure 資料庫移移專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9cec-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="d9cec-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9cec-104">SYNTAX</span></span>

### <span data-ttu-id="d9cec-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d9cec-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cec-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cec-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cec-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9cec-108">描述</span><span class="sxs-lookup"><span data-stu-id="d9cec-108">DESCRIPTION</span></span>
<span data-ttu-id="d9cec-109">此Get-AzDataMigrationProject Cmdlet 會取回 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9cec-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="d9cec-110">例子</span><span class="sxs-lookup"><span data-stu-id="d9cec-110">EXAMPLES</span></span>

### <span data-ttu-id="d9cec-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d9cec-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="d9cec-112">上述範例會從名為 testResourceGroup 且受服務稱為 testService 的資源群組中，取用名為 TestProject 的 Azure 資料庫移移專案</span><span class="sxs-lookup"><span data-stu-id="d9cec-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="d9cec-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="d9cec-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="d9cec-114">上述範例會根據傳遞的 PSProject 物件輸入參數，來取回 Azure 資料庫移轉專案。</span><span class="sxs-lookup"><span data-stu-id="d9cec-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="d9cec-115">參數</span><span class="sxs-lookup"><span data-stu-id="d9cec-115">PARAMETERS</span></span>

### <span data-ttu-id="d9cec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cec-116">-DefaultProfile</span></span>
<span data-ttu-id="d9cec-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9cec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9cec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9cec-118">-InputObject</span></span>
<span data-ttu-id="d9cec-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="d9cec-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="d9cec-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9cec-120">-Name</span></span>
<span data-ttu-id="d9cec-121">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="d9cec-121">The name of the project.</span></span>

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

### <span data-ttu-id="d9cec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9cec-122">-ResourceGroupName</span></span>
<span data-ttu-id="d9cec-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9cec-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9cec-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9cec-124">-ResourceId</span></span>
<span data-ttu-id="d9cec-125">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9cec-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="d9cec-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d9cec-126">-ServiceName</span></span>
<span data-ttu-id="d9cec-127">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d9cec-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="d9cec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cec-128">CommonParameters</span></span>
<span data-ttu-id="d9cec-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9cec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cec-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d9cec-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cec-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d9cec-131">INPUTS</span></span>

### <span data-ttu-id="d9cec-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d9cec-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="d9cec-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d9cec-133">System.String</span></span>

## <span data-ttu-id="d9cec-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d9cec-134">OUTPUTS</span></span>

### <span data-ttu-id="d9cec-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="d9cec-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="d9cec-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d9cec-136">NOTES</span></span>

## <span data-ttu-id="d9cec-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9cec-137">RELATED LINKS</span></span>
