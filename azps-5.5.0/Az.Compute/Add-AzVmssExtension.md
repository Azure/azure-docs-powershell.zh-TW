---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 152d6e861d7622e262279c1f665565347e0ab2cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141338"
---
# <span data-ttu-id="148b8-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="148b8-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="148b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="148b8-102">SYNOPSIS</span></span>
<span data-ttu-id="148b8-103">將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="148b8-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="148b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="148b8-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="148b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="148b8-105">DESCRIPTION</span></span>
<span data-ttu-id="148b8-106">**AzVmssExtension** Cmdlet 會將延伸 (VMSS 的虛擬電腦規模集新增至 [) ]。</span><span class="sxs-lookup"><span data-stu-id="148b8-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="148b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="148b8-107">EXAMPLES</span></span>

### <span data-ttu-id="148b8-108">範例1：在 VMSS 中新增副檔名</span><span class="sxs-lookup"><span data-stu-id="148b8-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="148b8-109">這個命令會將延伸新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="148b8-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="148b8-110">範例2：使用設定和受保護的設定，將延伸新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="148b8-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="148b8-111">這個命令會在 blob 儲存空間上加上含範例 bash 腳本的 VMSS 副檔名，並在 [設定] 和 [安全存取] 中，指定 [受保護的設定] 中的 [blob 儲存] 與 [執行中] 命令</span><span class="sxs-lookup"><span data-stu-id="148b8-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="148b8-112">參數</span><span class="sxs-lookup"><span data-stu-id="148b8-112">PARAMETERS</span></span>

### <span data-ttu-id="148b8-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="148b8-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="148b8-114">指出延伸版本是否應該自動更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="148b8-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="148b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="148b8-115">-DefaultProfile</span></span>
<span data-ttu-id="148b8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="148b8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="148b8-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="148b8-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="148b8-118">指示如果有更新版本的擴充功能，平臺是否應自動升級延伸。</span><span class="sxs-lookup"><span data-stu-id="148b8-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="148b8-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="148b8-119">-ForceUpdateTag</span></span>
<span data-ttu-id="148b8-120">如果提供值且與前一個值不同，延伸處理常式將被迫更新，即使延伸設定尚未變更也一樣。</span><span class="sxs-lookup"><span data-stu-id="148b8-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="148b8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="148b8-121">-Name</span></span>
<span data-ttu-id="148b8-122">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="148b8-122">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="148b8-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="148b8-123">-ProtectedSetting</span></span>
<span data-ttu-id="148b8-124">以字串形式指定延伸的專用配置。</span><span class="sxs-lookup"><span data-stu-id="148b8-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="148b8-125">這個 Cmdlet 會加密私人配置。</span><span class="sxs-lookup"><span data-stu-id="148b8-125">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="148b8-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="148b8-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="148b8-127">需要預配此延伸的副檔名名稱集合。</span><span class="sxs-lookup"><span data-stu-id="148b8-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="148b8-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="148b8-128">-Publisher</span></span>
<span data-ttu-id="148b8-129">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="148b8-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="148b8-130">發行者在註冊延伸時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="148b8-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="148b8-131">這可以使用 [AzVMImagePublisher](./Get-AzVMImagePublisher.md) Cmdlet 來取得發行者。</span><span class="sxs-lookup"><span data-stu-id="148b8-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="148b8-132">-設定</span><span class="sxs-lookup"><span data-stu-id="148b8-132">-Setting</span></span>
<span data-ttu-id="148b8-133">指定副檔名的公用配置（以字串形式）。</span><span class="sxs-lookup"><span data-stu-id="148b8-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="148b8-134">這個 Cmdlet 不會加密公用配置。</span><span class="sxs-lookup"><span data-stu-id="148b8-134">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="148b8-135">-類型</span><span class="sxs-lookup"><span data-stu-id="148b8-135">-Type</span></span>
<span data-ttu-id="148b8-136">指定延伸類型。</span><span class="sxs-lookup"><span data-stu-id="148b8-136">Specifies the extension type.</span></span>
<span data-ttu-id="148b8-137">您可以使用 [AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) Cmdlet 來取得延伸類型。</span><span class="sxs-lookup"><span data-stu-id="148b8-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="148b8-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="148b8-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="148b8-139">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="148b8-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="148b8-140">您可以使用 [AzVMExtensionImage](./Get-AzVMExtensionImage.md) Cmdlet 來取得副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="148b8-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="148b8-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="148b8-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="148b8-142">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="148b8-142">Specify the VMSS object.</span></span>
<span data-ttu-id="148b8-143">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="148b8-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="148b8-144">-確認</span><span class="sxs-lookup"><span data-stu-id="148b8-144">-Confirm</span></span>
<span data-ttu-id="148b8-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="148b8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="148b8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="148b8-146">-WhatIf</span></span>
<span data-ttu-id="148b8-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="148b8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="148b8-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="148b8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="148b8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="148b8-149">CommonParameters</span></span>
<span data-ttu-id="148b8-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="148b8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="148b8-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="148b8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="148b8-152">輸入</span><span class="sxs-lookup"><span data-stu-id="148b8-152">INPUTS</span></span>

### <span data-ttu-id="148b8-153">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="148b8-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="148b8-154">System.object</span><span class="sxs-lookup"><span data-stu-id="148b8-154">System.String</span></span>

### <span data-ttu-id="148b8-155">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="148b8-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="148b8-156">System.object</span><span class="sxs-lookup"><span data-stu-id="148b8-156">System.Object</span></span>

## <span data-ttu-id="148b8-157">輸出</span><span class="sxs-lookup"><span data-stu-id="148b8-157">OUTPUTS</span></span>

### <span data-ttu-id="148b8-158">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="148b8-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="148b8-159">筆記</span><span class="sxs-lookup"><span data-stu-id="148b8-159">NOTES</span></span>

## <span data-ttu-id="148b8-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="148b8-160">RELATED LINKS</span></span>

[<span data-ttu-id="148b8-161">移除-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="148b8-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="148b8-162">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="148b8-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="148b8-163">AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="148b8-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="148b8-164">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="148b8-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="148b8-165">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="148b8-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
