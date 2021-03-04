---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 4dfe4f52a344b8d2308288cfb659792c7b4aabab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903605"
---
# <span data-ttu-id="65261-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="65261-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="65261-102">簡介</span><span class="sxs-lookup"><span data-stu-id="65261-102">SYNOPSIS</span></span>
<span data-ttu-id="65261-103">會取回與 Azure 資料庫移移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="65261-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="65261-104">語法</span><span class="sxs-lookup"><span data-stu-id="65261-104">SYNTAX</span></span>

### <span data-ttu-id="65261-105">ResourceGroupSet (預設) </span><span class="sxs-lookup"><span data-stu-id="65261-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65261-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65261-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65261-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="65261-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65261-108">描述</span><span class="sxs-lookup"><span data-stu-id="65261-108">DESCRIPTION</span></span>
<span data-ttu-id="65261-109">此Get-AzDataMigrationService Cmdlet 會依據服務名稱與 Azure 資源組名做為輸入參數，來取取與 Azure 資料庫移轉服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="65261-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="65261-110">例子</span><span class="sxs-lookup"><span data-stu-id="65261-110">EXAMPLES</span></span>

### <span data-ttu-id="65261-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="65261-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="65261-112">上述範例會取回稱為 testService 的 Azure 資料庫移移服務實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="65261-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="65261-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="65261-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="65261-114">上述範例會從名為 testResourceGroup 的資源群組中，取回 Azure 資料庫移移服務。</span><span class="sxs-lookup"><span data-stu-id="65261-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="65261-115">參數</span><span class="sxs-lookup"><span data-stu-id="65261-115">PARAMETERS</span></span>

### <span data-ttu-id="65261-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65261-116">-DefaultProfile</span></span>
<span data-ttu-id="65261-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="65261-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65261-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="65261-118">-Name</span></span>
<span data-ttu-id="65261-119">資料庫移移服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="65261-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="65261-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65261-120">-ResourceGroupName</span></span>
<span data-ttu-id="65261-121">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="65261-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="65261-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65261-122">-ResourceId</span></span>
<span data-ttu-id="65261-123">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="65261-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="65261-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65261-124">CommonParameters</span></span>
<span data-ttu-id="65261-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="65261-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65261-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="65261-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65261-127">輸入</span><span class="sxs-lookup"><span data-stu-id="65261-127">INPUTS</span></span>

### <span data-ttu-id="65261-128">System.String</span><span class="sxs-lookup"><span data-stu-id="65261-128">System.String</span></span>

## <span data-ttu-id="65261-129">輸出</span><span class="sxs-lookup"><span data-stu-id="65261-129">OUTPUTS</span></span>

### <span data-ttu-id="65261-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="65261-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="65261-131">筆記</span><span class="sxs-lookup"><span data-stu-id="65261-131">NOTES</span></span>

## <span data-ttu-id="65261-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="65261-132">RELATED LINKS</span></span>
