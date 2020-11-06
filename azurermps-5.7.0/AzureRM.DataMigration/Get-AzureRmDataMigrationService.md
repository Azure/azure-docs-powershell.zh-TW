---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450616"
---
# <span data-ttu-id="e943a-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="e943a-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="e943a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e943a-102">SYNOPSIS</span></span>
<span data-ttu-id="e943a-103">檢索與 Azure Database 遷移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="e943a-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e943a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e943a-104">SYNTAX</span></span>

### <span data-ttu-id="e943a-105">ResourceGroupSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e943a-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="e943a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e943a-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="e943a-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="e943a-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="e943a-108">說明</span><span class="sxs-lookup"><span data-stu-id="e943a-108">DESCRIPTION</span></span>
<span data-ttu-id="e943a-109">Get-AzureRmDataMigrationService Cmdlet 會根據服務名稱和 Azure 資源群組名稱，以輸入參數，來檢索與 Azure Database 遷移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="e943a-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="e943a-110">示例</span><span class="sxs-lookup"><span data-stu-id="e943a-110">EXAMPLES</span></span>

### <span data-ttu-id="e943a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e943a-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="e943a-112">上述範例會檢索稱為 testService 的 Azure 資料庫移轉服務實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="e943a-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="e943a-113">範例2</span><span class="sxs-lookup"><span data-stu-id="e943a-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="e943a-114">上述範例會在名為 testResourceGroup 的資源群組中，檢索 Azure 資料庫移轉服務。</span><span class="sxs-lookup"><span data-stu-id="e943a-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="e943a-115">參數</span><span class="sxs-lookup"><span data-stu-id="e943a-115">PARAMETERS</span></span>

### <span data-ttu-id="e943a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e943a-116">-DefaultProfile</span></span>
<span data-ttu-id="e943a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e943a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e943a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e943a-118">-Name</span></span>
<span data-ttu-id="e943a-119">資料移轉服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="e943a-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e943a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e943a-120">-ResourceGroupName</span></span>
<span data-ttu-id="e943a-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e943a-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e943a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e943a-122">-ResourceId</span></span>
<span data-ttu-id="e943a-123">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e943a-123">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e943a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e943a-124">INPUTS</span></span>

### <span data-ttu-id="e943a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e943a-125">System.String</span></span>


## <span data-ttu-id="e943a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e943a-126">OUTPUTS</span></span>

### <span data-ttu-id="e943a-127">System.object. IList "1 [Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService、DataMigration、Version = 0.1.0.0、Culture = 中性、PublicKeyToken = null）]</span><span class="sxs-lookup"><span data-stu-id="e943a-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="e943a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e943a-128">NOTES</span></span>

## <span data-ttu-id="e943a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e943a-129">RELATED LINKS</span></span>





