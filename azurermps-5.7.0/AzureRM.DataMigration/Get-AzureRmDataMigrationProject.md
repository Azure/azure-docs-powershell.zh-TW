---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454263"
---
# <span data-ttu-id="0fa22-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="0fa22-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="0fa22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0fa22-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa22-103">檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fa22-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fa22-104">句法</span><span class="sxs-lookup"><span data-stu-id="0fa22-104">SYNTAX</span></span>

### <span data-ttu-id="0fa22-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0fa22-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="0fa22-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa22-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="0fa22-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa22-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="0fa22-108">說明</span><span class="sxs-lookup"><span data-stu-id="0fa22-108">DESCRIPTION</span></span>
<span data-ttu-id="0fa22-109">Get-AzureRmDataMigrationProject Cmdlet 會檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="0fa22-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="0fa22-110">示例</span><span class="sxs-lookup"><span data-stu-id="0fa22-110">EXAMPLES</span></span>

### <span data-ttu-id="0fa22-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0fa22-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="0fa22-112">上述範例會在名為「testResourceGroup」的資源群組中檢索名為 TestProject 的 Azure 資料庫移轉專案，並在 [服務稱為 testService]</span><span class="sxs-lookup"><span data-stu-id="0fa22-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="0fa22-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0fa22-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="0fa22-114">上述範例會根據傳入的 PSProject 物件輸入參數，來檢索 Azure Database 移植專案。</span><span class="sxs-lookup"><span data-stu-id="0fa22-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="0fa22-115">參數</span><span class="sxs-lookup"><span data-stu-id="0fa22-115">PARAMETERS</span></span>

### <span data-ttu-id="0fa22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa22-116">-DefaultProfile</span></span>
<span data-ttu-id="0fa22-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0fa22-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fa22-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa22-118">-InputObject</span></span>
<span data-ttu-id="0fa22-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="0fa22-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa22-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0fa22-120">-Name</span></span>
<span data-ttu-id="0fa22-121">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0fa22-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fa22-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa22-122">-ResourceGroupName</span></span>
<span data-ttu-id="0fa22-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0fa22-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fa22-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa22-124">-ResourceId</span></span>
<span data-ttu-id="0fa22-125">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0fa22-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="0fa22-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0fa22-126">-ServiceName</span></span>
<span data-ttu-id="0fa22-127">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="0fa22-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="0fa22-128">輸入</span><span class="sxs-lookup"><span data-stu-id="0fa22-128">INPUTS</span></span>

### <span data-ttu-id="0fa22-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="0fa22-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="0fa22-130">System.object</span><span class="sxs-lookup"><span data-stu-id="0fa22-130">System.String</span></span>


## <span data-ttu-id="0fa22-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0fa22-131">OUTPUTS</span></span>

### <span data-ttu-id="0fa22-132">DataMigration 集合. 泛型. IList "1 [PSProject，DataMigration，Version = 0.1.0.0，Culture = 中性，PublicKeyToken = null]] （區域性 = null）</span><span class="sxs-lookup"><span data-stu-id="0fa22-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="0fa22-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0fa22-133">NOTES</span></span>

## <span data-ttu-id="0fa22-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0fa22-134">RELATED LINKS</span></span>

