---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0390c3f55c444b4a0e37e25c93536b60d10bc7b1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793463"
---
# <span data-ttu-id="3eddd-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="3eddd-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="3eddd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3eddd-102">SYNOPSIS</span></span>
<span data-ttu-id="3eddd-103">建立新的虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="3eddd-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="3eddd-104">句法</span><span class="sxs-lookup"><span data-stu-id="3eddd-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eddd-105">說明</span><span class="sxs-lookup"><span data-stu-id="3eddd-105">DESCRIPTION</span></span>
<span data-ttu-id="3eddd-106">建立虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="3eddd-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="3eddd-107">示例</span><span class="sxs-lookup"><span data-stu-id="3eddd-107">EXAMPLES</span></span>

### <span data-ttu-id="3eddd-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3eddd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="3eddd-109">新增平臺影像延伸。</span><span class="sxs-lookup"><span data-stu-id="3eddd-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="3eddd-110">參數</span><span class="sxs-lookup"><span data-stu-id="3eddd-110">PARAMETERS</span></span>

### <span data-ttu-id="3eddd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eddd-111">-AsJob</span></span>
<span data-ttu-id="3eddd-112">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="3eddd-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3eddd-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="3eddd-113">-ComputeRole</span></span>
<span data-ttu-id="3eddd-114">此延伸支援的角色、IaaS 或 PaaS 類型。</span><span class="sxs-lookup"><span data-stu-id="3eddd-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="3eddd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3eddd-115">-Force</span></span>
<span data-ttu-id="3eddd-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="3eddd-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3eddd-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="3eddd-117">-IsSystemExtension</span></span>
<span data-ttu-id="3eddd-118">表示系統是否有延伸。</span><span class="sxs-lookup"><span data-stu-id="3eddd-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="3eddd-119">-位置</span><span class="sxs-lookup"><span data-stu-id="3eddd-119">-Location</span></span>
<span data-ttu-id="3eddd-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="3eddd-120">Location of the resource.</span></span>

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

### <span data-ttu-id="3eddd-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3eddd-121">-Publisher</span></span>
<span data-ttu-id="3eddd-122">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3eddd-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="3eddd-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="3eddd-123">-SourceBlob</span></span>
<span data-ttu-id="3eddd-124">虛擬機器延伸套件的 URI。</span><span class="sxs-lookup"><span data-stu-id="3eddd-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eddd-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="3eddd-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="3eddd-126">如果支援多個延伸，則為 True。</span><span class="sxs-lookup"><span data-stu-id="3eddd-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="3eddd-127">-類型</span><span class="sxs-lookup"><span data-stu-id="3eddd-127">-Type</span></span>
<span data-ttu-id="3eddd-128">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="3eddd-128">Type of extension.</span></span>

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

### <span data-ttu-id="3eddd-129">-版本</span><span class="sxs-lookup"><span data-stu-id="3eddd-129">-Version</span></span>
<span data-ttu-id="3eddd-130">Vritual 電腦影像副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="3eddd-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="3eddd-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="3eddd-131">-VmOsType</span></span>
<span data-ttu-id="3eddd-132">部署擴充處理常式所需的目標虛擬機器作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="3eddd-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="3eddd-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="3eddd-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="3eddd-134">指示是否已針對虛擬電腦縮放設定支援啟用延伸的值。</span><span class="sxs-lookup"><span data-stu-id="3eddd-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="3eddd-135">-確認</span><span class="sxs-lookup"><span data-stu-id="3eddd-135">-Confirm</span></span>
<span data-ttu-id="3eddd-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3eddd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eddd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eddd-137">-WhatIf</span></span>
<span data-ttu-id="3eddd-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3eddd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eddd-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3eddd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eddd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eddd-140">CommonParameters</span></span>
<span data-ttu-id="3eddd-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3eddd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eddd-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3eddd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eddd-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3eddd-143">INPUTS</span></span>

## <span data-ttu-id="3eddd-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3eddd-144">OUTPUTS</span></span>

### <span data-ttu-id="3eddd-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="3eddd-145">VmExtensionObject</span></span>

## <span data-ttu-id="3eddd-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3eddd-146">NOTES</span></span>

## <span data-ttu-id="3eddd-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eddd-147">RELATED LINKS</span></span>

