---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456799"
---
# <span data-ttu-id="8ba96-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8ba96-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="8ba96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ba96-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba96-103">將虛擬機器儲存為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="8ba96-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba96-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ba96-104">SYNTAX</span></span>

### <span data-ttu-id="8ba96-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="8ba96-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ba96-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8ba96-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ba96-107">說明</span><span class="sxs-lookup"><span data-stu-id="8ba96-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba96-108">AzureRmVMImage Cmdlet 會將虛擬機器 **儲存** 為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="8ba96-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="8ba96-109">在您建立虛擬機器影像之前，請 sysprep 虛擬機器，然後使用 Set-AzureRmVM Cmdlet 將它標示為一般化。</span><span class="sxs-lookup"><span data-stu-id="8ba96-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="8ba96-110">這個 Cmdlet 的輸出是 (JSON) 範本的 JavaScript 物件符號。</span><span class="sxs-lookup"><span data-stu-id="8ba96-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="8ba96-111">您可以從捕獲的映射部署虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8ba96-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="8ba96-112">示例</span><span class="sxs-lookup"><span data-stu-id="8ba96-112">EXAMPLES</span></span>

### <span data-ttu-id="8ba96-113">範例1：捕獲虛擬機器</span><span class="sxs-lookup"><span data-stu-id="8ba96-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="8ba96-114">第一個命令會將名為 VirtualMachine07 的虛擬機器標示為「一般化」。</span><span class="sxs-lookup"><span data-stu-id="8ba96-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="8ba96-115">第二個命令會將名為 VirtualMachine07 的虛擬機器捕獲為 VMImage。</span><span class="sxs-lookup"><span data-stu-id="8ba96-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="8ba96-116">**Output** 屬性會傳回 JSON 範本。</span><span class="sxs-lookup"><span data-stu-id="8ba96-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="8ba96-117">參數</span><span class="sxs-lookup"><span data-stu-id="8ba96-117">PARAMETERS</span></span>

### <span data-ttu-id="8ba96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba96-118">-DefaultProfile</span></span>
<span data-ttu-id="8ba96-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ba96-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ba96-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="8ba96-120">-DestinationContainerName</span></span>
<span data-ttu-id="8ba96-121">指定您想要保留影像之「系統」容器內的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba96-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="8ba96-122">如果容器不存在，就會為您建立。</span><span class="sxs-lookup"><span data-stu-id="8ba96-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="8ba96-123">組成 VMImage 的虛擬硬碟 (Vhd) 會駐留在此參數指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="8ba96-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="8ba96-124">如果 Vhd 分佈在多個儲存空間帳戶中，這個 Cmdlet 會在每個儲存空間帳戶中建立一個具有此名稱的容器。</span><span class="sxs-lookup"><span data-stu-id="8ba96-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="8ba96-125">所儲存影像的 URL 類似以下所示：</span><span class="sxs-lookup"><span data-stu-id="8ba96-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="8ba96-126">\<storageAccountName\>blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx。</span><span class="sxs-lookup"><span data-stu-id="8ba96-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

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

### <span data-ttu-id="8ba96-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8ba96-127">-Id</span></span>
<span data-ttu-id="8ba96-128">指定虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba96-128">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="8ba96-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ba96-129">-Name</span></span>
<span data-ttu-id="8ba96-130">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba96-130">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba96-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8ba96-131">-Overwrite</span></span>
<span data-ttu-id="8ba96-132">表示此 Cmdlet 會覆寫目的地容器中具有相同前置詞的任何 Vhd。</span><span class="sxs-lookup"><span data-stu-id="8ba96-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

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

### <span data-ttu-id="8ba96-133">-Path</span><span class="sxs-lookup"><span data-stu-id="8ba96-133">-Path</span></span>
<span data-ttu-id="8ba96-134">指定 VHD 的路徑。</span><span class="sxs-lookup"><span data-stu-id="8ba96-134">Specifies the path of the VHD.</span></span>

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

### <span data-ttu-id="8ba96-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba96-135">-ResourceGroupName</span></span>
<span data-ttu-id="8ba96-136">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ba96-136">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8ba96-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="8ba96-137">-VHDNamePrefix</span></span>
<span data-ttu-id="8ba96-138">在組成 VMImage 儲存設定檔的 blob 名稱中，指定前置詞。</span><span class="sxs-lookup"><span data-stu-id="8ba96-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="8ba96-139">例如，作業系統磁片的首碼 vhdPrefix 會產生 name vhdPrefix- \<guid\> osdisk .。。vhd.</span><span class="sxs-lookup"><span data-stu-id="8ba96-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

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

### <span data-ttu-id="8ba96-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba96-140">CommonParameters</span></span>
<span data-ttu-id="8ba96-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ba96-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba96-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ba96-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba96-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8ba96-143">INPUTS</span></span>

## <span data-ttu-id="8ba96-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8ba96-144">OUTPUTS</span></span>

## <span data-ttu-id="8ba96-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8ba96-145">NOTES</span></span>

## <span data-ttu-id="8ba96-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ba96-146">RELATED LINKS</span></span>

[<span data-ttu-id="8ba96-147">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8ba96-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="8ba96-148">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8ba96-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="8ba96-149">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8ba96-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8ba96-150">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8ba96-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8ba96-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba96-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)


