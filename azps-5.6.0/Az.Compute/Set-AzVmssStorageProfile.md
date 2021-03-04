---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: ec233765f401348895275291ddad0571d1ddfc85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908293"
---
# <span data-ttu-id="11010-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="11010-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="11010-102">簡介</span><span class="sxs-lookup"><span data-stu-id="11010-102">SYNOPSIS</span></span>
<span data-ttu-id="11010-103">設定 VMSS 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="11010-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="11010-104">語法</span><span class="sxs-lookup"><span data-stu-id="11010-104">SYNTAX</span></span>

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

## <span data-ttu-id="11010-105">描述</span><span class="sxs-lookup"><span data-stu-id="11010-105">DESCRIPTION</span></span>
<span data-ttu-id="11010-106">**Set-Az VmssStorageProfile** Cmdlet 會設定虛擬機器縮放集 (VMSS) 。</span><span class="sxs-lookup"><span data-stu-id="11010-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="11010-107">例子</span><span class="sxs-lookup"><span data-stu-id="11010-107">EXAMPLES</span></span>

### <span data-ttu-id="11010-108">範例 1：設定 VMSS 的儲存配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="11010-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="11010-109">此命令會為名為 Contoso VMSS 的 VMSS 設定儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="11010-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="11010-110">參數</span><span class="sxs-lookup"><span data-stu-id="11010-110">PARAMETERS</span></span>

### <span data-ttu-id="11010-111">-Data至上</span><span class="sxs-lookup"><span data-stu-id="11010-111">-DataDisk</span></span>
<span data-ttu-id="11010-112">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="11010-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="11010-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11010-113">-DefaultProfile</span></span>
<span data-ttu-id="11010-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="11010-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11010-115">-DiffSettingSetting</span><span class="sxs-lookup"><span data-stu-id="11010-115">-DiffDiskSetting</span></span>
<span data-ttu-id="11010-116">指定作業系統磁片的不同磁片設定。</span><span class="sxs-lookup"><span data-stu-id="11010-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="11010-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="11010-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="11010-118">指定客戶管理的磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="11010-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="11010-119">這僅適用于受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="11010-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="11010-120">-影像</span><span class="sxs-lookup"><span data-stu-id="11010-120">-Image</span></span>
<span data-ttu-id="11010-121">指定使用者圖像的 Blob URI。</span><span class="sxs-lookup"><span data-stu-id="11010-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="11010-122">VMSS 會在同一個使用者映射容器內建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="11010-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="11010-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="11010-123">-ImageReferenceId</span></span>
<span data-ttu-id="11010-124">指定影像參照識別碼。</span><span class="sxs-lookup"><span data-stu-id="11010-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="11010-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="11010-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="11010-126">指定 VMImage 提供的虛擬機器 (類型) 類型。</span><span class="sxs-lookup"><span data-stu-id="11010-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="11010-127">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11010-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="11010-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="11010-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="11010-129">指定 VMImage 的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="11010-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="11010-130">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11010-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="11010-131">-ImageReferenceSKU</span><span class="sxs-lookup"><span data-stu-id="11010-131">-ImageReferenceSku</span></span>
<span data-ttu-id="11010-132">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="11010-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="11010-133">若要取得 SKUS，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11010-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="11010-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="11010-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="11010-135">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="11010-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="11010-136">若要使用最新版本，請指定最新版本的值，而非特定版本。</span><span class="sxs-lookup"><span data-stu-id="11010-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="11010-137">-Managed前小分</span><span class="sxs-lookup"><span data-stu-id="11010-137">-ManagedDisk</span></span>
<span data-ttu-id="11010-138">指定受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="11010-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="11010-139">-Os在Caching</span><span class="sxs-lookup"><span data-stu-id="11010-139">-OsDiskCaching</span></span>
<span data-ttu-id="11010-140">指定作業系統磁片的緩存模式。</span><span class="sxs-lookup"><span data-stu-id="11010-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="11010-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11010-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11010-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="11010-142">ReadOnly</span></span>
- <span data-ttu-id="11010-143">朗讀預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="11010-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="11010-144">如果您變更緩存值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11010-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="11010-145">此設定會影響磁片的一致性與績效。</span><span class="sxs-lookup"><span data-stu-id="11010-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="11010-146">-OsCreateOption</span><span class="sxs-lookup"><span data-stu-id="11010-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="11010-147">指定此 Cmdlet 如何建立 VMSS 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11010-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="11010-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="11010-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="11010-149">附加：當您使用特殊磁片來建立 VMSS 虛擬機器時，會使用此值。</span><span class="sxs-lookup"><span data-stu-id="11010-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="11010-150">FromImage：當您使用影像建立 VMSS 虛擬機器時，會使用此值。</span><span class="sxs-lookup"><span data-stu-id="11010-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="11010-151">如果您使用的是平臺圖像，您也會使用 *imageReference* 參數。</span><span class="sxs-lookup"><span data-stu-id="11010-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="11010-152">-OsName</span><span class="sxs-lookup"><span data-stu-id="11010-152">-OsDiskName</span></span>
<span data-ttu-id="11010-153">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="11010-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="11010-154">-OsCioOsType</span><span class="sxs-lookup"><span data-stu-id="11010-154">-OsDiskOsType</span></span>
<span data-ttu-id="11010-155">指定磁片上的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="11010-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="11010-156">這僅適用于使用者影像案例，而非平臺圖像。</span><span class="sxs-lookup"><span data-stu-id="11010-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="11010-157">-OsRiteWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="11010-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="11010-158">指定作業系統磁片上是否應該啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="11010-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="11010-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="11010-159">-VhdContainer</span></span>
<span data-ttu-id="11010-160">指定用來儲存 VMSS 作業系統磁片的容器 URL。</span><span class="sxs-lookup"><span data-stu-id="11010-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="11010-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11010-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="11010-162">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="11010-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="11010-163">若要取得物件，請使用New-AzVmssConfig物件。</span><span class="sxs-lookup"><span data-stu-id="11010-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="11010-164">-確認</span><span class="sxs-lookup"><span data-stu-id="11010-164">-Confirm</span></span>
<span data-ttu-id="11010-165">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="11010-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11010-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11010-166">-WhatIf</span></span>
<span data-ttu-id="11010-167">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11010-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11010-168">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11010-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11010-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11010-169">CommonParameters</span></span>
<span data-ttu-id="11010-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="11010-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11010-171">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11010-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11010-172">輸入</span><span class="sxs-lookup"><span data-stu-id="11010-172">INPUTS</span></span>

### <span data-ttu-id="11010-173">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11010-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="11010-174">System.String</span><span class="sxs-lookup"><span data-stu-id="11010-174">System.String</span></span>

### <span data-ttu-id="11010-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="11010-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="11010-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="11010-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="11010-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="11010-177">System.String[]</span></span>

### <span data-ttu-id="11010-178">Microsoft.Azure.management.Compute.models.VirtualMachineScaleSetDataAz[]</span><span class="sxs-lookup"><span data-stu-id="11010-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="11010-179">輸出</span><span class="sxs-lookup"><span data-stu-id="11010-179">OUTPUTS</span></span>

### <span data-ttu-id="11010-180">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11010-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="11010-181">筆記</span><span class="sxs-lookup"><span data-stu-id="11010-181">NOTES</span></span>

## <span data-ttu-id="11010-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="11010-182">RELATED LINKS</span></span>

[<span data-ttu-id="11010-183">Get-AzEVImageOffer</span><span class="sxs-lookup"><span data-stu-id="11010-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="11010-184">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="11010-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="11010-185">Get-AzKUImageSku</span><span class="sxs-lookup"><span data-stu-id="11010-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="11010-186">New-AzEvssConfig</span><span class="sxs-lookup"><span data-stu-id="11010-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


