---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796362"
---
# <span data-ttu-id="d7dd5-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d7dd5-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="d7dd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d7dd5-103">將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="d7dd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7dd5-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7dd5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="d7dd5-106">**AzVmssExtension** Cmdlet 會將延伸 (VMSS 的虛擬電腦規模集新增至 [) ]。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d7dd5-107">示例</span><span class="sxs-lookup"><span data-stu-id="d7dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="d7dd5-108">範例1：在 VMSS 中新增副檔名</span><span class="sxs-lookup"><span data-stu-id="d7dd5-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="d7dd5-109">這個命令會將延伸新增至 VMMS。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="d7dd5-110">參數</span><span class="sxs-lookup"><span data-stu-id="d7dd5-110">PARAMETERS</span></span>

### <span data-ttu-id="d7dd5-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d7dd5-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d7dd5-112">指出延伸版本是否應該自動更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="d7dd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7dd5-113">-DefaultProfile</span></span>
<span data-ttu-id="d7dd5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd5-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="d7dd5-115">-ForceUpdateTag</span></span>
<span data-ttu-id="d7dd5-116">如果提供值且與前一個值不同，延伸處理常式將被迫更新，即使延伸設定尚未變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7dd5-117">-Name</span></span>
<span data-ttu-id="d7dd5-118">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d7dd5-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d7dd5-119">-ProtectedSetting</span></span>
<span data-ttu-id="d7dd5-120">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="d7dd5-121">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="d7dd5-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d7dd5-122">-Publisher</span></span>
<span data-ttu-id="d7dd5-123">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="d7dd5-124">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="d7dd5-125">這可以使用 [AzVMImagePublisher](./Get-AzVMImagePublisher.md) Cmdlet 來取得發行者。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="d7dd5-126">-設定</span><span class="sxs-lookup"><span data-stu-id="d7dd5-126">-Setting</span></span>
<span data-ttu-id="d7dd5-127">指定副檔名的公用配置（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="d7dd5-128">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="d7dd5-129">-類型</span><span class="sxs-lookup"><span data-stu-id="d7dd5-129">-Type</span></span>
<span data-ttu-id="d7dd5-130">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-130">Specifies the extension type.</span></span>
<span data-ttu-id="d7dd5-131">您可以使用 [AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) Cmdlet 來取得延伸類型。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="d7dd5-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d7dd5-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="d7dd5-133">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d7dd5-134">您可以使用 [AzVMExtensionImage](./Get-AzVMExtensionImage.md) Cmdlet 來取得副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="d7dd5-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7dd5-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d7dd5-136">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-136">Specify the VMSS object.</span></span>
<span data-ttu-id="d7dd5-137">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7dd5-138">-確認</span><span class="sxs-lookup"><span data-stu-id="d7dd5-138">-Confirm</span></span>
<span data-ttu-id="d7dd5-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7dd5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7dd5-140">-WhatIf</span></span>
<span data-ttu-id="d7dd5-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7dd5-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7dd5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7dd5-143">CommonParameters</span></span>
<span data-ttu-id="d7dd5-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7dd5-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7dd5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="d7dd5-146">INPUTS</span></span>

### <span data-ttu-id="d7dd5-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7dd5-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d7dd5-148">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="d7dd5-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d7dd5-149">輸出</span><span class="sxs-lookup"><span data-stu-id="d7dd5-149">OUTPUTS</span></span>

###  
<span data-ttu-id="d7dd5-150">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d7dd5-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d7dd5-151">筆記</span><span class="sxs-lookup"><span data-stu-id="d7dd5-151">NOTES</span></span>

## <span data-ttu-id="d7dd5-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7dd5-152">RELATED LINKS</span></span>

[<span data-ttu-id="d7dd5-153">移除-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="d7dd5-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="d7dd5-154">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d7dd5-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="d7dd5-155">AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="d7dd5-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="d7dd5-156">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d7dd5-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="d7dd5-157">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d7dd5-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
