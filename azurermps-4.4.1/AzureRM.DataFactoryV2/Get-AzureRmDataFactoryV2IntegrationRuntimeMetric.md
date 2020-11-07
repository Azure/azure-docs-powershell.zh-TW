---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626640"
---
# <span data-ttu-id="7eec7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="7eec7-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="7eec7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eec7-102">SYNOPSIS</span></span>
<span data-ttu-id="7eec7-103">取得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="7eec7-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eec7-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eec7-104">SYNTAX</span></span>

### <span data-ttu-id="7eec7-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="7eec7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="7eec7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7eec7-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="7eec7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7eec7-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="7eec7-108">說明</span><span class="sxs-lookup"><span data-stu-id="7eec7-108">DESCRIPTION</span></span>
<span data-ttu-id="7eec7-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric Cmdlet 會取得資料工廠中集成執行時間的度量資料。</span><span class="sxs-lookup"><span data-stu-id="7eec7-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="7eec7-110">示例</span><span class="sxs-lookup"><span data-stu-id="7eec7-110">EXAMPLES</span></span>

### <span data-ttu-id="7eec7-111">範例1：取得整合執行時間度量</span><span class="sxs-lookup"><span data-stu-id="7eec7-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="7eec7-112">這個命令會在名為「rg-test-dfv2」的資源群組和名為「test-eu2」的資源群組的訂閱中，顯示名為「test-selfhost-ir」之整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="7eec7-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="7eec7-113">參數</span><span class="sxs-lookup"><span data-stu-id="7eec7-113">PARAMETERS</span></span>

### <span data-ttu-id="7eec7-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7eec7-114">-DataFactoryName</span></span>
<span data-ttu-id="7eec7-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="7eec7-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eec7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eec7-116">-InputObject</span></span>
<span data-ttu-id="7eec7-117">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="7eec7-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eec7-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7eec7-118">-Name</span></span>
<span data-ttu-id="7eec7-119">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="7eec7-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eec7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eec7-120">-ResourceGroupName</span></span>
<span data-ttu-id="7eec7-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eec7-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eec7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eec7-122">-ResourceId</span></span>
<span data-ttu-id="7eec7-123">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7eec7-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="7eec7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7eec7-124">INPUTS</span></span>

### <span data-ttu-id="7eec7-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7eec7-125">System.String</span></span>
<span data-ttu-id="7eec7-126">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="7eec7-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="7eec7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7eec7-127">OUTPUTS</span></span>

### <span data-ttu-id="7eec7-128">PSIntegrationRuntimeMetrics 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="7eec7-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="7eec7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7eec7-129">NOTES</span></span>

## <span data-ttu-id="7eec7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eec7-130">RELATED LINKS</span></span>
[<span data-ttu-id="7eec7-131">AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7eec7-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

