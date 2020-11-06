---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42181271e9295212f256cfc519e8ecc32eeae048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443135"
---
# <span data-ttu-id="3a126-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="3a126-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="3a126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a126-102">SYNOPSIS</span></span>
<span data-ttu-id="3a126-103">建立新的虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="3a126-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="3a126-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a126-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a126-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a126-105">DESCRIPTION</span></span>
<span data-ttu-id="3a126-106">建立虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="3a126-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="3a126-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a126-107">EXAMPLES</span></span>

### <span data-ttu-id="3a126-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a126-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="3a126-109">新增平臺影像延伸。</span><span class="sxs-lookup"><span data-stu-id="3a126-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="3a126-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a126-110">PARAMETERS</span></span>

### <span data-ttu-id="3a126-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a126-111">-AsJob</span></span>
<span data-ttu-id="3a126-112">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="3a126-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3a126-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="3a126-113">-ComputeRole</span></span>
<span data-ttu-id="3a126-114">此延伸支援的角色、IaaS 或 PaaS 類型。</span><span class="sxs-lookup"><span data-stu-id="3a126-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

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

### <span data-ttu-id="3a126-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3a126-115">-Force</span></span>
<span data-ttu-id="3a126-116">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="3a126-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3a126-117">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="3a126-117">-IsSystemExtension</span></span>
<span data-ttu-id="3a126-118">表示系統是否有延伸。</span><span class="sxs-lookup"><span data-stu-id="3a126-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="3a126-119">-位置</span><span class="sxs-lookup"><span data-stu-id="3a126-119">-Location</span></span>
<span data-ttu-id="3a126-120">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="3a126-120">Location of the resource.</span></span>

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

### <span data-ttu-id="3a126-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3a126-121">-Publisher</span></span>
<span data-ttu-id="3a126-122">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a126-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="3a126-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="3a126-123">-SourceBlob</span></span>
<span data-ttu-id="3a126-124">虛擬機器延伸套件的 URI。</span><span class="sxs-lookup"><span data-stu-id="3a126-124">URI to virtual machine extension package.</span></span>

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

### <span data-ttu-id="3a126-125">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="3a126-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="3a126-126">如果支援多個延伸，則為 True。</span><span class="sxs-lookup"><span data-stu-id="3a126-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="3a126-127">-類型</span><span class="sxs-lookup"><span data-stu-id="3a126-127">-Type</span></span>
<span data-ttu-id="3a126-128">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="3a126-128">Type of extension.</span></span>

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

### <span data-ttu-id="3a126-129">-版本</span><span class="sxs-lookup"><span data-stu-id="3a126-129">-Version</span></span>
<span data-ttu-id="3a126-130">Vritual 電腦影像副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="3a126-130">The version of the vritual machine image extension.</span></span>

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

### <span data-ttu-id="3a126-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="3a126-131">-VmOsType</span></span>
<span data-ttu-id="3a126-132">部署擴充處理常式所需的目標虛擬機器作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="3a126-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

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

### <span data-ttu-id="3a126-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="3a126-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="3a126-134">指示是否已針對虛擬電腦縮放設定支援啟用延伸的值。</span><span class="sxs-lookup"><span data-stu-id="3a126-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="3a126-135">-確認</span><span class="sxs-lookup"><span data-stu-id="3a126-135">-Confirm</span></span>
<span data-ttu-id="3a126-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a126-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a126-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a126-137">-WhatIf</span></span>
<span data-ttu-id="3a126-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a126-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a126-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a126-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a126-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a126-140">CommonParameters</span></span>
<span data-ttu-id="3a126-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a126-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a126-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a126-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a126-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3a126-143">INPUTS</span></span>

## <span data-ttu-id="3a126-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3a126-144">OUTPUTS</span></span>

### <span data-ttu-id="3a126-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="3a126-145">VmExtensionObject</span></span>

## <span data-ttu-id="3a126-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3a126-146">NOTES</span></span>

## <span data-ttu-id="3a126-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a126-147">RELATED LINKS</span></span>

