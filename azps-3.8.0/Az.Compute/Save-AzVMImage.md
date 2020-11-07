---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958029"
---
# <span data-ttu-id="69490-101">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="69490-101">Save-AzVMImage</span></span>

## <span data-ttu-id="69490-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69490-102">SYNOPSIS</span></span>
<span data-ttu-id="69490-103">將虛擬機器儲存為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="69490-103">Saves a virtual machine as a VMImage.</span></span>

## <span data-ttu-id="69490-104">句法</span><span class="sxs-lookup"><span data-stu-id="69490-104">SYNTAX</span></span>

### <span data-ttu-id="69490-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="69490-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69490-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="69490-106">IdParameterSetName</span></span>
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69490-107">說明</span><span class="sxs-lookup"><span data-stu-id="69490-107">DESCRIPTION</span></span>
<span data-ttu-id="69490-108">AzVMImage Cmdlet 會將虛擬機器 **儲存** 為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="69490-108">The **Save-AzVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="69490-109">在您建立虛擬機器影像之前，請 sysprep 虛擬機器，然後使用 Set-AzVM Cmdlet 將它標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="69490-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzVM cmdlet.</span></span>
<span data-ttu-id="69490-110">這個 Cmdlet 的輸出是 (JSON) 範本的 JavaScript 物件符號。</span><span class="sxs-lookup"><span data-stu-id="69490-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="69490-111">您可以從捕獲的映射部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="69490-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="69490-112">示例</span><span class="sxs-lookup"><span data-stu-id="69490-112">EXAMPLES</span></span>

### <span data-ttu-id="69490-113">範例1：捕獲虛擬機器</span><span class="sxs-lookup"><span data-stu-id="69490-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="69490-114">第一個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="69490-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>
<span data-ttu-id="69490-115">第二個命令會將名為 VirtualMachine07 的虛擬機器捕獲為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="69490-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="69490-116">**Output** 屬性會傳回 JSON 範本。</span><span class="sxs-lookup"><span data-stu-id="69490-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="69490-117">參數</span><span class="sxs-lookup"><span data-stu-id="69490-117">PARAMETERS</span></span>

### <span data-ttu-id="69490-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69490-118">-AsJob</span></span>
<span data-ttu-id="69490-119">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="69490-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="69490-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69490-120">-DefaultProfile</span></span>
<span data-ttu-id="69490-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69490-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69490-122">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="69490-122">-DestinationContainerName</span></span>
<span data-ttu-id="69490-123">指定您想要保留影像之「系統」容器內的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="69490-123">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>
<span data-ttu-id="69490-124">如果容器不存在，就會為您建立。</span><span class="sxs-lookup"><span data-stu-id="69490-124">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="69490-125">組成 VMImage 的虛擬硬碟 (Vhd) 會駐留在此參數指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="69490-125">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="69490-126">如果 Vhd 分佈在多個儲存空間帳戶中，這個 Cmdlet 會在每個儲存空間帳戶中建立一個具有此名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="69490-126">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="69490-127">已儲存影像的 URL 類似： HTTPs:// \< storageAccountName \> . blob.core.windows.net/system/Microsoft.Compute/Images/ \< imagesContainer \> / \< vhdPrefix-osDisk \> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx..。</span><span class="sxs-lookup"><span data-stu-id="69490-127">The URL of the saved image is similar to: https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="69490-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="69490-128">-Id</span></span>
<span data-ttu-id="69490-129">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="69490-129">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="69490-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="69490-130">-Name</span></span>
<span data-ttu-id="69490-131">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="69490-131">Specifies a name.</span></span>

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

### <span data-ttu-id="69490-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="69490-132">-Overwrite</span></span>
<span data-ttu-id="69490-133">表示此 Cmdlet 會覆寫目的地容器中具有相同前置詞的任何 Vhd。</span><span class="sxs-lookup"><span data-stu-id="69490-133">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="69490-134">-Path</span><span class="sxs-lookup"><span data-stu-id="69490-134">-Path</span></span>
<span data-ttu-id="69490-135">儲存所捕獲影像範本的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="69490-135">The file path in which the template of the captured image is stored.</span></span>

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

### <span data-ttu-id="69490-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69490-136">-ResourceGroupName</span></span>
<span data-ttu-id="69490-137">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69490-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="69490-138">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="69490-138">-VHDNamePrefix</span></span>
<span data-ttu-id="69490-139">在組成 VMImage 儲存設定檔的 blob 名稱中，指定前置詞。</span><span class="sxs-lookup"><span data-stu-id="69490-139">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>
<span data-ttu-id="69490-140">例如，作業系統磁片的首碼 vhdPrefix 會產生 name vhdPrefix-osdisk。 \<guid.empty \> 。</span><span class="sxs-lookup"><span data-stu-id="69490-140">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="69490-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69490-141">CommonParameters</span></span>
<span data-ttu-id="69490-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69490-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69490-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="69490-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69490-144">輸入</span><span class="sxs-lookup"><span data-stu-id="69490-144">INPUTS</span></span>

### <span data-ttu-id="69490-145">System.object</span><span class="sxs-lookup"><span data-stu-id="69490-145">System.String</span></span>

### <span data-ttu-id="69490-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="69490-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="69490-147">輸出</span><span class="sxs-lookup"><span data-stu-id="69490-147">OUTPUTS</span></span>

### <span data-ttu-id="69490-148">PSComputeLongRunningOperation 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="69490-148">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="69490-149">筆記</span><span class="sxs-lookup"><span data-stu-id="69490-149">NOTES</span></span>

## <span data-ttu-id="69490-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="69490-150">RELATED LINKS</span></span>

[<span data-ttu-id="69490-151">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="69490-151">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="69490-152">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="69490-152">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="69490-153">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="69490-153">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="69490-154">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="69490-154">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="69490-155">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="69490-155">Set-AzVM</span></span>](./Set-AzVM.md)


