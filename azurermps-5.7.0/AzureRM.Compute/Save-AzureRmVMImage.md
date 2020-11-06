---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455484"
---
# <span data-ttu-id="90f4e-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="90f4e-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="90f4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90f4e-102">SYNOPSIS</span></span>
<span data-ttu-id="90f4e-103">將虛擬機器儲存為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="90f4e-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90f4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="90f4e-104">SYNTAX</span></span>

### <span data-ttu-id="90f4e-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="90f4e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### <span data-ttu-id="90f4e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="90f4e-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="90f4e-107">說明</span><span class="sxs-lookup"><span data-stu-id="90f4e-107">DESCRIPTION</span></span>
<span data-ttu-id="90f4e-108">AzureRmVMImage Cmdlet 會將虛擬機器 **儲存** 為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="90f4e-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="90f4e-109">在您建立虛擬機器影像之前，請 sysprep 虛擬機器，然後使用 Set-AzureRmVM Cmdlet 將它標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="90f4e-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="90f4e-110">這個 Cmdlet 的輸出是 (JSON) 範本的 JavaScript 物件符號。</span><span class="sxs-lookup"><span data-stu-id="90f4e-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="90f4e-111">您可以從捕獲的映射部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="90f4e-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="90f4e-112">示例</span><span class="sxs-lookup"><span data-stu-id="90f4e-112">EXAMPLES</span></span>

### <span data-ttu-id="90f4e-113">範例1：捕獲虛擬機器</span><span class="sxs-lookup"><span data-stu-id="90f4e-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="90f4e-114">第一個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="90f4e-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="90f4e-115">第二個命令會將名為 VirtualMachine07 的虛擬機器捕獲為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="90f4e-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="90f4e-116">**Output** 屬性會傳回 JSON 範本。</span><span class="sxs-lookup"><span data-stu-id="90f4e-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="90f4e-117">參數</span><span class="sxs-lookup"><span data-stu-id="90f4e-117">PARAMETERS</span></span>

### <span data-ttu-id="90f4e-118">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="90f4e-118">-DestinationContainerName</span></span>
<span data-ttu-id="90f4e-119">指定您想要保留影像之「系統」容器內的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="90f4e-119">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="90f4e-120">如果容器不存在，就會為您建立。</span><span class="sxs-lookup"><span data-stu-id="90f4e-120">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="90f4e-121">組成 VMImage 的虛擬硬碟 (Vhd) 會駐留在此參數指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="90f4e-121">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="90f4e-122">如果 Vhd 分佈在多個儲存空間帳戶中，這個 Cmdlet 會在每個儲存空間帳戶中建立一個具有此名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="90f4e-122">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="90f4e-123">所儲存影像的 URL 類似以下所示：</span><span class="sxs-lookup"><span data-stu-id="90f4e-123">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="90f4e-124">\<storageAccountName\>blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx。</span><span class="sxs-lookup"><span data-stu-id="90f4e-124">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="90f4e-125">-Id</span></span>
<span data-ttu-id="90f4e-126">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="90f4e-126">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="90f4e-127">-Name</span></span>
<span data-ttu-id="90f4e-128">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="90f4e-128">Specifies a name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="90f4e-129">-Overwrite</span></span>
<span data-ttu-id="90f4e-130">表示此 Cmdlet 會覆寫目的地容器中具有相同前置詞的任何 Vhd。</span><span class="sxs-lookup"><span data-stu-id="90f4e-130">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-131">-Path</span><span class="sxs-lookup"><span data-stu-id="90f4e-131">-Path</span></span>
<span data-ttu-id="90f4e-132">指定 VHD 的路徑。</span><span class="sxs-lookup"><span data-stu-id="90f4e-132">Specifies the path of the VHD.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f4e-133">-ResourceGroupName</span></span>
<span data-ttu-id="90f4e-134">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90f4e-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-135">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="90f4e-135">-VHDNamePrefix</span></span>
<span data-ttu-id="90f4e-136">在組成 VMImage 儲存設定檔的 blob 名稱中，指定前置詞。</span><span class="sxs-lookup"><span data-stu-id="90f4e-136">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="90f4e-137">例如，作業系統磁片的首碼 vhdPrefix 會產生 name vhdPrefix- \<guid\> osdisk .。。vhd.</span><span class="sxs-lookup"><span data-stu-id="90f4e-137">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f4e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f4e-138">CommonParameters</span></span>
<span data-ttu-id="90f4e-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90f4e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f4e-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90f4e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f4e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="90f4e-141">INPUTS</span></span>

### <span data-ttu-id="90f4e-142">所有</span><span class="sxs-lookup"><span data-stu-id="90f4e-142">None</span></span>
<span data-ttu-id="90f4e-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="90f4e-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90f4e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="90f4e-144">OUTPUTS</span></span>

## <span data-ttu-id="90f4e-145">筆記</span><span class="sxs-lookup"><span data-stu-id="90f4e-145">NOTES</span></span>

## <span data-ttu-id="90f4e-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="90f4e-146">RELATED LINKS</span></span>

[<span data-ttu-id="90f4e-147">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="90f4e-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="90f4e-148">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="90f4e-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="90f4e-149">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="90f4e-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="90f4e-150">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="90f4e-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="90f4e-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="90f4e-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


