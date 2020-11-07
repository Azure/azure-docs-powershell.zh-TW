---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0bbd694fff313f4c7b8983521dee8cd1c01f7561
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793441"
---
# <span data-ttu-id="e9b9f-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="e9b9f-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="e9b9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b9f-103">取得更新執行的清單。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-103">Get the list of update runs.</span></span>

## <span data-ttu-id="e9b9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9b9f-104">SYNTAX</span></span>

### <span data-ttu-id="e9b9f-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e9b9f-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e9b9f-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e9b9f-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9b9f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b9f-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e9b9f-108">說明</span><span class="sxs-lookup"><span data-stu-id="e9b9f-108">DESCRIPTION</span></span>
<span data-ttu-id="e9b9f-109">取得更新執行的清單。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-109">Get the list of update runs.</span></span> <span data-ttu-id="e9b9f-110">如果適用，會將傳回的 UpdateRun 物件實例以管道方式重新開機-AzsUpdateRun。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="e9b9f-111">示例</span><span class="sxs-lookup"><span data-stu-id="e9b9f-111">EXAMPLES</span></span>

### <span data-ttu-id="e9b9f-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e9b9f-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="e9b9f-113">取得所有嘗試套用特定更新的清單。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="e9b9f-114">參數</span><span class="sxs-lookup"><span data-stu-id="e9b9f-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b9f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9b9f-115">-Name</span></span>
<span data-ttu-id="e9b9f-116">更新執行識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-116">Update run identifier.</span></span>

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

### <span data-ttu-id="e9b9f-117">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="e9b9f-117">-UpdateName</span></span>
<span data-ttu-id="e9b9f-118">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-119">-位置</span><span class="sxs-lookup"><span data-stu-id="e9b9f-119">-Location</span></span>
<span data-ttu-id="e9b9f-120">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-120">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b9f-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9b9f-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-122">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b9f-123">-ResourceId</span></span>
<span data-ttu-id="e9b9f-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-124">The resource id.</span></span>

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

### <span data-ttu-id="e9b9f-125">-略過</span><span class="sxs-lookup"><span data-stu-id="e9b9f-125">-Skip</span></span>
<span data-ttu-id="e9b9f-126">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-126">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-127">-上方</span><span class="sxs-lookup"><span data-stu-id="e9b9f-127">-Top</span></span>
<span data-ttu-id="e9b9f-128">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9b9f-129">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b9f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b9f-130">CommonParameters</span></span>
<span data-ttu-id="e9b9f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b9f-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9b9f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b9f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e9b9f-133">INPUTS</span></span>

## <span data-ttu-id="e9b9f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e9b9f-134">OUTPUTS</span></span>

### <span data-ttu-id="e9b9f-135">AzureStack （UpdateRun）的</span><span class="sxs-lookup"><span data-stu-id="e9b9f-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="e9b9f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e9b9f-136">NOTES</span></span>

## <span data-ttu-id="e9b9f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9b9f-137">RELATED LINKS</span></span>