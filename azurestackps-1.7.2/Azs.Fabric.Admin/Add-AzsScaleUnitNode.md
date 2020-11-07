---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793423"
---
# <span data-ttu-id="71875-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="71875-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="71875-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71875-102">SYNOPSIS</span></span>
<span data-ttu-id="71875-103">擴大比例單位。</span><span class="sxs-lookup"><span data-stu-id="71875-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="71875-104">句法</span><span class="sxs-lookup"><span data-stu-id="71875-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="71875-105">說明</span><span class="sxs-lookup"><span data-stu-id="71875-105">DESCRIPTION</span></span>
<span data-ttu-id="71875-106">將新的縮放比例單位節點新增至縮放比例單位分類。</span><span class="sxs-lookup"><span data-stu-id="71875-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="71875-107">示例</span><span class="sxs-lookup"><span data-stu-id="71875-107">EXAMPLES</span></span>

### <span data-ttu-id="71875-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="71875-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="71875-109">新增節點清單至比例單位。</span><span class="sxs-lookup"><span data-stu-id="71875-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="71875-110">參數</span><span class="sxs-lookup"><span data-stu-id="71875-110">PARAMETERS</span></span>

### <span data-ttu-id="71875-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71875-111">-AsJob</span></span>
<span data-ttu-id="71875-112">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="71875-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71875-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="71875-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="71875-114">在傳回成功前，請等候儲存複製完成。</span><span class="sxs-lookup"><span data-stu-id="71875-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71875-115">-位置</span><span class="sxs-lookup"><span data-stu-id="71875-115">-Location</span></span>
<span data-ttu-id="71875-116">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="71875-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71875-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="71875-117">-NodeList</span></span>
<span data-ttu-id="71875-118">可讓您新增一組比例單位節點的輸入資料清單。</span><span class="sxs-lookup"><span data-stu-id="71875-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71875-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71875-119">-ResourceGroupName</span></span>
<span data-ttu-id="71875-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71875-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71875-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="71875-121">-ScaleUnit</span></span>
<span data-ttu-id="71875-122">縮放單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="71875-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71875-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71875-123">CommonParameters</span></span>
<span data-ttu-id="71875-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71875-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71875-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71875-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71875-126">輸入</span><span class="sxs-lookup"><span data-stu-id="71875-126">INPUTS</span></span>

## <span data-ttu-id="71875-127">輸出</span><span class="sxs-lookup"><span data-stu-id="71875-127">OUTPUTS</span></span>

## <span data-ttu-id="71875-128">筆記</span><span class="sxs-lookup"><span data-stu-id="71875-128">NOTES</span></span>

## <span data-ttu-id="71875-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="71875-129">RELATED LINKS</span></span>

