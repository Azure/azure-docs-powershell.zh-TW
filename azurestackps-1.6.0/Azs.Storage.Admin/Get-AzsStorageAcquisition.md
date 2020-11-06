---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442943"
---
# <span data-ttu-id="0f863-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="0f863-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="0f863-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f863-102">SYNOPSIS</span></span>
<span data-ttu-id="0f863-103">傳回 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="0f863-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="0f863-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f863-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f863-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f863-105">DESCRIPTION</span></span>
<span data-ttu-id="0f863-106">傳回 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="0f863-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="0f863-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f863-107">EXAMPLES</span></span>

### <span data-ttu-id="0f863-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f863-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="0f863-109">取得 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="0f863-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="0f863-110">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f863-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="0f863-111">取得 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="0f863-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="0f863-112">參數</span><span class="sxs-lookup"><span data-stu-id="0f863-112">PARAMETERS</span></span>

### <span data-ttu-id="0f863-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="0f863-113">-FarmName</span></span>
<span data-ttu-id="0f863-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="0f863-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f863-115">-篩選</span><span class="sxs-lookup"><span data-stu-id="0f863-115">-Filter</span></span>
<span data-ttu-id="0f863-116">篩選字串</span><span class="sxs-lookup"><span data-stu-id="0f863-116">Filter string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f863-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f863-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f863-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0f863-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f863-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f863-119">CommonParameters</span></span>
<span data-ttu-id="0f863-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f863-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f863-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f863-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f863-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0f863-122">INPUTS</span></span>

## <span data-ttu-id="0f863-123">輸出</span><span class="sxs-lookup"><span data-stu-id="0f863-123">OUTPUTS</span></span>

## <span data-ttu-id="0f863-124">筆記</span><span class="sxs-lookup"><span data-stu-id="0f863-124">NOTES</span></span>

## <span data-ttu-id="0f863-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f863-125">RELATED LINKS</span></span>

