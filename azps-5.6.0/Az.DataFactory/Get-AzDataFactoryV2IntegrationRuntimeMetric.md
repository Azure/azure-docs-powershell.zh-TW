---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 12810756f1ebe3e3bf345519d981b660f4c61aa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907734"
---
# <span data-ttu-id="55c2d-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="55c2d-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="55c2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="55c2d-103">獲得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="55c2d-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="55c2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="55c2d-104">SYNTAX</span></span>

### <span data-ttu-id="55c2d-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="55c2d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55c2d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="55c2d-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55c2d-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="55c2d-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55c2d-108">描述</span><span class="sxs-lookup"><span data-stu-id="55c2d-108">DESCRIPTION</span></span>
<span data-ttu-id="55c2d-109">Cmdlet Get-AzDataFactoryV2IntegrationRuntimeMetric在資料工廠中獲得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="55c2d-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="55c2d-110">例子</span><span class="sxs-lookup"><span data-stu-id="55c2d-110">EXAMPLES</span></span>

### <span data-ttu-id="55c2d-111">範例 1：取得整合執行時間度量</span><span class="sxs-lookup"><span data-stu-id="55c2d-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="55c2d-112">此命令會在名為'rg-test-dfv2'及名為'test-df-eu2'的資料工廠之資源群組訂閱中，顯示名為"test-selfhost-ir"之整合執行時間的計量資料。</span><span class="sxs-lookup"><span data-stu-id="55c2d-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="55c2d-113">參數</span><span class="sxs-lookup"><span data-stu-id="55c2d-113">PARAMETERS</span></span>

### <span data-ttu-id="55c2d-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="55c2d-114">-DataFactoryName</span></span>
<span data-ttu-id="55c2d-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="55c2d-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c2d-116">-DefaultProfile</span></span>
<span data-ttu-id="55c2d-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55c2d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55c2d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55c2d-118">-InputObject</span></span>
<span data-ttu-id="55c2d-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="55c2d-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55c2d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="55c2d-120">-Name</span></span>
<span data-ttu-id="55c2d-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="55c2d-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="55c2d-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="55c2d-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c2d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c2d-124">-ResourceId</span></span>
<span data-ttu-id="55c2d-125">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="55c2d-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c2d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c2d-126">CommonParameters</span></span>
<span data-ttu-id="55c2d-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55c2d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c2d-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="55c2d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c2d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="55c2d-129">INPUTS</span></span>

### <span data-ttu-id="55c2d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="55c2d-130">System.String</span></span>

### <span data-ttu-id="55c2d-131">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="55c2d-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="55c2d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="55c2d-132">OUTPUTS</span></span>

### <span data-ttu-id="55c2d-133">Microsoft.Azure.Commands.DataFactoryV2.models.PSMetricRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="55c2d-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="55c2d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="55c2d-134">NOTES</span></span>

## <span data-ttu-id="55c2d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="55c2d-135">RELATED LINKS</span></span>

[<span data-ttu-id="55c2d-136">Get-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="55c2d-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

