---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7eac7b9d23914aa909a111958d64cc9d4247d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968077"
---
# <span data-ttu-id="f3a8b-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="f3a8b-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="f3a8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a8b-103">傳回目前可用的虛擬機器影像延伸。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-103">Returns virtual machine image extensions currently available.</span></span>

## <span data-ttu-id="f3a8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3a8b-104">SYNTAX</span></span>

### <span data-ttu-id="f3a8b-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f3a8b-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Publisher <String>] [-Type <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="f3a8b-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f3a8b-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3a8b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3a8b-107">ResourceId</span></span>
```
Get-AzsVMExtension -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f3a8b-108">說明</span><span class="sxs-lookup"><span data-stu-id="f3a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="f3a8b-109">傳回虛擬機器影像延伸。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-109">Returns virtual machine image extensions.</span></span>

## <span data-ttu-id="f3a8b-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="f3a8b-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3a8b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVMExtension
```

<span data-ttu-id="f3a8b-112">取得某個位置的所有 VM 延伸。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-112">Get all VM extensions at a location.</span></span>

### <span data-ttu-id="f3a8b-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3a8b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="f3a8b-114">取得特定的 VM 延伸。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-114">Get specific VM extension.</span></span>

## <span data-ttu-id="f3a8b-115">參數</span><span class="sxs-lookup"><span data-stu-id="f3a8b-115">PARAMETERS</span></span>

### <span data-ttu-id="f3a8b-116">-位置</span><span class="sxs-lookup"><span data-stu-id="f3a8b-116">-Location</span></span>
<span data-ttu-id="f3a8b-117">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-117">Location of the resource.</span></span>

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

### <span data-ttu-id="f3a8b-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f3a8b-118">-Publisher</span></span>
<span data-ttu-id="f3a8b-119">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-119">Name of the publisher.</span></span>

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

### <span data-ttu-id="f3a8b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3a8b-120">-ResourceId</span></span>
<span data-ttu-id="f3a8b-121">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-121">The resource id.</span></span>

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

### <span data-ttu-id="f3a8b-122">-類型</span><span class="sxs-lookup"><span data-stu-id="f3a8b-122">-Type</span></span>
<span data-ttu-id="f3a8b-123">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-123">Type of extension.</span></span>

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

### <span data-ttu-id="f3a8b-124">-版本</span><span class="sxs-lookup"><span data-stu-id="f3a8b-124">-Version</span></span>
<span data-ttu-id="f3a8b-125">虛擬機器影像副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-125">The version of the virtual machine image extension.</span></span>

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

### <span data-ttu-id="f3a8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a8b-126">CommonParameters</span></span>
<span data-ttu-id="f3a8b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a8b-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3a8b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a8b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f3a8b-129">INPUTS</span></span>

## <span data-ttu-id="f3a8b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f3a8b-130">OUTPUTS</span></span>

### <span data-ttu-id="f3a8b-131">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="f3a8b-131">VmExtensionObject</span></span>

## <span data-ttu-id="f3a8b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f3a8b-132">NOTES</span></span>

## <span data-ttu-id="f3a8b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3a8b-133">RELATED LINKS</span></span>
