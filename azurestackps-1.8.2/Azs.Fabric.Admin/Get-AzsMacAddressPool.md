---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e22024b1b246a60104db0832860ed0aff699ff5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968067"
---
# <span data-ttu-id="06ee1-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="06ee1-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="06ee1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="06ee1-103">傳回位於某個位置的所有 MAC 位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="06ee1-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="06ee1-104">句法</span><span class="sxs-lookup"><span data-stu-id="06ee1-104">SYNTAX</span></span>

### <span data-ttu-id="06ee1-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="06ee1-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="06ee1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="06ee1-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="06ee1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="06ee1-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="06ee1-108">說明</span><span class="sxs-lookup"><span data-stu-id="06ee1-108">DESCRIPTION</span></span>
<span data-ttu-id="06ee1-109">傳回位於某個位置的所有 MAC 位址集區清單。</span><span class="sxs-lookup"><span data-stu-id="06ee1-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="06ee1-110">示例</span><span class="sxs-lookup"><span data-stu-id="06ee1-110">EXAMPLES</span></span>

### <span data-ttu-id="06ee1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="06ee1-111">EXAMPLE 1</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="06ee1-112">取得某個位置的所有 MAC 位址集區。</span><span class="sxs-lookup"><span data-stu-id="06ee1-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="06ee1-113">範例2</span><span class="sxs-lookup"><span data-stu-id="06ee1-113">EXAMPLE 2</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="06ee1-114">根據名稱在位置取得特定的 MAC 位址集區。</span><span class="sxs-lookup"><span data-stu-id="06ee1-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="06ee1-115">參數</span><span class="sxs-lookup"><span data-stu-id="06ee1-115">PARAMETERS</span></span>

### <span data-ttu-id="06ee1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="06ee1-116">-Name</span></span>
<span data-ttu-id="06ee1-117">MAC 位址集區的名稱。</span><span class="sxs-lookup"><span data-stu-id="06ee1-117">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="06ee1-118">-位置</span><span class="sxs-lookup"><span data-stu-id="06ee1-118">-Location</span></span>
<span data-ttu-id="06ee1-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="06ee1-119">Location of the resource.</span></span>

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

### <span data-ttu-id="06ee1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ee1-120">-ResourceGroupName</span></span>
<span data-ttu-id="06ee1-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="06ee1-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="06ee1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06ee1-122">-ResourceId</span></span>
<span data-ttu-id="06ee1-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="06ee1-123">The resource id.</span></span>

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

### <span data-ttu-id="06ee1-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="06ee1-124">-Filter</span></span>
<span data-ttu-id="06ee1-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="06ee1-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ee1-126">-略過</span><span class="sxs-lookup"><span data-stu-id="06ee1-126">-Skip</span></span>
<span data-ttu-id="06ee1-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="06ee1-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="06ee1-128">-上方</span><span class="sxs-lookup"><span data-stu-id="06ee1-128">-Top</span></span>
<span data-ttu-id="06ee1-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="06ee1-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="06ee1-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="06ee1-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="06ee1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ee1-131">CommonParameters</span></span>
<span data-ttu-id="06ee1-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06ee1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ee1-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06ee1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ee1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="06ee1-134">INPUTS</span></span>

## <span data-ttu-id="06ee1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="06ee1-135">OUTPUTS</span></span>

### <span data-ttu-id="06ee1-136">MacAddressPool 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="06ee1-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="06ee1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="06ee1-137">NOTES</span></span>

## <span data-ttu-id="06ee1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="06ee1-138">RELATED LINKS</span></span>
