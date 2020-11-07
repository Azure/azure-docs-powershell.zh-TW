---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87bab7bc266a77d9459bb0a3166d09f2b7d6c7de
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793442"
---
# <span data-ttu-id="527ce-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="527ce-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="527ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="527ce-102">SYNOPSIS</span></span>
<span data-ttu-id="527ce-103">取得可用更新的清單。</span><span class="sxs-lookup"><span data-stu-id="527ce-103">Get the list of available updates.</span></span>

## <span data-ttu-id="527ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="527ce-104">SYNTAX</span></span>

### <span data-ttu-id="527ce-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="527ce-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="527ce-106">獲取</span><span class="sxs-lookup"><span data-stu-id="527ce-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="527ce-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="527ce-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="527ce-108">說明</span><span class="sxs-lookup"><span data-stu-id="527ce-108">DESCRIPTION</span></span>
<span data-ttu-id="527ce-109">取得可用更新的清單。</span><span class="sxs-lookup"><span data-stu-id="527ce-109">Get the list of available updates.</span></span> <span data-ttu-id="527ce-110">如果適用，此模組傳回的更新可能會以管道傳送到「安裝-AzsUpdate」。</span><span class="sxs-lookup"><span data-stu-id="527ce-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="527ce-111">示例</span><span class="sxs-lookup"><span data-stu-id="527ce-111">EXAMPLES</span></span>

### <span data-ttu-id="527ce-112">範例1</span><span class="sxs-lookup"><span data-stu-id="527ce-112">EXAMPLE 1</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="527ce-113">取得可用更新的清單。</span><span class="sxs-lookup"><span data-stu-id="527ce-113">Get the list of available updates.</span></span>

### <span data-ttu-id="527ce-114">範例2</span><span class="sxs-lookup"><span data-stu-id="527ce-114">EXAMPLE 2</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="527ce-115">取得特定的更新。</span><span class="sxs-lookup"><span data-stu-id="527ce-115">Get the specific update.</span></span>

## <span data-ttu-id="527ce-116">參數</span><span class="sxs-lookup"><span data-stu-id="527ce-116">PARAMETERS</span></span>

### <span data-ttu-id="527ce-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="527ce-117">-Name</span></span>
<span data-ttu-id="527ce-118">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="527ce-118">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Update

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="527ce-119">-位置</span><span class="sxs-lookup"><span data-stu-id="527ce-119">-Location</span></span>
<span data-ttu-id="527ce-120">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="527ce-120">The name of the update location.</span></span>

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

### <span data-ttu-id="527ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="527ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="527ce-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="527ce-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="527ce-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="527ce-123">-ResourceId</span></span>
<span data-ttu-id="527ce-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="527ce-124">The resource id.</span></span>

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

### <span data-ttu-id="527ce-125">-略過</span><span class="sxs-lookup"><span data-stu-id="527ce-125">-Skip</span></span>
<span data-ttu-id="527ce-126">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="527ce-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="527ce-127">-上方</span><span class="sxs-lookup"><span data-stu-id="527ce-127">-Top</span></span>
<span data-ttu-id="527ce-128">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="527ce-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="527ce-129">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="527ce-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="527ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527ce-130">CommonParameters</span></span>
<span data-ttu-id="527ce-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="527ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527ce-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="527ce-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527ce-133">輸入</span><span class="sxs-lookup"><span data-stu-id="527ce-133">INPUTS</span></span>

## <span data-ttu-id="527ce-134">輸出</span><span class="sxs-lookup"><span data-stu-id="527ce-134">OUTPUTS</span></span>

### <span data-ttu-id="527ce-135">AzureStack 更新. 系統管理模型。</span><span class="sxs-lookup"><span data-stu-id="527ce-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="527ce-136">筆記</span><span class="sxs-lookup"><span data-stu-id="527ce-136">NOTES</span></span>

## <span data-ttu-id="527ce-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="527ce-137">RELATED LINKS</span></span>
