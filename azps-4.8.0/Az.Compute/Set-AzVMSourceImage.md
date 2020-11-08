---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsourceimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSourceImage.md
ms.openlocfilehash: a1ed1fa266638891507b6853199bff23d23aa1b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128355"
---
# <span data-ttu-id="8e681-101">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="8e681-101">Set-AzVMSourceImage</span></span>

## <span data-ttu-id="8e681-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e681-102">SYNOPSIS</span></span>
<span data-ttu-id="8e681-103">指定虛擬機器的影像。</span><span class="sxs-lookup"><span data-stu-id="8e681-103">Specifies the image for a virtual machine.</span></span>

## <span data-ttu-id="8e681-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e681-104">SYNTAX</span></span>

### <span data-ttu-id="8e681-105">ImageReferenceSkuParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8e681-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e681-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e681-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e681-107">說明</span><span class="sxs-lookup"><span data-stu-id="8e681-107">DESCRIPTION</span></span>
<span data-ttu-id="8e681-108">**AzVMSourceImage** Cmdlet 會指定要用於虛擬機器的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="8e681-108">The **Set-AzVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="8e681-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e681-109">EXAMPLES</span></span>

### <span data-ttu-id="8e681-110">範例1：設定影像的值</span><span class="sxs-lookup"><span data-stu-id="8e681-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="8e681-111">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e681-111">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="8e681-112">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e681-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="8e681-113">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="8e681-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="8e681-114">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="8e681-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="8e681-115">最終命令會設定發行者名稱、優惠、SKU 及版本的值。</span><span class="sxs-lookup"><span data-stu-id="8e681-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="8e681-116">**AzVMImagePublisher** 、 **AzVMImageOffer** 、 **AzVMImageSku** 和 **AzVMImage** Cmdlet 都可以探索這些設定。</span><span class="sxs-lookup"><span data-stu-id="8e681-116">The **Get-AzVMImagePublisher** , **Get-AzVMImageOffer** , **Get-AzVMImageSku** , and **Get-AzVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="8e681-117">參數</span><span class="sxs-lookup"><span data-stu-id="8e681-117">PARAMETERS</span></span>

### <span data-ttu-id="8e681-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e681-118">-DefaultProfile</span></span>
<span data-ttu-id="8e681-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e681-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e681-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8e681-120">-Id</span></span>
<span data-ttu-id="8e681-121">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="8e681-121">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e681-122">-優惠</span><span class="sxs-lookup"><span data-stu-id="8e681-122">-Offer</span></span>
<span data-ttu-id="8e681-123">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="8e681-123">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="8e681-124">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e681-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e681-125">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="8e681-125">-PublisherName</span></span>
<span data-ttu-id="8e681-126">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e681-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="8e681-127">若要取得發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e681-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e681-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="8e681-128">-Skus</span></span>
<span data-ttu-id="8e681-129">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="8e681-129">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="8e681-130">若要取得 Sku，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e681-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e681-131">-版本</span><span class="sxs-lookup"><span data-stu-id="8e681-131">-Version</span></span>
<span data-ttu-id="8e681-132">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="8e681-132">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="8e681-133">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="8e681-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e681-134">-VM</span><span class="sxs-lookup"><span data-stu-id="8e681-134">-VM</span></span>
<span data-ttu-id="8e681-135">指定要設定的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="8e681-135">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e681-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e681-136">CommonParameters</span></span>
<span data-ttu-id="8e681-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e681-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e681-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e681-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e681-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8e681-139">INPUTS</span></span>

### <span data-ttu-id="8e681-140">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8e681-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8e681-141">System.object</span><span class="sxs-lookup"><span data-stu-id="8e681-141">System.String</span></span>

## <span data-ttu-id="8e681-142">輸出</span><span class="sxs-lookup"><span data-stu-id="8e681-142">OUTPUTS</span></span>

### <span data-ttu-id="8e681-143">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="8e681-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8e681-144">筆記</span><span class="sxs-lookup"><span data-stu-id="8e681-144">NOTES</span></span>

## <span data-ttu-id="8e681-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e681-145">RELATED LINKS</span></span>

[<span data-ttu-id="8e681-146">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8e681-146">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="8e681-147">AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8e681-147">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="8e681-148">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="8e681-148">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="8e681-149">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8e681-149">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8e681-150">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8e681-150">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="8e681-151">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8e681-151">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

