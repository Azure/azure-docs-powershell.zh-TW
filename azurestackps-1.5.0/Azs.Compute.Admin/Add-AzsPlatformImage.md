---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ec1f3e70752a5386cd5dad78d867da68091b96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443136"
---
# <span data-ttu-id="25218-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="25218-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="25218-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25218-102">SYNOPSIS</span></span>
<span data-ttu-id="25218-103">從指定的影像配置新增虛擬機器平臺影像。</span><span class="sxs-lookup"><span data-stu-id="25218-103">Add a virtual machine platform image from a given image configuration.</span></span>

## <span data-ttu-id="25218-104">句法</span><span class="sxs-lookup"><span data-stu-id="25218-104">SYNTAX</span></span>

```
Add-AzsPlatformImage [-Publisher] <String> [-Offer] <String> [-Sku] <String> [-Version] <String>
 [-OsType] <Object> [-OsUri] <String> [[-BillingPartNumber] <String>] [[-DataDisks] <DataDisk[]>]
 [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25218-105">說明</span><span class="sxs-lookup"><span data-stu-id="25218-105">DESCRIPTION</span></span>
<span data-ttu-id="25218-106">新增平臺影像。</span><span class="sxs-lookup"><span data-stu-id="25218-106">Add a platform image.</span></span>

## <span data-ttu-id="25218-107">示例</span><span class="sxs-lookup"><span data-stu-id="25218-107">EXAMPLES</span></span>

### <span data-ttu-id="25218-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="25218-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Sku 16.04-LTS -Version 1.0.0 -OsType "Linux" -OsUri "https://test.blob.local.azurestack.external/test/xenial-server-cloudimg-amd64-disk1.vhd"
```

<span data-ttu-id="25218-109">新增平臺影像。</span><span class="sxs-lookup"><span data-stu-id="25218-109">Add a new platform image.</span></span>

## <span data-ttu-id="25218-110">參數</span><span class="sxs-lookup"><span data-stu-id="25218-110">PARAMETERS</span></span>

### <span data-ttu-id="25218-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25218-111">-AsJob</span></span>
<span data-ttu-id="25218-112">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="25218-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-113">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="25218-113">-BillingPartNumber</span></span>
<span data-ttu-id="25218-114">組件編號是用來帳單軟體成本。</span><span class="sxs-lookup"><span data-stu-id="25218-114">The part number is used to bill for software costs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-115">-DataDisks</span><span class="sxs-lookup"><span data-stu-id="25218-115">-DataDisks</span></span>
<span data-ttu-id="25218-116">平臺影像所使用的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="25218-116">Data disks used by the platform image.</span></span>

```yaml
Type: DataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-117">-Force</span><span class="sxs-lookup"><span data-stu-id="25218-117">-Force</span></span>
<span data-ttu-id="25218-118">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="25218-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-119">-位置</span><span class="sxs-lookup"><span data-stu-id="25218-119">-Location</span></span>
<span data-ttu-id="25218-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="25218-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-121">-優惠</span><span class="sxs-lookup"><span data-stu-id="25218-121">-Offer</span></span>
<span data-ttu-id="25218-122">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="25218-122">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-123">-OsType</span><span class="sxs-lookup"><span data-stu-id="25218-123">-OsType</span></span>
<span data-ttu-id="25218-124">作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="25218-124">Operating system type.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-125">-OsUri</span><span class="sxs-lookup"><span data-stu-id="25218-125">-OsUri</span></span>
<span data-ttu-id="25218-126">磁片的位置。</span><span class="sxs-lookup"><span data-stu-id="25218-126">Location of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="25218-127">-Publisher</span></span>
<span data-ttu-id="25218-128">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="25218-128">Name of the publisher.</span></span>

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

### <span data-ttu-id="25218-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="25218-129">-Sku</span></span>
<span data-ttu-id="25218-130">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="25218-130">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-131">-版本</span><span class="sxs-lookup"><span data-stu-id="25218-131">-Version</span></span>
<span data-ttu-id="25218-132">虛擬機器平臺影像的版本。</span><span class="sxs-lookup"><span data-stu-id="25218-132">The version of the virtual machine platform image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-133">-確認</span><span class="sxs-lookup"><span data-stu-id="25218-133">-Confirm</span></span>
<span data-ttu-id="25218-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25218-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25218-135">-WhatIf</span></span>
<span data-ttu-id="25218-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25218-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25218-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25218-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25218-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25218-138">CommonParameters</span></span>
<span data-ttu-id="25218-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25218-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25218-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25218-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25218-141">輸入</span><span class="sxs-lookup"><span data-stu-id="25218-141">INPUTS</span></span>

## <span data-ttu-id="25218-142">輸出</span><span class="sxs-lookup"><span data-stu-id="25218-142">OUTPUTS</span></span>

### <span data-ttu-id="25218-143">PlatformImageObject</span><span class="sxs-lookup"><span data-stu-id="25218-143">PlatformImageObject</span></span>

## <span data-ttu-id="25218-144">筆記</span><span class="sxs-lookup"><span data-stu-id="25218-144">NOTES</span></span>

## <span data-ttu-id="25218-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="25218-145">RELATED LINKS</span></span>

