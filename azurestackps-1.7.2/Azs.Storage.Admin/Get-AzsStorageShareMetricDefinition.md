---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793228"
---
# <span data-ttu-id="99790-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="99790-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="99790-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99790-102">SYNOPSIS</span></span>
<span data-ttu-id="99790-103">傳回儲存空間共用的度量值定義清單。</span><span class="sxs-lookup"><span data-stu-id="99790-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="99790-104">句法</span><span class="sxs-lookup"><span data-stu-id="99790-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="99790-105">說明</span><span class="sxs-lookup"><span data-stu-id="99790-105">DESCRIPTION</span></span>
<span data-ttu-id="99790-106">傳回儲存空間共用的度量值定義清單。</span><span class="sxs-lookup"><span data-stu-id="99790-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="99790-107">示例</span><span class="sxs-lookup"><span data-stu-id="99790-107">EXAMPLES</span></span>

### <span data-ttu-id="99790-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="99790-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="99790-109">取得儲存空間共用的度量定義清單。</span><span class="sxs-lookup"><span data-stu-id="99790-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="99790-110">參數</span><span class="sxs-lookup"><span data-stu-id="99790-110">PARAMETERS</span></span>

### <span data-ttu-id="99790-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="99790-111">-FarmName</span></span>
<span data-ttu-id="99790-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="99790-112">Farm Id.</span></span>

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

### <span data-ttu-id="99790-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="99790-113">-Name</span></span>
<span data-ttu-id="99790-114">[共用名稱稱]。</span><span class="sxs-lookup"><span data-stu-id="99790-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99790-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99790-115">-ResourceGroupName</span></span>
<span data-ttu-id="99790-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="99790-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99790-117">-略過</span><span class="sxs-lookup"><span data-stu-id="99790-117">-Skip</span></span>
<span data-ttu-id="99790-118">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="99790-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99790-119">-上方</span><span class="sxs-lookup"><span data-stu-id="99790-119">-Top</span></span>
<span data-ttu-id="99790-120">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="99790-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="99790-121">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="99790-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99790-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99790-122">CommonParameters</span></span>
<span data-ttu-id="99790-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99790-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99790-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99790-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99790-125">輸入</span><span class="sxs-lookup"><span data-stu-id="99790-125">INPUTS</span></span>

## <span data-ttu-id="99790-126">輸出</span><span class="sxs-lookup"><span data-stu-id="99790-126">OUTPUTS</span></span>

### <span data-ttu-id="99790-127">AzureStack （MetricDefinition）的</span><span class="sxs-lookup"><span data-stu-id="99790-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="99790-128">筆記</span><span class="sxs-lookup"><span data-stu-id="99790-128">NOTES</span></span>

## <span data-ttu-id="99790-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="99790-129">RELATED LINKS</span></span>

