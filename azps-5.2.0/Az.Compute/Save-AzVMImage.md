---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284312"
---
# <span data-ttu-id="e31ac-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e31ac-101">Save-AzVMImage</span></span>

## <span data-ttu-id="e31ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e31ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e31ac-103">將虛擬機器儲存為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="e31ac-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="e31ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="e31ac-104">SYNTAX</span></span>

### <span data-ttu-id="e31ac-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="e31ac-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e31ac-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e31ac-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e31ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="e31ac-107">DESCRIPTION</span></span>
<span data-ttu-id="e31ac-108">AzVMImage Cmdlet 會將虛擬機器 **儲存** 為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="e31ac-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="e31ac-109">在您建立虛擬機器影像之前，請 sysprep 虛擬機器，然後使用 Set-AzVM Cmdlet 將它標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="e31ac-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="e31ac-110">這個 Cmdlet 的輸出是 (JSON) 範本的 JavaScript 物件符號。</span><span class="sxs-lookup"><span data-stu-id="e31ac-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="e31ac-111">您可以從捕獲的映射部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e31ac-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="e31ac-112">示例</span><span class="sxs-lookup"><span data-stu-id="e31ac-112">EXAMPLES</span></span>

### <span data-ttu-id="e31ac-113">範例1：捕獲虛擬機器</span><span class="sxs-lookup"><span data-stu-id="e31ac-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="e31ac-114">第一個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="e31ac-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="e31ac-115">第二個命令會將名為 VirtualMachine07 的虛擬機器捕獲為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="e31ac-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="e31ac-116">**Output** 屬性會傳回 JSON 範本。</span><span class="sxs-lookup"><span data-stu-id="e31ac-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="e31ac-117">參數</span><span class="sxs-lookup"><span data-stu-id="e31ac-117">PARAMETERS</span></span>

### <span data-ttu-id="e31ac-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e31ac-118">-AsJob</span></span>
<span data-ttu-id="e31ac-119">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="e31ac-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e31ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31ac-120">-DefaultProfile</span></span>
<span data-ttu-id="e31ac-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e31ac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e31ac-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="e31ac-122">-DestinationContainerName</span></span>
<span data-ttu-id="e31ac-123">指定您想要保留影像之「系統」容器內的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="e31ac-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="e31ac-124">如果容器不存在，就會為您建立。</span><span class="sxs-lookup"><span data-stu-id="e31ac-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="e31ac-125">組成 VMImage 的虛擬硬碟 (Vhd) 會駐留在此參數指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="e31ac-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="e31ac-126">如果 Vhd 分佈在多個儲存空間帳戶中，這個 Cmdlet 會在每個儲存空間帳戶中建立一個具有此名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="e31ac-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="e31ac-127">已儲存影像的 URL 類似： blob.core.windows.net/system/Microsoft.Compute/Images/. HTTPs://。 \<storageAccountName\> \<imagesContainer\> / \<vhdPrefix-osDisk\></span><span class="sxs-lookup"><span data-stu-id="e31ac-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="e31ac-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e31ac-128">-Id</span></span>
<span data-ttu-id="e31ac-129">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e31ac-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e31ac-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="e31ac-130">-Name</span></span>
<span data-ttu-id="e31ac-131">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="e31ac-131">Specifies a name.</span></span>

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

### <span data-ttu-id="e31ac-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e31ac-132">-Overwrite</span></span>
<span data-ttu-id="e31ac-133">表示此 Cmdlet 會覆寫目的地容器中具有相同前置詞的任何 Vhd。</span><span class="sxs-lookup"><span data-stu-id="e31ac-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="e31ac-134">-Path</span><span class="sxs-lookup"><span data-stu-id="e31ac-134">-Path</span></span>
<span data-ttu-id="e31ac-135">儲存所捕獲影像範本的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="e31ac-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="e31ac-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31ac-136">-ResourceGroupName</span></span>
<span data-ttu-id="e31ac-137">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e31ac-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e31ac-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e31ac-138">-VHDNamePrefix</span></span>
<span data-ttu-id="e31ac-139">在組成 VMImage 儲存設定檔的 blob 名稱中，指定前置詞。</span><span class="sxs-lookup"><span data-stu-id="e31ac-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="e31ac-140">例如，作業系統磁片的首碼 vhdPrefix 會產生 name vhdPrefix- \<guid\> osdisk .。。vhd.</span><span class="sxs-lookup"><span data-stu-id="e31ac-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="e31ac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31ac-141">CommonParameters</span></span>
<span data-ttu-id="e31ac-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e31ac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31ac-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e31ac-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31ac-144">輸入</span><span class="sxs-lookup"><span data-stu-id="e31ac-144">INPUTS</span></span>

### <span data-ttu-id="e31ac-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e31ac-145">System.String</span></span>

### <span data-ttu-id="e31ac-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e31ac-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e31ac-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e31ac-147">OUTPUTS</span></span>

### <span data-ttu-id="e31ac-148">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="e31ac-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e31ac-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e31ac-149">NOTES</span></span>

## <span data-ttu-id="e31ac-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e31ac-150">RELATED LINKS</span></span>

[<span data-ttu-id="e31ac-151">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e31ac-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="e31ac-152">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e31ac-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="e31ac-153">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e31ac-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="e31ac-154">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e31ac-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="e31ac-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="e31ac-155">Set-AzVM</span></span>](./Set-AzVM.md)


