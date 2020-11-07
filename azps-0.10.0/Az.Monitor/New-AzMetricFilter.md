---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: eb2fbc1bf327bcfe9b7ca72139742d102e5b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794586"
---
# <span data-ttu-id="d0f24-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="d0f24-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="d0f24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0f24-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f24-103">建立可用於查詢度量單位的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="d0f24-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="d0f24-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0f24-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f24-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0f24-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f24-106">**新的-AzMetricFilter** Cmdlet 會建立可用於查詢度量單位的公制維度篩選。</span><span class="sxs-lookup"><span data-stu-id="d0f24-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="d0f24-107">示例</span><span class="sxs-lookup"><span data-stu-id="d0f24-107">EXAMPLES</span></span>

### <span data-ttu-id="d0f24-108">範例1：建立度量維度篩選</span><span class="sxs-lookup"><span data-stu-id="d0f24-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="d0f24-109">這個命令會建立 [城市 eq "北京」或 [城市 eq" （紐約）] 格式的度量維度篩選。</span><span class="sxs-lookup"><span data-stu-id="d0f24-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="d0f24-110">參數</span><span class="sxs-lookup"><span data-stu-id="d0f24-110">PARAMETERS</span></span>

### <span data-ttu-id="d0f24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f24-111">-DefaultProfile</span></span>
<span data-ttu-id="d0f24-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0f24-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f24-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="d0f24-113">-Dimension</span></span>
<span data-ttu-id="d0f24-114">度量維度的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0f24-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="d0f24-115">-運算子</span><span class="sxs-lookup"><span data-stu-id="d0f24-115">-Operator</span></span>
<span data-ttu-id="d0f24-116">指定用來選取 [公制] 維度的運算子。</span><span class="sxs-lookup"><span data-stu-id="d0f24-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="d0f24-117">-值</span><span class="sxs-lookup"><span data-stu-id="d0f24-117">-Value</span></span>
<span data-ttu-id="d0f24-118">指定公制維度值的陣列。</span><span class="sxs-lookup"><span data-stu-id="d0f24-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="d0f24-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f24-119">CommonParameters</span></span>
<span data-ttu-id="d0f24-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0f24-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f24-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d0f24-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f24-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d0f24-122">INPUTS</span></span>

### <span data-ttu-id="d0f24-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d0f24-123">System.String</span></span>

### <span data-ttu-id="d0f24-124">System.object []</span><span class="sxs-lookup"><span data-stu-id="d0f24-124">System.String[]</span></span>

## <span data-ttu-id="d0f24-125">輸出</span><span class="sxs-lookup"><span data-stu-id="d0f24-125">OUTPUTS</span></span>

### <span data-ttu-id="d0f24-126">System.object</span><span class="sxs-lookup"><span data-stu-id="d0f24-126">System.String</span></span>

## <span data-ttu-id="d0f24-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d0f24-127">NOTES</span></span>

## <span data-ttu-id="d0f24-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0f24-128">RELATED LINKS</span></span>

<span data-ttu-id="d0f24-129">[AzMetric](./Get-AzMetric.md) 
[AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="d0f24-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

