---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443175"
---
# <span data-ttu-id="c42d4-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="c42d4-101">Get-AzsPlan</span></span>

## <span data-ttu-id="c42d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c42d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c42d4-103">列出所有訂閱的所有方案。</span><span class="sxs-lookup"><span data-stu-id="c42d4-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="c42d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="c42d4-104">SYNTAX</span></span>

### <span data-ttu-id="c42d4-105">ListAll (預設) </span><span class="sxs-lookup"><span data-stu-id="c42d4-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c42d4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c42d4-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="c42d4-107">清單</span><span class="sxs-lookup"><span data-stu-id="c42d4-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c42d4-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c42d4-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c42d4-109">說明</span><span class="sxs-lookup"><span data-stu-id="c42d4-109">DESCRIPTION</span></span>
<span data-ttu-id="c42d4-110">列出所有訂閱的所有方案。</span><span class="sxs-lookup"><span data-stu-id="c42d4-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="c42d4-111">示例</span><span class="sxs-lookup"><span data-stu-id="c42d4-111">EXAMPLES</span></span>

### <span data-ttu-id="c42d4-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c42d4-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="c42d4-113">在此訂閱下取得特定方案。</span><span class="sxs-lookup"><span data-stu-id="c42d4-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="c42d4-114">參數</span><span class="sxs-lookup"><span data-stu-id="c42d4-114">PARAMETERS</span></span>

### <span data-ttu-id="c42d4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c42d4-115">-Name</span></span>
<span data-ttu-id="c42d4-116">方案名稱。</span><span class="sxs-lookup"><span data-stu-id="c42d4-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c42d4-118">資源所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c42d4-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c42d4-119">-ResourceId</span></span>
<span data-ttu-id="c42d4-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c42d4-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42d4-121">-略過</span><span class="sxs-lookup"><span data-stu-id="c42d4-121">-Skip</span></span>
<span data-ttu-id="c42d4-122">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c42d4-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d4-123">-上方</span><span class="sxs-lookup"><span data-stu-id="c42d4-123">-Top</span></span>
<span data-ttu-id="c42d4-124">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="c42d4-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c42d4-125">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="c42d4-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c42d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42d4-126">CommonParameters</span></span>
<span data-ttu-id="c42d4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c42d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42d4-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c42d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42d4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c42d4-129">INPUTS</span></span>

## <span data-ttu-id="c42d4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="c42d4-130">OUTPUTS</span></span>

### <span data-ttu-id="c42d4-131">AzureStack. 管理模型. 規劃</span><span class="sxs-lookup"><span data-stu-id="c42d4-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="c42d4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="c42d4-132">NOTES</span></span>

## <span data-ttu-id="c42d4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c42d4-133">RELATED LINKS</span></span>

