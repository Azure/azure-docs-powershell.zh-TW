---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626408"
---
# <span data-ttu-id="91afa-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="91afa-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="91afa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91afa-102">SYNOPSIS</span></span>
<span data-ttu-id="91afa-103">建立可用於查詢度量單位的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="91afa-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91afa-104">句法</span><span class="sxs-lookup"><span data-stu-id="91afa-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91afa-105">說明</span><span class="sxs-lookup"><span data-stu-id="91afa-105">DESCRIPTION</span></span>
<span data-ttu-id="91afa-106">**新的-AzureRmMetricFilter** Cmdlet 會建立可用於查詢度量單位的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="91afa-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="91afa-107">示例</span><span class="sxs-lookup"><span data-stu-id="91afa-107">EXAMPLES</span></span>

### <span data-ttu-id="91afa-108">範例1：建立度量維度篩選</span><span class="sxs-lookup"><span data-stu-id="91afa-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="91afa-109">這個命令會建立 [城市 eq "北京」或 [城市 eq" （紐約）] 格式的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="91afa-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="91afa-110">參數</span><span class="sxs-lookup"><span data-stu-id="91afa-110">PARAMETERS</span></span>

### <span data-ttu-id="91afa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91afa-111">-DefaultProfile</span></span>
<span data-ttu-id="91afa-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91afa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91afa-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="91afa-113">-Dimension</span></span>
<span data-ttu-id="91afa-114">度量維度的名稱。</span><span class="sxs-lookup"><span data-stu-id="91afa-114">The name of the metric dimension.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91afa-115">-運算子</span><span class="sxs-lookup"><span data-stu-id="91afa-115">-Operator</span></span>
<span data-ttu-id="91afa-116">指定用來選取 [公制] 維度的運算子。</span><span class="sxs-lookup"><span data-stu-id="91afa-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91afa-117">-值</span><span class="sxs-lookup"><span data-stu-id="91afa-117">-Value</span></span>
<span data-ttu-id="91afa-118">指定公制維度值的陣列。</span><span class="sxs-lookup"><span data-stu-id="91afa-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91afa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91afa-119">CommonParameters</span></span>
<span data-ttu-id="91afa-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91afa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91afa-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91afa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91afa-122">輸入</span><span class="sxs-lookup"><span data-stu-id="91afa-122">INPUTS</span></span>

### <span data-ttu-id="91afa-123">System.object</span><span class="sxs-lookup"><span data-stu-id="91afa-123">System.String</span></span>

### <span data-ttu-id="91afa-124">System.object []</span><span class="sxs-lookup"><span data-stu-id="91afa-124">System.String[]</span></span>

## <span data-ttu-id="91afa-125">輸出</span><span class="sxs-lookup"><span data-stu-id="91afa-125">OUTPUTS</span></span>

### <span data-ttu-id="91afa-126">System.object</span><span class="sxs-lookup"><span data-stu-id="91afa-126">System.String</span></span>

## <span data-ttu-id="91afa-127">筆記</span><span class="sxs-lookup"><span data-stu-id="91afa-127">NOTES</span></span>

## <span data-ttu-id="91afa-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="91afa-128">RELATED LINKS</span></span>

<span data-ttu-id="91afa-129">[AzureRmMetric](./Get-AzureRmMetric.md) 
[AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="91afa-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

