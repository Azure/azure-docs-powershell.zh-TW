---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444967"
---
# <span data-ttu-id="e1f69-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="e1f69-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="e1f69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1f69-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f69-103">設定 VMSS 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="e1f69-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1f69-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1f69-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f69-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1f69-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f69-106">**AzureRmVmssStorageProfile** Cmdlet 會設定虛擬機器縮放集 (VMSS) 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="e1f69-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e1f69-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1f69-107">EXAMPLES</span></span>

### <span data-ttu-id="e1f69-108">範例1：設定 VMSS 的儲存配置檔案屬性</span><span class="sxs-lookup"><span data-stu-id="e1f69-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="e1f69-109">這個命令會設定名為 ContosoVMSS 之 VMSS 的儲存配置檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="e1f69-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="e1f69-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1f69-110">PARAMETERS</span></span>

### <span data-ttu-id="e1f69-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="e1f69-111">-DataDisk</span></span>
<span data-ttu-id="e1f69-112">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="e1f69-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="e1f69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f69-113">-DefaultProfile</span></span>
<span data-ttu-id="e1f69-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1f69-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1f69-115">-影像</span><span class="sxs-lookup"><span data-stu-id="e1f69-115">-Image</span></span>
<span data-ttu-id="e1f69-116">指定使用者影像的 blob URI。</span><span class="sxs-lookup"><span data-stu-id="e1f69-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="e1f69-117">VMSS 會在使用者影像的同一個容器中建立作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="e1f69-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="e1f69-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="e1f69-118">-ImageReferenceId</span></span>
<span data-ttu-id="e1f69-119">指定影像參照 ID。</span><span class="sxs-lookup"><span data-stu-id="e1f69-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="e1f69-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="e1f69-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="e1f69-121">指定 (VMImage) 優惠的虛擬機器影像類型。</span><span class="sxs-lookup"><span data-stu-id="e1f69-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="e1f69-122">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1f69-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="e1f69-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="e1f69-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="e1f69-124">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f69-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e1f69-125">若要取得發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1f69-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e1f69-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="e1f69-126">-ImageReferenceSku</span></span>
<span data-ttu-id="e1f69-127">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="e1f69-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="e1f69-128">若要取得 Sku，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1f69-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="e1f69-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="e1f69-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="e1f69-130">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="e1f69-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="e1f69-131">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="e1f69-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="e1f69-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e1f69-132">-ManagedDisk</span></span>
<span data-ttu-id="e1f69-133">指定受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="e1f69-133">Specifies the managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f69-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="e1f69-134">-OsDiskCaching</span></span>
<span data-ttu-id="e1f69-135">指定作業系統磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="e1f69-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="e1f69-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e1f69-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1f69-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="e1f69-137">ReadOnly</span></span>
- <span data-ttu-id="e1f69-138">讀</span><span class="sxs-lookup"><span data-stu-id="e1f69-138">ReadWrite</span></span>

<span data-ttu-id="e1f69-139">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="e1f69-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="e1f69-140">如果您變更快取值，Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e1f69-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="e1f69-141">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="e1f69-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="e1f69-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="e1f69-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="e1f69-143">指定此 Cmdlet 如何建立 VMSS 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e1f69-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="e1f69-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e1f69-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1f69-145">附加：當您使用專用磁片來建立 VMSS 虛擬機器時，就會用到這個值。</span><span class="sxs-lookup"><span data-stu-id="e1f69-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="e1f69-146">FromImage：當您使用影像來建立 VMSS 虛擬機器時，會用到這個值。</span><span class="sxs-lookup"><span data-stu-id="e1f69-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="e1f69-147">如果您使用的是平臺影像，您也會使用 *imageReference* 參數。</span><span class="sxs-lookup"><span data-stu-id="e1f69-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f69-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="e1f69-148">-OsDiskName</span></span>
<span data-ttu-id="e1f69-149">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f69-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="e1f69-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="e1f69-150">-OsDiskOsType</span></span>
<span data-ttu-id="e1f69-151">指定磁片上的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="e1f69-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="e1f69-152">這只是使用者影像案例所需要的，不適用於平臺影像。</span><span class="sxs-lookup"><span data-stu-id="e1f69-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="e1f69-153">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="e1f69-153">-VhdContainer</span></span>
<span data-ttu-id="e1f69-154">指定用來儲存 VMSS 作業系統磁片的容器 Url。</span><span class="sxs-lookup"><span data-stu-id="e1f69-154">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="e1f69-155">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e1f69-155">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e1f69-156">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="e1f69-156">Specifies the VMSS object.</span></span>
<span data-ttu-id="e1f69-157">若要取得物件，請使用 New-AzureRmVmssConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="e1f69-157">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="e1f69-158">-確認</span><span class="sxs-lookup"><span data-stu-id="e1f69-158">-Confirm</span></span>
<span data-ttu-id="e1f69-159">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1f69-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1f69-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f69-160">-WhatIf</span></span>
<span data-ttu-id="e1f69-161">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1f69-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1f69-162">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1f69-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1f69-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f69-163">CommonParameters</span></span>
<span data-ttu-id="e1f69-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1f69-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f69-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1f69-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f69-166">輸入</span><span class="sxs-lookup"><span data-stu-id="e1f69-166">INPUTS</span></span>

###  
<span data-ttu-id="e1f69-167">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e1f69-167">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e1f69-168">輸出</span><span class="sxs-lookup"><span data-stu-id="e1f69-168">OUTPUTS</span></span>

## <span data-ttu-id="e1f69-169">筆記</span><span class="sxs-lookup"><span data-stu-id="e1f69-169">NOTES</span></span>

## <span data-ttu-id="e1f69-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1f69-170">RELATED LINKS</span></span>

[<span data-ttu-id="e1f69-171">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e1f69-171">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="e1f69-172">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e1f69-172">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="e1f69-173">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e1f69-173">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="e1f69-174">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e1f69-174">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


