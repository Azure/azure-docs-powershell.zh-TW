---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798950"
---
# <span data-ttu-id="a2793-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="a2793-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="a2793-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2793-102">SYNOPSIS</span></span>
<span data-ttu-id="a2793-103">取得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="a2793-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="a2793-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2793-104">SYNTAX</span></span>

### <span data-ttu-id="a2793-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="a2793-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2793-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2793-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2793-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a2793-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2793-108">說明</span><span class="sxs-lookup"><span data-stu-id="a2793-108">DESCRIPTION</span></span>
<span data-ttu-id="a2793-109">Get-AzDataFactoryV2IntegrationRuntimeMetric Cmdlet 會取得資料工廠中集成執行時間的度量資料。</span><span class="sxs-lookup"><span data-stu-id="a2793-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="a2793-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2793-110">EXAMPLES</span></span>

### <span data-ttu-id="a2793-111">範例1：取得整合執行時間度量</span><span class="sxs-lookup"><span data-stu-id="a2793-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="a2793-112">這個命令會在名為「rg-test-dfv2」的資源群組和名為「test-eu2」的資源群組的訂閱中，顯示名為「test-selfhost-ir」之整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="a2793-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="a2793-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2793-113">PARAMETERS</span></span>

### <span data-ttu-id="a2793-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a2793-114">-DataFactoryName</span></span>
<span data-ttu-id="a2793-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a2793-115">The data factory name.</span></span>

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

### <span data-ttu-id="a2793-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2793-116">-DefaultProfile</span></span>
<span data-ttu-id="a2793-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2793-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2793-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2793-118">-InputObject</span></span>
<span data-ttu-id="a2793-119">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="a2793-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="a2793-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2793-120">-Name</span></span>
<span data-ttu-id="a2793-121">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="a2793-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="a2793-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2793-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2793-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2793-123">The resource group name.</span></span>

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

### <span data-ttu-id="a2793-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2793-124">-ResourceId</span></span>
<span data-ttu-id="a2793-125">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2793-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a2793-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2793-126">CommonParameters</span></span>
<span data-ttu-id="a2793-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2793-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2793-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2793-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2793-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a2793-129">INPUTS</span></span>

### <span data-ttu-id="a2793-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a2793-130">System.String</span></span>

### <span data-ttu-id="a2793-131">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="a2793-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a2793-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a2793-132">OUTPUTS</span></span>

### <span data-ttu-id="a2793-133">PSIntegrationRuntimeMetrics 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="a2793-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="a2793-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a2793-134">NOTES</span></span>

## <span data-ttu-id="a2793-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2793-135">RELATED LINKS</span></span>

[<span data-ttu-id="a2793-136">AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a2793-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

