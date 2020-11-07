---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f8c9192100536a04b664f981a9df9e1508a1f87
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968359"
---
# <span data-ttu-id="3837e-101">Get-AzsStorageShare</span><span class="sxs-lookup"><span data-stu-id="3837e-101">Get-AzsStorageShare</span></span>

## <span data-ttu-id="3837e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3837e-102">SYNOPSIS</span></span>
<span data-ttu-id="3837e-103">傳回儲存空間共用的清單。</span><span class="sxs-lookup"><span data-stu-id="3837e-103">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3837e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3837e-104">SYNTAX</span></span>

### <span data-ttu-id="3837e-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="3837e-105">List (Default)</span></span>
```
Get-AzsStorageShare -FarmName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3837e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3837e-106">Get</span></span>
```
Get-AzsStorageShare -FarmName <String> -ShareName <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3837e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3837e-107">ResourceId</span></span>
```
Get-AzsStorageShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3837e-108">說明</span><span class="sxs-lookup"><span data-stu-id="3837e-108">DESCRIPTION</span></span>
<span data-ttu-id="3837e-109">傳回儲存空間共用的清單。</span><span class="sxs-lookup"><span data-stu-id="3837e-109">Returns a list of storage shares.</span></span>

## <span data-ttu-id="3837e-110">示例</span><span class="sxs-lookup"><span data-stu-id="3837e-110">EXAMPLES</span></span>

### <span data-ttu-id="3837e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3837e-111">EXAMPLE 1</span></span>
```
Get-AzsStorageShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="3837e-112">取得儲存空間共用的清單。</span><span class="sxs-lookup"><span data-stu-id="3837e-112">Get the list of storage shares.</span></span>

## <span data-ttu-id="3837e-113">參數</span><span class="sxs-lookup"><span data-stu-id="3837e-113">PARAMETERS</span></span>

### <span data-ttu-id="3837e-114">-FarmName</span><span class="sxs-lookup"><span data-stu-id="3837e-114">-FarmName</span></span>
<span data-ttu-id="3837e-115">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="3837e-115">Farm Id.</span></span>

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

### <span data-ttu-id="3837e-116">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="3837e-116">-ShareName</span></span>
<span data-ttu-id="3837e-117">[共用名稱稱]。</span><span class="sxs-lookup"><span data-stu-id="3837e-117">Share name.</span></span>

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

### <span data-ttu-id="3837e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3837e-118">-ResourceGroupName</span></span>
<span data-ttu-id="3837e-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3837e-119">Resource group name.</span></span>

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

### <span data-ttu-id="3837e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3837e-120">-ResourceId</span></span>
<span data-ttu-id="3837e-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="3837e-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3837e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3837e-122">CommonParameters</span></span>
<span data-ttu-id="3837e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3837e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3837e-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3837e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3837e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="3837e-125">INPUTS</span></span>

## <span data-ttu-id="3837e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="3837e-126">OUTPUTS</span></span>

### <span data-ttu-id="3837e-127">AzureStack 的 [系統管理]。共用</span><span class="sxs-lookup"><span data-stu-id="3837e-127">Microsoft.AzureStack.Management.Storage.Admin.Models.Share</span></span>

## <span data-ttu-id="3837e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="3837e-128">NOTES</span></span>

## <span data-ttu-id="3837e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="3837e-129">RELATED LINKS</span></span>
