---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968318"
---
# <span data-ttu-id="bc400-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="bc400-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="bc400-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc400-102">SYNOPSIS</span></span>
<span data-ttu-id="bc400-103">傳回所有儲存空間伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="bc400-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="bc400-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc400-104">SYNTAX</span></span>

### <span data-ttu-id="bc400-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="bc400-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bc400-106">獲取</span><span class="sxs-lookup"><span data-stu-id="bc400-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bc400-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc400-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bc400-108">說明</span><span class="sxs-lookup"><span data-stu-id="bc400-108">DESCRIPTION</span></span>
<span data-ttu-id="bc400-109">傳回所有儲存空間伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="bc400-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="bc400-110">示例</span><span class="sxs-lookup"><span data-stu-id="bc400-110">EXAMPLES</span></span>

### <span data-ttu-id="bc400-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bc400-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="bc400-112">取得所有儲存區的清單。</span><span class="sxs-lookup"><span data-stu-id="bc400-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="bc400-113">參數</span><span class="sxs-lookup"><span data-stu-id="bc400-113">PARAMETERS</span></span>

### <span data-ttu-id="bc400-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc400-114">-Name</span></span>
<span data-ttu-id="bc400-115">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="bc400-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc400-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc400-116">-ResourceGroupName</span></span>
<span data-ttu-id="bc400-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bc400-117">Resource group name.</span></span>

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

### <span data-ttu-id="bc400-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc400-118">-ResourceId</span></span>
<span data-ttu-id="bc400-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="bc400-119">The resource id.</span></span>

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

### <span data-ttu-id="bc400-120">-略過</span><span class="sxs-lookup"><span data-stu-id="bc400-120">-Skip</span></span>
<span data-ttu-id="bc400-121">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="bc400-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bc400-122">-上方</span><span class="sxs-lookup"><span data-stu-id="bc400-122">-Top</span></span>
<span data-ttu-id="bc400-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="bc400-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bc400-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="bc400-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bc400-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc400-125">CommonParameters</span></span>
<span data-ttu-id="bc400-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc400-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc400-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc400-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc400-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bc400-128">INPUTS</span></span>

## <span data-ttu-id="bc400-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bc400-129">OUTPUTS</span></span>

### <span data-ttu-id="bc400-130">AzureStack 的系統管理員. 系統管理模型。</span><span class="sxs-lookup"><span data-stu-id="bc400-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="bc400-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bc400-131">NOTES</span></span>

## <span data-ttu-id="bc400-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc400-132">RELATED LINKS</span></span>
