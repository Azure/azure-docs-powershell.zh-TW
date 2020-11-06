---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: aba54b47a5d335bb4f6ef1fbbf7bef66fa694aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446862"
---
# <span data-ttu-id="b751b-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="b751b-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="b751b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b751b-102">SYNOPSIS</span></span>
<span data-ttu-id="b751b-103">取得整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="b751b-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b751b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b751b-104">SYNTAX</span></span>

### <span data-ttu-id="b751b-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="b751b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b751b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b751b-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b751b-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b751b-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b751b-108">說明</span><span class="sxs-lookup"><span data-stu-id="b751b-108">DESCRIPTION</span></span>
<span data-ttu-id="b751b-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric Cmdlet 會取得資料工廠中集成執行時間的度量資料。</span><span class="sxs-lookup"><span data-stu-id="b751b-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="b751b-110">示例</span><span class="sxs-lookup"><span data-stu-id="b751b-110">EXAMPLES</span></span>

### <span data-ttu-id="b751b-111">範例1：取得整合執行時間度量</span><span class="sxs-lookup"><span data-stu-id="b751b-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="b751b-112">這個命令會在名為「rg-test-dfv2」的資源群組和名為「test-eu2」的資源群組的訂閱中，顯示名為「test-selfhost-ir」之整合執行時間的公制資料。</span><span class="sxs-lookup"><span data-stu-id="b751b-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="b751b-113">參數</span><span class="sxs-lookup"><span data-stu-id="b751b-113">PARAMETERS</span></span>

### <span data-ttu-id="b751b-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b751b-114">-DataFactoryName</span></span>
<span data-ttu-id="b751b-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="b751b-115">The data factory name.</span></span>

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

### <span data-ttu-id="b751b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b751b-116">-InputObject</span></span>
<span data-ttu-id="b751b-117">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="b751b-117">The integration runtime object.</span></span>

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

### <span data-ttu-id="b751b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b751b-118">-Name</span></span>
<span data-ttu-id="b751b-119">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b751b-119">The integration runtime name.</span></span>

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

### <span data-ttu-id="b751b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b751b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b751b-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b751b-121">The resource group name.</span></span>

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

### <span data-ttu-id="b751b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b751b-122">-ResourceId</span></span>
<span data-ttu-id="b751b-123">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b751b-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b751b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b751b-124">-DefaultProfile</span></span>
<span data-ttu-id="b751b-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b751b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b751b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b751b-126">CommonParameters</span></span>
<span data-ttu-id="b751b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b751b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b751b-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b751b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b751b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b751b-129">INPUTS</span></span>

### <span data-ttu-id="b751b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b751b-130">System.String</span></span>
<span data-ttu-id="b751b-131">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b751b-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b751b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b751b-132">OUTPUTS</span></span>

### <span data-ttu-id="b751b-133">PSIntegrationRuntimeMetrics 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b751b-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="b751b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b751b-134">NOTES</span></span>

## <span data-ttu-id="b751b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b751b-135">RELATED LINKS</span></span>

[<span data-ttu-id="b751b-136">AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b751b-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

