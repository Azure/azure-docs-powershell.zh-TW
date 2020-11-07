---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966054"
---
# <span data-ttu-id="8faaf-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="8faaf-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="8faaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8faaf-102">SYNOPSIS</span></span>
<span data-ttu-id="8faaf-103">設定 VMSS 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="8faaf-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="8faaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="8faaf-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8faaf-105">說明</span><span class="sxs-lookup"><span data-stu-id="8faaf-105">DESCRIPTION</span></span>
<span data-ttu-id="8faaf-106">**AzVmssStorageProfile** Cmdlet 會設定虛擬機器縮放集 (VMSS) 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="8faaf-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8faaf-107">示例</span><span class="sxs-lookup"><span data-stu-id="8faaf-107">EXAMPLES</span></span>

### <span data-ttu-id="8faaf-108">範例1：設定 VMSS 的儲存配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="8faaf-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="8faaf-109">這個命令會設定名為 ContosoVMSS 之 VMSS 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="8faaf-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="8faaf-110">參數</span><span class="sxs-lookup"><span data-stu-id="8faaf-110">PARAMETERS</span></span>

### <span data-ttu-id="8faaf-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="8faaf-111">-DataDisk</span></span>
<span data-ttu-id="8faaf-112">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="8faaf-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8faaf-113">-DefaultProfile</span></span>
<span data-ttu-id="8faaf-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8faaf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8faaf-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="8faaf-115">-DiffDiskSetting</span></span>
<span data-ttu-id="8faaf-116">指定作業系統磁片的差異磁片設定。</span><span class="sxs-lookup"><span data-stu-id="8faaf-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="8faaf-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8faaf-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8faaf-118">指定客戶管理磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8faaf-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="8faaf-119">只能為受管理的磁片指定這種情況。</span><span class="sxs-lookup"><span data-stu-id="8faaf-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="8faaf-120">-影像</span><span class="sxs-lookup"><span data-stu-id="8faaf-120">-Image</span></span>
<span data-ttu-id="8faaf-121">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="8faaf-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="8faaf-122">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="8faaf-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="8faaf-123">-ImageReferenceId</span></span>
<span data-ttu-id="8faaf-124">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="8faaf-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="8faaf-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="8faaf-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="8faaf-126">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="8faaf-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="8faaf-127">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8faaf-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="8faaf-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="8faaf-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="8faaf-129">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="8faaf-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="8faaf-130">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8faaf-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8faaf-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="8faaf-131">-ImageReferenceSku</span></span>
<span data-ttu-id="8faaf-132">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="8faaf-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="8faaf-133">若要取得 Sku，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8faaf-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="8faaf-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="8faaf-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="8faaf-135">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="8faaf-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="8faaf-136">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="8faaf-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="8faaf-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8faaf-137">-ManagedDisk</span></span>
<span data-ttu-id="8faaf-138">指定受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="8faaf-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="8faaf-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="8faaf-139">-OsDiskCaching</span></span>
<span data-ttu-id="8faaf-140">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="8faaf-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="8faaf-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8faaf-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8faaf-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="8faaf-142">ReadOnly</span></span>
- <span data-ttu-id="8faaf-143">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="8faaf-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="8faaf-144">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8faaf-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="8faaf-145">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="8faaf-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="8faaf-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="8faaf-147">指定此 Cmdlet 如何建立 VMSS 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8faaf-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="8faaf-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8faaf-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8faaf-149">附加：當您使用專用磁片來建立 VMSS 虛擬機器時，就會用到這個值。</span><span class="sxs-lookup"><span data-stu-id="8faaf-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="8faaf-150">FromImage：當您使用影像來建立 VMSS 虛擬機器時，會用到這個值。</span><span class="sxs-lookup"><span data-stu-id="8faaf-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="8faaf-151">如果您使用的是平臺影像，您也會使用 *imageReference* 參數。</span><span class="sxs-lookup"><span data-stu-id="8faaf-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="8faaf-152">-OsDiskName</span></span>
<span data-ttu-id="8faaf-153">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="8faaf-153">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="8faaf-154">-OsDiskOsType</span></span>
<span data-ttu-id="8faaf-155">指定磁片上的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="8faaf-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="8faaf-156">這只是使用者影像案例所需要的，不適用於平臺影像。</span><span class="sxs-lookup"><span data-stu-id="8faaf-156">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8faaf-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="8faaf-158">指定是否應該在 OS 磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="8faaf-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="8faaf-159">-VhdContainer</span></span>
<span data-ttu-id="8faaf-160">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="8faaf-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8faaf-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8faaf-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8faaf-162">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="8faaf-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="8faaf-163">若要取得物件，請使用 New-AzVmssConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="8faaf-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="8faaf-164">-確認</span><span class="sxs-lookup"><span data-stu-id="8faaf-164">-Confirm</span></span>
<span data-ttu-id="8faaf-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8faaf-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8faaf-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8faaf-166">-WhatIf</span></span>
<span data-ttu-id="8faaf-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8faaf-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8faaf-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8faaf-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8faaf-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8faaf-169">CommonParameters</span></span>
<span data-ttu-id="8faaf-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8faaf-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8faaf-171">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8faaf-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8faaf-172">輸入</span><span class="sxs-lookup"><span data-stu-id="8faaf-172">INPUTS</span></span>

### <span data-ttu-id="8faaf-173">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="8faaf-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8faaf-174">System.object</span><span class="sxs-lookup"><span data-stu-id="8faaf-174">System.String</span></span>

### <span data-ttu-id="8faaf-175">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="8faaf-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8faaf-176">"OperatingSystemTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="8faaf-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8faaf-177">System.object []</span><span class="sxs-lookup"><span data-stu-id="8faaf-177">System.String[]</span></span>

### <span data-ttu-id="8faaf-178">VirtualMachineScaleSetDataDisk [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="8faaf-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="8faaf-179">輸出</span><span class="sxs-lookup"><span data-stu-id="8faaf-179">OUTPUTS</span></span>

### <span data-ttu-id="8faaf-180">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="8faaf-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8faaf-181">筆記</span><span class="sxs-lookup"><span data-stu-id="8faaf-181">NOTES</span></span>

## <span data-ttu-id="8faaf-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="8faaf-182">RELATED LINKS</span></span>

[<span data-ttu-id="8faaf-183">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8faaf-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="8faaf-184">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8faaf-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8faaf-185">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8faaf-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="8faaf-186">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8faaf-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


