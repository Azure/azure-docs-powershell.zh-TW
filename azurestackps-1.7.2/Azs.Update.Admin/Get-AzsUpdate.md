---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc16e5ecb0a70c20f9cd8b77b16208a09ac0a023
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793408"
---
# <span data-ttu-id="beaca-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="beaca-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="beaca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="beaca-102">SYNOPSIS</span></span>
<span data-ttu-id="beaca-103">取得可用更新的清單。</span><span class="sxs-lookup"><span data-stu-id="beaca-103">Get the list of available updates.</span></span>

## <span data-ttu-id="beaca-104">句法</span><span class="sxs-lookup"><span data-stu-id="beaca-104">SYNTAX</span></span>

### <span data-ttu-id="beaca-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="beaca-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="beaca-106">獲取</span><span class="sxs-lookup"><span data-stu-id="beaca-106">Get</span></span>
```
Get-AzsUpdate [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="beaca-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="beaca-107">ResourceId</span></span>
```
Get-AzsUpdate -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="beaca-108">說明</span><span class="sxs-lookup"><span data-stu-id="beaca-108">DESCRIPTION</span></span>
<span data-ttu-id="beaca-109">取得可用更新的清單。</span><span class="sxs-lookup"><span data-stu-id="beaca-109">Get the list of available updates.</span></span> <span data-ttu-id="beaca-110">如果適用，此模組傳回的更新可能會以管道傳送到「安裝-AzsUpdate」。</span><span class="sxs-lookup"><span data-stu-id="beaca-110">Updates returned from this module may be piped to 'Install-AzsUpdate', if applicable.</span></span>

## <span data-ttu-id="beaca-111">示例</span><span class="sxs-lookup"><span data-stu-id="beaca-111">EXAMPLES</span></span>

### <span data-ttu-id="beaca-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="beaca-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate | ft
```

<span data-ttu-id="beaca-113">取得可用更新的清單。</span><span class="sxs-lookup"><span data-stu-id="beaca-113">Get the list of available updates.</span></span>

### <span data-ttu-id="beaca-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="beaca-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1
```

<span data-ttu-id="beaca-115">取得特定的更新。</span><span class="sxs-lookup"><span data-stu-id="beaca-115">Get the specific update.</span></span>

## <span data-ttu-id="beaca-116">參數</span><span class="sxs-lookup"><span data-stu-id="beaca-116">PARAMETERS</span></span>

### <span data-ttu-id="beaca-117">-位置</span><span class="sxs-lookup"><span data-stu-id="beaca-117">-Location</span></span>
<span data-ttu-id="beaca-118">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="beaca-118">The name of the update location.</span></span>

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

### <span data-ttu-id="beaca-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="beaca-119">-Name</span></span>
<span data-ttu-id="beaca-120">更新的名稱。</span><span class="sxs-lookup"><span data-stu-id="beaca-120">Name of the update.</span></span>

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

### <span data-ttu-id="beaca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beaca-121">-ResourceGroupName</span></span>
<span data-ttu-id="beaca-122">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="beaca-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="beaca-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="beaca-123">-ResourceId</span></span>
<span data-ttu-id="beaca-124">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="beaca-124">The resource id.</span></span>

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

### <span data-ttu-id="beaca-125">-略過</span><span class="sxs-lookup"><span data-stu-id="beaca-125">-Skip</span></span>
<span data-ttu-id="beaca-126">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="beaca-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="beaca-127">-上方</span><span class="sxs-lookup"><span data-stu-id="beaca-127">-Top</span></span>
<span data-ttu-id="beaca-128">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="beaca-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="beaca-129">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="beaca-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="beaca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beaca-130">CommonParameters</span></span>
<span data-ttu-id="beaca-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="beaca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beaca-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="beaca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beaca-133">輸入</span><span class="sxs-lookup"><span data-stu-id="beaca-133">INPUTS</span></span>

## <span data-ttu-id="beaca-134">輸出</span><span class="sxs-lookup"><span data-stu-id="beaca-134">OUTPUTS</span></span>

### <span data-ttu-id="beaca-135">AzureStack 更新. 系統管理模型。</span><span class="sxs-lookup"><span data-stu-id="beaca-135">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="beaca-136">筆記</span><span class="sxs-lookup"><span data-stu-id="beaca-136">NOTES</span></span>

## <span data-ttu-id="beaca-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="beaca-137">RELATED LINKS</span></span>

