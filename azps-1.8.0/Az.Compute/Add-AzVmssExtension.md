---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 5caece2430cc69e265747ceb55538549debda638
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622818"
---
# <span data-ttu-id="fde45-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fde45-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="fde45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fde45-102">SYNOPSIS</span></span>
<span data-ttu-id="fde45-103">將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="fde45-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="fde45-104">句法</span><span class="sxs-lookup"><span data-stu-id="fde45-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fde45-105">說明</span><span class="sxs-lookup"><span data-stu-id="fde45-105">DESCRIPTION</span></span>
<span data-ttu-id="fde45-106">**AzVmssExtension** Cmdlet 會將延伸 (VMSS 的虛擬電腦規模集新增至 [) ]。</span><span class="sxs-lookup"><span data-stu-id="fde45-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fde45-107">示例</span><span class="sxs-lookup"><span data-stu-id="fde45-107">EXAMPLES</span></span>

### <span data-ttu-id="fde45-108">範例1：在 VMSS 中新增副檔名</span><span class="sxs-lookup"><span data-stu-id="fde45-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="fde45-109">這個命令會將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="fde45-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="fde45-110">範例2：使用設定和受保護的設定，將延伸新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="fde45-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="fde45-111">這個命令會在 blob 儲存空間上加上含範例 bash 腳本的 VMSS 副檔名，並在 [設定] 和 [安全存取] 中，指定 [受保護的設定] 中的 [blob 儲存] 與 [執行中] 命令</span><span class="sxs-lookup"><span data-stu-id="fde45-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="fde45-112">參數</span><span class="sxs-lookup"><span data-stu-id="fde45-112">PARAMETERS</span></span>

### <span data-ttu-id="fde45-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fde45-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fde45-114">指出延伸版本是否應該自動更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="fde45-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="fde45-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde45-115">-DefaultProfile</span></span>
<span data-ttu-id="fde45-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fde45-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde45-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="fde45-117">-ForceUpdateTag</span></span>
<span data-ttu-id="fde45-118">如果提供值且與前一個值不同，延伸處理常式將被迫更新，即使延伸設定尚未變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="fde45-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="fde45-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fde45-119">-Name</span></span>
<span data-ttu-id="fde45-120">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="fde45-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fde45-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="fde45-121">-ProtectedSetting</span></span>
<span data-ttu-id="fde45-122">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="fde45-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="fde45-123">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="fde45-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="fde45-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="fde45-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="fde45-125">需要預配此延伸的副檔名名稱集合。</span><span class="sxs-lookup"><span data-stu-id="fde45-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fde45-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fde45-126">-Publisher</span></span>
<span data-ttu-id="fde45-127">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="fde45-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="fde45-128">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="fde45-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="fde45-129">這可以使用 [AzVMImagePublisher](./Get-AzVMImagePublisher.md) Cmdlet 來取得發行者。</span><span class="sxs-lookup"><span data-stu-id="fde45-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="fde45-130">-設定</span><span class="sxs-lookup"><span data-stu-id="fde45-130">-Setting</span></span>
<span data-ttu-id="fde45-131">指定副檔名的公用配置（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="fde45-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="fde45-132">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="fde45-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="fde45-133">-類型</span><span class="sxs-lookup"><span data-stu-id="fde45-133">-Type</span></span>
<span data-ttu-id="fde45-134">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="fde45-134">Specifies the extension type.</span></span>
<span data-ttu-id="fde45-135">您可以使用 [AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) Cmdlet 來取得延伸類型。</span><span class="sxs-lookup"><span data-stu-id="fde45-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="fde45-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fde45-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="fde45-137">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="fde45-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="fde45-138">您可以使用 [AzVMExtensionImage](./Get-AzVMExtensionImage.md) Cmdlet 來取得副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="fde45-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="fde45-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fde45-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fde45-140">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="fde45-140">Specify the VMSS object.</span></span>
<span data-ttu-id="fde45-141">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="fde45-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="fde45-142">-確認</span><span class="sxs-lookup"><span data-stu-id="fde45-142">-Confirm</span></span>
<span data-ttu-id="fde45-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fde45-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde45-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde45-144">-WhatIf</span></span>
<span data-ttu-id="fde45-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fde45-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fde45-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fde45-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde45-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde45-147">CommonParameters</span></span>
<span data-ttu-id="fde45-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fde45-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde45-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fde45-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde45-150">輸入</span><span class="sxs-lookup"><span data-stu-id="fde45-150">INPUTS</span></span>

### <span data-ttu-id="fde45-151">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="fde45-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fde45-152">System.object</span><span class="sxs-lookup"><span data-stu-id="fde45-152">System.String</span></span>

### <span data-ttu-id="fde45-153">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fde45-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fde45-154">System.object</span><span class="sxs-lookup"><span data-stu-id="fde45-154">System.Object</span></span>

## <span data-ttu-id="fde45-155">輸出</span><span class="sxs-lookup"><span data-stu-id="fde45-155">OUTPUTS</span></span>

### <span data-ttu-id="fde45-156">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="fde45-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fde45-157">筆記</span><span class="sxs-lookup"><span data-stu-id="fde45-157">NOTES</span></span>

## <span data-ttu-id="fde45-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="fde45-158">RELATED LINKS</span></span>

[<span data-ttu-id="fde45-159">移除-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="fde45-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="fde45-160">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fde45-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="fde45-161">AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="fde45-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="fde45-162">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="fde45-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="fde45-163">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fde45-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
