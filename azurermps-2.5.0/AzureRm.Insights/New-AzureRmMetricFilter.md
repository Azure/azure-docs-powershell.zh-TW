---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
ms.openlocfilehash: 42633beddee9e6681e68ce1ba61e71d276abf478
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800977"
---
# <span data-ttu-id="81915-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="81915-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="81915-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81915-102">SYNOPSIS</span></span>
<span data-ttu-id="81915-103">建立可用於查詢度量單位的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="81915-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81915-104">句法</span><span class="sxs-lookup"><span data-stu-id="81915-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81915-105">說明</span><span class="sxs-lookup"><span data-stu-id="81915-105">DESCRIPTION</span></span>
<span data-ttu-id="81915-106">**新的-AzureRmMetricFilter** Cmdlet 會建立可用於查詢度量單位的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="81915-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="81915-107">示例</span><span class="sxs-lookup"><span data-stu-id="81915-107">EXAMPLES</span></span>

### <span data-ttu-id="81915-108">範例1：建立度量維度篩選</span><span class="sxs-lookup"><span data-stu-id="81915-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="81915-109">這個命令會建立 [城市 eq "北京」或 [城市 eq" （紐約）] 格式的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="81915-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="81915-110">參數</span><span class="sxs-lookup"><span data-stu-id="81915-110">PARAMETERS</span></span>

### <span data-ttu-id="81915-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81915-111">-DefaultProfile</span></span>
<span data-ttu-id="81915-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81915-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81915-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="81915-113">-Dimension</span></span>
<span data-ttu-id="81915-114">度量維度的名稱。</span><span class="sxs-lookup"><span data-stu-id="81915-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="81915-115">-運算子</span><span class="sxs-lookup"><span data-stu-id="81915-115">-Operator</span></span>
<span data-ttu-id="81915-116">指定用來選取 [公制] 維度的運算子。</span><span class="sxs-lookup"><span data-stu-id="81915-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="81915-117">-值</span><span class="sxs-lookup"><span data-stu-id="81915-117">-Value</span></span>
<span data-ttu-id="81915-118">指定公制維度值的陣列。</span><span class="sxs-lookup"><span data-stu-id="81915-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="81915-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81915-119">CommonParameters</span></span>
<span data-ttu-id="81915-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81915-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81915-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81915-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81915-122">輸入</span><span class="sxs-lookup"><span data-stu-id="81915-122">INPUTS</span></span>

### <span data-ttu-id="81915-123">System.object</span><span class="sxs-lookup"><span data-stu-id="81915-123">System.String</span></span>

### <span data-ttu-id="81915-124">System.object []</span><span class="sxs-lookup"><span data-stu-id="81915-124">System.String[]</span></span>

## <span data-ttu-id="81915-125">輸出</span><span class="sxs-lookup"><span data-stu-id="81915-125">OUTPUTS</span></span>

### <span data-ttu-id="81915-126">System.object</span><span class="sxs-lookup"><span data-stu-id="81915-126">System.String</span></span>

## <span data-ttu-id="81915-127">筆記</span><span class="sxs-lookup"><span data-stu-id="81915-127">NOTES</span></span>

## <span data-ttu-id="81915-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="81915-128">RELATED LINKS</span></span>

<span data-ttu-id="81915-129">[AzureRmMetric](./Get-AzureRmMetric.md) 
[AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="81915-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

