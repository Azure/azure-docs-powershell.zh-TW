---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9234cb73b1f9c3652827293ae2813f78d7ce336
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611573"
---
# <span data-ttu-id="59ffe-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="59ffe-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="59ffe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="59ffe-103">取得更新位置清單。</span><span class="sxs-lookup"><span data-stu-id="59ffe-103">Get the list of update locations.</span></span>

## <span data-ttu-id="59ffe-104">句法</span><span class="sxs-lookup"><span data-stu-id="59ffe-104">SYNTAX</span></span>

### <span data-ttu-id="59ffe-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="59ffe-105">List (Default)</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="59ffe-106">獲取</span><span class="sxs-lookup"><span data-stu-id="59ffe-106">Get</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="59ffe-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59ffe-107">ResourceId</span></span>
```
Get-AzsUpdateLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="59ffe-108">說明</span><span class="sxs-lookup"><span data-stu-id="59ffe-108">DESCRIPTION</span></span>
<span data-ttu-id="59ffe-109">取得更新位置清單。</span><span class="sxs-lookup"><span data-stu-id="59ffe-109">Get the list of update locations.</span></span> <span data-ttu-id="59ffe-110">傳回的位置可以使用 AzsUpdate，在特定位置取得可用的更新。</span><span class="sxs-lookup"><span data-stu-id="59ffe-110">The locations returned can be used to get available updates at a particular location using Get-AzsUpdate.</span></span>

## <span data-ttu-id="59ffe-111">示例</span><span class="sxs-lookup"><span data-stu-id="59ffe-111">EXAMPLES</span></span>

### <span data-ttu-id="59ffe-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="59ffe-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateLocation
```

<span data-ttu-id="59ffe-113">取得更新位置清單。</span><span class="sxs-lookup"><span data-stu-id="59ffe-113">Get the list of update locations.</span></span>

## <span data-ttu-id="59ffe-114">參數</span><span class="sxs-lookup"><span data-stu-id="59ffe-114">PARAMETERS</span></span>

### <span data-ttu-id="59ffe-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="59ffe-115">-Name</span></span>
<span data-ttu-id="59ffe-116">更新位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="59ffe-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ffe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ffe-117">-ResourceGroupName</span></span>
<span data-ttu-id="59ffe-118">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="59ffe-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="59ffe-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59ffe-119">-ResourceId</span></span>
<span data-ttu-id="59ffe-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="59ffe-120">The resource id.</span></span>

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

### <span data-ttu-id="59ffe-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ffe-121">CommonParameters</span></span>
<span data-ttu-id="59ffe-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59ffe-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ffe-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59ffe-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ffe-124">輸入</span><span class="sxs-lookup"><span data-stu-id="59ffe-124">INPUTS</span></span>

## <span data-ttu-id="59ffe-125">輸出</span><span class="sxs-lookup"><span data-stu-id="59ffe-125">OUTPUTS</span></span>

### <span data-ttu-id="59ffe-126">AzureStack （UpdateLocation）的</span><span class="sxs-lookup"><span data-stu-id="59ffe-126">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateLocation</span></span>

## <span data-ttu-id="59ffe-127">筆記</span><span class="sxs-lookup"><span data-stu-id="59ffe-127">NOTES</span></span>

## <span data-ttu-id="59ffe-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="59ffe-128">RELATED LINKS</span></span>

