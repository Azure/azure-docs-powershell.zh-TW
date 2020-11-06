---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: fbf9d8c38c10465c565e40a284171b3232ba2949
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453579"
---
# <span data-ttu-id="68917-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="68917-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="68917-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68917-102">SYNOPSIS</span></span>
<span data-ttu-id="68917-103">將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="68917-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68917-104">句法</span><span class="sxs-lookup"><span data-stu-id="68917-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68917-105">說明</span><span class="sxs-lookup"><span data-stu-id="68917-105">DESCRIPTION</span></span>
<span data-ttu-id="68917-106">**AzureRmVmssExtension** Cmdlet 會將延伸 (VMSS 的虛擬電腦規模集新增至 [) ]。</span><span class="sxs-lookup"><span data-stu-id="68917-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="68917-107">示例</span><span class="sxs-lookup"><span data-stu-id="68917-107">EXAMPLES</span></span>

### <span data-ttu-id="68917-108">範例1：在 VMSS 中新增副檔名</span><span class="sxs-lookup"><span data-stu-id="68917-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="68917-109">這個命令會將延伸新增至 VMMS。</span><span class="sxs-lookup"><span data-stu-id="68917-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="68917-110">參數</span><span class="sxs-lookup"><span data-stu-id="68917-110">PARAMETERS</span></span>

### <span data-ttu-id="68917-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="68917-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="68917-112">指出延伸版本是否應該自動更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="68917-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68917-113">-DefaultProfile</span></span>
<span data-ttu-id="68917-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68917-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68917-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="68917-115">-ForceUpdateTag</span></span>
<span data-ttu-id="68917-116">如果提供值且與前一個值不同，延伸處理常式將被迫更新，即使延伸設定尚未變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="68917-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="68917-117">-Name</span></span>
<span data-ttu-id="68917-118">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="68917-118">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="68917-119">-ProtectedSetting</span></span>
<span data-ttu-id="68917-120">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="68917-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="68917-121">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="68917-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="68917-122">-Publisher</span></span>
<span data-ttu-id="68917-123">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="68917-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="68917-124">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="68917-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="68917-125">這可以使用 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) Cmdlet 來取得發行者。</span><span class="sxs-lookup"><span data-stu-id="68917-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-126">-設定</span><span class="sxs-lookup"><span data-stu-id="68917-126">-Setting</span></span>
<span data-ttu-id="68917-127">指定副檔名的公用配置（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="68917-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="68917-128">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="68917-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-129">-類型</span><span class="sxs-lookup"><span data-stu-id="68917-129">-Type</span></span>
<span data-ttu-id="68917-130">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="68917-130">Specifies the extension type.</span></span>
<span data-ttu-id="68917-131">您可以使用 [AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) Cmdlet 來取得延伸類型。</span><span class="sxs-lookup"><span data-stu-id="68917-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="68917-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="68917-133">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="68917-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="68917-134">您可以使用 [AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) Cmdlet 來取得副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="68917-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68917-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="68917-136">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="68917-136">Specify the VMSS object.</span></span>
<span data-ttu-id="68917-137">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="68917-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68917-138">-確認</span><span class="sxs-lookup"><span data-stu-id="68917-138">-Confirm</span></span>
<span data-ttu-id="68917-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68917-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68917-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68917-140">-WhatIf</span></span>
<span data-ttu-id="68917-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68917-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68917-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68917-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68917-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68917-143">CommonParameters</span></span>
<span data-ttu-id="68917-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68917-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68917-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68917-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68917-146">輸入</span><span class="sxs-lookup"><span data-stu-id="68917-146">INPUTS</span></span>

## <span data-ttu-id="68917-147">輸出</span><span class="sxs-lookup"><span data-stu-id="68917-147">OUTPUTS</span></span>

###  
<span data-ttu-id="68917-148">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="68917-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="68917-149">筆記</span><span class="sxs-lookup"><span data-stu-id="68917-149">NOTES</span></span>

## <span data-ttu-id="68917-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="68917-150">RELATED LINKS</span></span>

[<span data-ttu-id="68917-151">移除-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="68917-151">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="68917-152">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="68917-152">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="68917-153">AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="68917-153">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="68917-154">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="68917-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="68917-155">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="68917-155">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
