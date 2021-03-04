---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 774fb61f2394c5634c8415a7a18ce63f4e696a3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912066"
---
# <span data-ttu-id="2b297-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="2b297-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="2b297-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b297-102">SYNOPSIS</span></span>
<span data-ttu-id="2b297-103">新增擴充功能至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="2b297-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="2b297-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b297-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b297-105">描述</span><span class="sxs-lookup"><span data-stu-id="2b297-105">DESCRIPTION</span></span>
<span data-ttu-id="2b297-106">**Add-Az VmssExtension** Cmdlet 在 VMSS (虛擬機器縮放集) 。</span><span class="sxs-lookup"><span data-stu-id="2b297-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="2b297-107">例子</span><span class="sxs-lookup"><span data-stu-id="2b297-107">EXAMPLES</span></span>

### <span data-ttu-id="2b297-108">範例 1：新增擴充功能至 VMSS</span><span class="sxs-lookup"><span data-stu-id="2b297-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="2b297-109">此命令會將擴充功能新增到 VMSS。</span><span class="sxs-lookup"><span data-stu-id="2b297-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="2b297-110">範例 2：新增副檔名至 VMSS 與設定及受保護的設定</span><span class="sxs-lookup"><span data-stu-id="2b297-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="2b297-111">此命令會將副檔名新增到 VMSS，並包含 Blob 儲存空間的 bash 腳本範例，在設定中指定 Blob 儲存的 URL，以及受保護設定中的可執行命令和安全性存取。</span><span class="sxs-lookup"><span data-stu-id="2b297-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="2b297-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b297-112">PARAMETERS</span></span>

### <span data-ttu-id="2b297-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2b297-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2b297-114">指出擴充功能版本是否應該自動更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="2b297-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="2b297-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b297-115">-DefaultProfile</span></span>
<span data-ttu-id="2b297-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b297-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b297-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="2b297-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="2b297-118">指出如果有較新版本的擴充功能可用，該擴充功能是否應該由平臺自動升級。</span><span class="sxs-lookup"><span data-stu-id="2b297-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

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

### <span data-ttu-id="2b297-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="2b297-119">-ForceUpdateTag</span></span>
<span data-ttu-id="2b297-120">如果提供值且與先前的值不同，即使擴充功能組配置沒有變更，擴充處理常式也會強制更新。</span><span class="sxs-lookup"><span data-stu-id="2b297-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="2b297-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b297-121">-Name</span></span>
<span data-ttu-id="2b297-122">指定此 Cmdlet 新增的副檔名。</span><span class="sxs-lookup"><span data-stu-id="2b297-122">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="2b297-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="2b297-123">-ProtectedSetting</span></span>
<span data-ttu-id="2b297-124">指定副檔名的私人群組原則，做為字串。</span><span class="sxs-lookup"><span data-stu-id="2b297-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="2b297-125">此 Cmdlet 會加密私人組配置。</span><span class="sxs-lookup"><span data-stu-id="2b297-125">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="2b297-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="2b297-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="2b297-127">副檔名集合，之後需要提供此擴充功能。</span><span class="sxs-lookup"><span data-stu-id="2b297-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="2b297-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2b297-128">-Publisher</span></span>
<span data-ttu-id="2b297-129">指定擴充功能發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b297-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="2b297-130">發行者在發行者註冊擴充功能時提供名稱。</span><span class="sxs-lookup"><span data-stu-id="2b297-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="2b297-131">這可以使用 [Get-AzCMImagePublisher Cmdlet](./Get-AzVMImagePublisher.md) 取得發行者。</span><span class="sxs-lookup"><span data-stu-id="2b297-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="2b297-132">-設定</span><span class="sxs-lookup"><span data-stu-id="2b297-132">-Setting</span></span>
<span data-ttu-id="2b297-133">指定副檔名的公用群組原則做為字串。</span><span class="sxs-lookup"><span data-stu-id="2b297-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="2b297-134">此 Cmdlet 不會加密公用組配置。</span><span class="sxs-lookup"><span data-stu-id="2b297-134">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="2b297-135">-類型</span><span class="sxs-lookup"><span data-stu-id="2b297-135">-Type</span></span>
<span data-ttu-id="2b297-136">指定擴充功能類型。</span><span class="sxs-lookup"><span data-stu-id="2b297-136">Specifies the extension type.</span></span>
<span data-ttu-id="2b297-137">您可以使用 [Get-AzCMExtensionImageType](./Get-AzVMExtensionImageType.md) Cmdlet 取得副檔名類型。</span><span class="sxs-lookup"><span data-stu-id="2b297-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="2b297-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2b297-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="2b297-139">指定要用於此虛擬機器的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="2b297-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2b297-140">您可以使用 [Get-AzCMExtensionImdlet](./Get-AzVMExtensionImage.md) 取得擴充功能的版本。</span><span class="sxs-lookup"><span data-stu-id="2b297-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="2b297-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2b297-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2b297-142">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="2b297-142">Specify the VMSS object.</span></span>
<span data-ttu-id="2b297-143">您可以使用 [New-AzEvssConfig](./New-AzVmssConfig.md) 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="2b297-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="2b297-144">-確認</span><span class="sxs-lookup"><span data-stu-id="2b297-144">-Confirm</span></span>
<span data-ttu-id="2b297-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2b297-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b297-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b297-146">-WhatIf</span></span>
<span data-ttu-id="2b297-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b297-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b297-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b297-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b297-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b297-149">CommonParameters</span></span>
<span data-ttu-id="2b297-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b297-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b297-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b297-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b297-152">輸入</span><span class="sxs-lookup"><span data-stu-id="2b297-152">INPUTS</span></span>

### <span data-ttu-id="2b297-153">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2b297-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2b297-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2b297-154">System.String</span></span>

### <span data-ttu-id="2b297-155">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b297-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2b297-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="2b297-156">System.Object</span></span>

## <span data-ttu-id="2b297-157">輸出</span><span class="sxs-lookup"><span data-stu-id="2b297-157">OUTPUTS</span></span>

### <span data-ttu-id="2b297-158">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2b297-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2b297-159">筆記</span><span class="sxs-lookup"><span data-stu-id="2b297-159">NOTES</span></span>

## <span data-ttu-id="2b297-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b297-160">RELATED LINKS</span></span>

[<span data-ttu-id="2b297-161">Remove-AzEvssExtension</span><span class="sxs-lookup"><span data-stu-id="2b297-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="2b297-162">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="2b297-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2b297-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="2b297-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="2b297-164">Get-Az解說ExtensionImage</span><span class="sxs-lookup"><span data-stu-id="2b297-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="2b297-165">New-AzEvssConfig</span><span class="sxs-lookup"><span data-stu-id="2b297-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
