---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434766"
---
# <span data-ttu-id="78197-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="78197-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="78197-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78197-102">SYNOPSIS</span></span>
<span data-ttu-id="78197-103">檢索與 Azure Database 遷移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="78197-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="78197-104">句法</span><span class="sxs-lookup"><span data-stu-id="78197-104">SYNTAX</span></span>

### <span data-ttu-id="78197-105">ResourceGroupSet (預設) </span><span class="sxs-lookup"><span data-stu-id="78197-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78197-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78197-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78197-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="78197-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78197-108">說明</span><span class="sxs-lookup"><span data-stu-id="78197-108">DESCRIPTION</span></span>
<span data-ttu-id="78197-109">Get-AzDataMigrationService Cmdlet 會根據服務名稱和 Azure 資源群組名稱，以輸入參數，來檢索與 Azure Database 遷移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="78197-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="78197-110">示例</span><span class="sxs-lookup"><span data-stu-id="78197-110">EXAMPLES</span></span>

### <span data-ttu-id="78197-111">範例1</span><span class="sxs-lookup"><span data-stu-id="78197-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="78197-112">上述範例會檢索稱為 testService 的 Azure 資料庫移轉服務實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="78197-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="78197-113">範例2</span><span class="sxs-lookup"><span data-stu-id="78197-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="78197-114">上述範例會在名為 testResourceGroup 的資源群組中，檢索 Azure 資料庫移轉服務。</span><span class="sxs-lookup"><span data-stu-id="78197-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="78197-115">參數</span><span class="sxs-lookup"><span data-stu-id="78197-115">PARAMETERS</span></span>

### <span data-ttu-id="78197-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78197-116">-DefaultProfile</span></span>
<span data-ttu-id="78197-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78197-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78197-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="78197-118">-Name</span></span>
<span data-ttu-id="78197-119">資料庫移轉服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="78197-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78197-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78197-120">-ResourceGroupName</span></span>
<span data-ttu-id="78197-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78197-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78197-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78197-122">-ResourceId</span></span>
<span data-ttu-id="78197-123">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="78197-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="78197-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78197-124">CommonParameters</span></span>
<span data-ttu-id="78197-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78197-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78197-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="78197-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78197-127">輸入</span><span class="sxs-lookup"><span data-stu-id="78197-127">INPUTS</span></span>

### <span data-ttu-id="78197-128">System.object</span><span class="sxs-lookup"><span data-stu-id="78197-128">System.String</span></span>

## <span data-ttu-id="78197-129">輸出</span><span class="sxs-lookup"><span data-stu-id="78197-129">OUTPUTS</span></span>

### <span data-ttu-id="78197-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="78197-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="78197-131">筆記</span><span class="sxs-lookup"><span data-stu-id="78197-131">NOTES</span></span>

## <span data-ttu-id="78197-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="78197-132">RELATED LINKS</span></span>
