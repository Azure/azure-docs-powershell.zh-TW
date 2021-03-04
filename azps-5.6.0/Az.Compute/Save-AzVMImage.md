---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: d979e89583b19270dfd13bae85a3afe1505ed55e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913969"
---
# <span data-ttu-id="b905b-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b905b-101">Save-AzVMImage</span></span>

## <span data-ttu-id="b905b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b905b-102">SYNOPSIS</span></span>
<span data-ttu-id="b905b-103">將虛擬機器存成 VMImage。</span><span class="sxs-lookup"><span data-stu-id="b905b-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="b905b-104">語法</span><span class="sxs-lookup"><span data-stu-id="b905b-104">SYNTAX</span></span>

### <span data-ttu-id="b905b-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="b905b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b905b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b905b-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b905b-107">描述</span><span class="sxs-lookup"><span data-stu-id="b905b-107">DESCRIPTION</span></span>
<span data-ttu-id="b905b-108">**Save-Az VMImage Cmdlet** 會將虛擬機器儲存為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="b905b-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="b905b-109">建立虛擬機器映射之前，請複製虛擬機器，然後使用 Cmdlet 將其Set-AzVM通用。</span><span class="sxs-lookup"><span data-stu-id="b905b-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="b905b-110">此 Cmdlet 的輸出是 JSON 範本 (JavaScript) 標記法。</span><span class="sxs-lookup"><span data-stu-id="b905b-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="b905b-111">您可以從捕獲的圖像部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b905b-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="b905b-112">例子</span><span class="sxs-lookup"><span data-stu-id="b905b-112">EXAMPLES</span></span>

### <span data-ttu-id="b905b-113">範例 1：捕獲虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b905b-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="b905b-114">第一個命令將 VirtualMachine07 的虛擬機器標記為通用。</span><span class="sxs-lookup"><span data-stu-id="b905b-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="b905b-115">第二個命令會以 VMImage 來捕獲名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b905b-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="b905b-116">Output **屬性** 會返回 JSON 範本。</span><span class="sxs-lookup"><span data-stu-id="b905b-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="b905b-117">參數</span><span class="sxs-lookup"><span data-stu-id="b905b-117">PARAMETERS</span></span>

### <span data-ttu-id="b905b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b905b-118">-AsJob</span></span>
<span data-ttu-id="b905b-119">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="b905b-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b905b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b905b-120">-DefaultProfile</span></span>
<span data-ttu-id="b905b-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b905b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b905b-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="b905b-122">-DestinationContainerName</span></span>
<span data-ttu-id="b905b-123">指定要保存影像之「系統」容器內的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="b905b-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="b905b-124">如果容器不存在，會建立您的容器。</span><span class="sxs-lookup"><span data-stu-id="b905b-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="b905b-125">虛擬硬碟 (VHDs) 構成此參數指定之容器中的 VMImage。</span><span class="sxs-lookup"><span data-stu-id="b905b-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="b905b-126">如果 VHD 分散在多個儲存帳戶中，此 Cmdlet 會在每個儲存帳戶中建立一個具有此名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="b905b-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="b905b-127">已儲存圖像的 URL 類似：HTTPs:// \<storageAccountName\> \<imagesContainer\> / \<vhdPrefix-osDisk\> .blob.core.windows.net/system/Microsoft.Compute/Images/ .xxxxxxxx-xxxx-xxxx-xxxxxxxxx.vhd。</span><span class="sxs-lookup"><span data-stu-id="b905b-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-128">-Id</span><span class="sxs-lookup"><span data-stu-id="b905b-128">-Id</span></span>
<span data-ttu-id="b905b-129">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b905b-129">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="b905b-130">-Name</span></span>
<span data-ttu-id="b905b-131">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="b905b-131">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-132">-覆寫</span><span class="sxs-lookup"><span data-stu-id="b905b-132">-Overwrite</span></span>
<span data-ttu-id="b905b-133">表示此 Cmdlet 會覆寫目的地容器中具有相同首碼的任何 VHD。</span><span class="sxs-lookup"><span data-stu-id="b905b-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-134">-路徑</span><span class="sxs-lookup"><span data-stu-id="b905b-134">-Path</span></span>
<span data-ttu-id="b905b-135">儲存所捕獲影像範本的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b905b-135">The file path in which the template of the captured image is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b905b-136">-ResourceGroupName</span></span>
<span data-ttu-id="b905b-137">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b905b-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="b905b-138">-VHDNamePrefix</span></span>
<span data-ttu-id="b905b-139">指定構成 VMImage 儲存設定檔之 Blob 名稱中的首碼。</span><span class="sxs-lookup"><span data-stu-id="b905b-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="b905b-140">例如，作業系統磁片的首碼 vhdPrefix 會導致 vhdPrefix-osax 名稱 \<guid\> 。vhd。</span><span class="sxs-lookup"><span data-stu-id="b905b-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b905b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b905b-141">CommonParameters</span></span>
<span data-ttu-id="b905b-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b905b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b905b-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b905b-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b905b-144">輸入</span><span class="sxs-lookup"><span data-stu-id="b905b-144">INPUTS</span></span>

### <span data-ttu-id="b905b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b905b-145">System.String</span></span>

### <span data-ttu-id="b905b-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b905b-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b905b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b905b-147">OUTPUTS</span></span>

### <span data-ttu-id="b905b-148">Microsoft.Azure.Commands.Compute.models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="b905b-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="b905b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b905b-149">NOTES</span></span>

## <span data-ttu-id="b905b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b905b-150">RELATED LINKS</span></span>

[<span data-ttu-id="b905b-151">Get-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="b905b-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="b905b-152">Get-AzEVImageOffer</span><span class="sxs-lookup"><span data-stu-id="b905b-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="b905b-153">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="b905b-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b905b-154">Get-AzKUImageSku</span><span class="sxs-lookup"><span data-stu-id="b905b-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="b905b-155">Set-AzMS</span><span class="sxs-lookup"><span data-stu-id="b905b-155">Set-AzVM</span></span>](./Set-AzVM.md)


