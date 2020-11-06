---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444764"
---
# <span data-ttu-id="2e386-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2e386-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="2e386-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e386-102">SYNOPSIS</span></span>
<span data-ttu-id="2e386-103">將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="2e386-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e386-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e386-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e386-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e386-105">DESCRIPTION</span></span>
<span data-ttu-id="2e386-106">**AzureRmVmssExtension** Cmdlet 會將延伸 (VMSS 的虛擬電腦規模集新增至 [) ]。</span><span class="sxs-lookup"><span data-stu-id="2e386-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="2e386-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e386-107">EXAMPLES</span></span>

### <span data-ttu-id="2e386-108">範例1：在 VMSS 中新增副檔名</span><span class="sxs-lookup"><span data-stu-id="2e386-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="2e386-109">這個命令會將延伸新增至 VMMS。</span><span class="sxs-lookup"><span data-stu-id="2e386-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="2e386-110">參數</span><span class="sxs-lookup"><span data-stu-id="2e386-110">PARAMETERS</span></span>

### <span data-ttu-id="2e386-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2e386-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2e386-112">指出延伸版本是否應該自動更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="2e386-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="2e386-113">-Name</span></span>
<span data-ttu-id="2e386-114">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e386-114">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2e386-115">-ProtectedSetting</span></span>
<span data-ttu-id="2e386-116">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="2e386-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="2e386-117">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="2e386-117">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2e386-118">-Publisher</span></span>
<span data-ttu-id="2e386-119">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2e386-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="2e386-120">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="2e386-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="2e386-121">這可以使用 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) Cmdlet 來取得發行者。</span><span class="sxs-lookup"><span data-stu-id="2e386-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-122">-設定</span><span class="sxs-lookup"><span data-stu-id="2e386-122">-Setting</span></span>
<span data-ttu-id="2e386-123">指定副檔名的公用配置（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="2e386-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="2e386-124">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="2e386-124">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-125">-類型</span><span class="sxs-lookup"><span data-stu-id="2e386-125">-Type</span></span>
<span data-ttu-id="2e386-126">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="2e386-126">Specifies the extension type.</span></span>
<span data-ttu-id="2e386-127">您可以使用 [AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) Cmdlet 來取得延伸類型。</span><span class="sxs-lookup"><span data-stu-id="2e386-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2e386-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="2e386-129">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="2e386-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2e386-130">您可以使用 [AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) Cmdlet 來取得副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="2e386-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2e386-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2e386-132">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="2e386-132">Specify the VMSS object.</span></span>
<span data-ttu-id="2e386-133">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="2e386-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e386-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2e386-134">-Confirm</span></span>
<span data-ttu-id="2e386-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2e386-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e386-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e386-136">-WhatIf</span></span>
<span data-ttu-id="2e386-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e386-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e386-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e386-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e386-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e386-139">CommonParameters</span></span>
<span data-ttu-id="2e386-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e386-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e386-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e386-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e386-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2e386-142">INPUTS</span></span>

### <span data-ttu-id="2e386-143">所有</span><span class="sxs-lookup"><span data-stu-id="2e386-143">None</span></span>
<span data-ttu-id="2e386-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2e386-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e386-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2e386-145">OUTPUTS</span></span>

###  
<span data-ttu-id="2e386-146">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2e386-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="2e386-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2e386-147">NOTES</span></span>

## <span data-ttu-id="2e386-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e386-148">RELATED LINKS</span></span>

[<span data-ttu-id="2e386-149">移除-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2e386-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="2e386-150">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2e386-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="2e386-151">AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="2e386-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="2e386-152">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="2e386-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="2e386-153">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2e386-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
