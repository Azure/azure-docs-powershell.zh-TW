---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5d94fdb44a5e37988853c95de794d67fcb26a515
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793608"
---
# <span data-ttu-id="548f2-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="548f2-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="548f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="548f2-102">SYNOPSIS</span></span>
<span data-ttu-id="548f2-103">取得更新位置清單。</span><span class="sxs-lookup"><span data-stu-id="548f2-103">Get the list of update locations.</span></span>

## <span data-ttu-id="548f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="548f2-104">SYNTAX</span></span>

### <span data-ttu-id="548f2-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="548f2-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="548f2-106">獲取</span><span class="sxs-lookup"><span data-stu-id="548f2-106">Get</span></span>
```
Get-AzsUpdateLocation [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="548f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="548f2-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="548f2-108">說明</span><span class="sxs-lookup"><span data-stu-id="548f2-108">DESCRIPTION</span></span>
<span data-ttu-id="548f2-109">取得更新位置清單。</span><span class="sxs-lookup"><span data-stu-id="548f2-109">Get the list of update locations.</span></span> <span data-ttu-id="548f2-110">傳回的位置可以使用 AzsUpdate，在特定位置取得可用的更新。</span><span class="sxs-lookup"><span data-stu-id="548f2-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="548f2-111">示例</span><span class="sxs-lookup"><span data-stu-id="548f2-111">EXAMPLES</span></span>

### <span data-ttu-id="548f2-112">範例1</span><span class="sxs-lookup"><span data-stu-id="548f2-112">EXAMPLE 1</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="548f2-113">取得更新位置清單。</span><span class="sxs-lookup"><span data-stu-id="548f2-113">Get the list of update locations.</span></span>

## <span data-ttu-id="548f2-114">參數</span><span class="sxs-lookup"><span data-stu-id="548f2-114">PARAMETERS</span></span>

### <span data-ttu-id="548f2-115">-位置</span><span class="sxs-lookup"><span data-stu-id="548f2-115">-Location</span></span>
<span data-ttu-id="548f2-116">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="548f2-116">Name of the Location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="548f2-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="548f2-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="548f2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="548f2-119">-ResourceId</span></span>
<span data-ttu-id="548f2-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="548f2-120">The resource id.</span></span>

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

### <span data-ttu-id="548f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548f2-121">CommonParameters</span></span>
<span data-ttu-id="548f2-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="548f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548f2-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="548f2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548f2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="548f2-124">INPUTS</span></span>

## <span data-ttu-id="548f2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="548f2-125">OUTPUTS</span></span>

### <span data-ttu-id="548f2-126">AzureStack （UpdateLocation）的</span><span class="sxs-lookup"><span data-stu-id="548f2-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="548f2-127">筆記</span><span class="sxs-lookup"><span data-stu-id="548f2-127">NOTES</span></span>

## <span data-ttu-id="548f2-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="548f2-128">RELATED LINKS</span></span>
