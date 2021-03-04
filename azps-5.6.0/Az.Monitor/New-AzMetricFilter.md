---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: a7fdb0824d464f1704f46a8e8fe19705b2b160fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917149"
---
# <span data-ttu-id="45de0-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="45de0-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="45de0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45de0-102">SYNOPSIS</span></span>
<span data-ttu-id="45de0-103">建立可用於查詢計量的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="45de0-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="45de0-104">語法</span><span class="sxs-lookup"><span data-stu-id="45de0-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45de0-105">描述</span><span class="sxs-lookup"><span data-stu-id="45de0-105">DESCRIPTION</span></span>
<span data-ttu-id="45de0-106">**New-AzMetricFilter** Cmdlet 會建立可用於查詢度量的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="45de0-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="45de0-107">例子</span><span class="sxs-lookup"><span data-stu-id="45de0-107">EXAMPLES</span></span>

### <span data-ttu-id="45de0-108">範例 1：建立公制維度篩選</span><span class="sxs-lookup"><span data-stu-id="45de0-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="45de0-109">此命令會建立"City eq 'Seattle' 或 City eq 'New York'" 格式的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="45de0-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="45de0-110">參數</span><span class="sxs-lookup"><span data-stu-id="45de0-110">PARAMETERS</span></span>

### <span data-ttu-id="45de0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45de0-111">-DefaultProfile</span></span>
<span data-ttu-id="45de0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45de0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45de0-113">-維度</span><span class="sxs-lookup"><span data-stu-id="45de0-113">-Dimension</span></span>
<span data-ttu-id="45de0-114">公制維度的名稱。</span><span class="sxs-lookup"><span data-stu-id="45de0-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="45de0-115">-運算子</span><span class="sxs-lookup"><span data-stu-id="45de0-115">-Operator</span></span>
<span data-ttu-id="45de0-116">指定用來選取公制維度的運算子。</span><span class="sxs-lookup"><span data-stu-id="45de0-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="45de0-117">-值</span><span class="sxs-lookup"><span data-stu-id="45de0-117">-Value</span></span>
<span data-ttu-id="45de0-118">指定公制維度值的陣列。</span><span class="sxs-lookup"><span data-stu-id="45de0-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="45de0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45de0-119">CommonParameters</span></span>
<span data-ttu-id="45de0-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45de0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45de0-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45de0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45de0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="45de0-122">INPUTS</span></span>

### <span data-ttu-id="45de0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="45de0-123">System.String</span></span>

### <span data-ttu-id="45de0-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="45de0-124">System.String[]</span></span>

## <span data-ttu-id="45de0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="45de0-125">OUTPUTS</span></span>

### <span data-ttu-id="45de0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="45de0-126">System.String</span></span>

## <span data-ttu-id="45de0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="45de0-127">NOTES</span></span>

## <span data-ttu-id="45de0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="45de0-128">RELATED LINKS</span></span>

<span data-ttu-id="45de0-129">[Get-AzMetric](./Get-AzMetric.md) 
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="45de0-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

