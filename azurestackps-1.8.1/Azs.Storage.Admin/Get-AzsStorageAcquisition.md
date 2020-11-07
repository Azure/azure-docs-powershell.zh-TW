---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793936"
---
# <span data-ttu-id="ee4dd-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="ee4dd-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="ee4dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4dd-103">傳回 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="ee4dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee4dd-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee4dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4dd-106">傳回 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="ee4dd-107">示例</span><span class="sxs-lookup"><span data-stu-id="ee4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ee4dd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ee4dd-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ee4dd-109">取得 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="ee4dd-110">範例2</span><span class="sxs-lookup"><span data-stu-id="ee4dd-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="ee4dd-111">取得 blob acquistions 清單。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="ee4dd-112">參數</span><span class="sxs-lookup"><span data-stu-id="ee4dd-112">PARAMETERS</span></span>

### <span data-ttu-id="ee4dd-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="ee4dd-113">-FarmName</span></span>
<span data-ttu-id="ee4dd-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-114">Farm Id.</span></span>

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

### <span data-ttu-id="ee4dd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4dd-115">-ResourceGroupName</span></span>
<span data-ttu-id="ee4dd-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-116">Resource group name.</span></span>

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

### <span data-ttu-id="ee4dd-117">-篩選</span><span class="sxs-lookup"><span data-stu-id="ee4dd-117">-Filter</span></span>
<span data-ttu-id="ee4dd-118">篩選字串</span><span class="sxs-lookup"><span data-stu-id="ee4dd-118">Filter string</span></span>

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

### <span data-ttu-id="ee4dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4dd-119">CommonParameters</span></span>
<span data-ttu-id="ee4dd-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4dd-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee4dd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4dd-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ee4dd-122">INPUTS</span></span>

## <span data-ttu-id="ee4dd-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ee4dd-123">OUTPUTS</span></span>

## <span data-ttu-id="ee4dd-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ee4dd-124">NOTES</span></span>

## <span data-ttu-id="ee4dd-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee4dd-125">RELATED LINKS</span></span>
