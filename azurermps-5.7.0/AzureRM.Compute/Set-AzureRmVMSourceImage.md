---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 91B2DE2F-442D-4428-8A6F-9C2CEC181CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMSourceImage.md
ms.openlocfilehash: d96d583f871e0d037c72018339d44952562bac35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446331"
---
# <span data-ttu-id="2b8b8-101">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="2b8b8-101">Set-AzureRmVMSourceImage</span></span>

## <span data-ttu-id="2b8b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8b8-103">指定虛擬機器的影像。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-103">Specifies the image for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b8b8-104">SYNTAX</span></span>

### <span data-ttu-id="2b8b8-105">ImageReferenceSkuParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2b8b8-105">ImageReferenceSkuParameterSet (Default)</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-PublisherName] <String> [-Offer] <String> [-Skus] <String>
 [-Version] <String> [<CommonParameters>]
```

### <span data-ttu-id="2b8b8-106">ImageReferenceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b8b8-106">ImageReferenceIdParameterSet</span></span>
```
Set-AzureRmVMSourceImage [-VM] <PSVirtualMachine> [-Id] <String> [<CommonParameters>]
```

## <span data-ttu-id="2b8b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b8b8-107">DESCRIPTION</span></span>
<span data-ttu-id="2b8b8-108">**AzureRmVMSourceImage** Cmdlet 會指定要用於虛擬機器的平臺影像。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-108">The **Set-AzureRmVMSourceImage** cmdlet specifies the platform image to use for a virtual machine.</span></span>

## <span data-ttu-id="2b8b8-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b8b8-109">EXAMPLES</span></span>

### <span data-ttu-id="2b8b8-110">範例1：設定影像的值</span><span class="sxs-lookup"><span data-stu-id="2b8b8-110">Example 1: Set values for an image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "MicrosoftWindowsServer" -Offer "WindowsServer" -Skus "2012-R2-Datacenter" -Version "latest"
```

<span data-ttu-id="2b8b8-111">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-111">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="2b8b8-112">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-112">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2b8b8-113">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2b8b8-114">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-114">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="2b8b8-115">最終命令會設定發行者名稱、優惠、SKU 及版本的值。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-115">The final command sets values for publisher name, offer, SKU, and version.</span></span>
<span data-ttu-id="2b8b8-116">**AzureRmVMImagePublisher** 、 **AzureRmVMImageOffer** 、 **AzureRmVMImageSku** 和 **AzureRmVMImage** Cmdlet 都可以探索這些設定。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-116">The **Get-AzureRmVMImagePublisher** , **Get-AzureRmVMImageOffer** , **Get-AzureRmVMImageSku** , and **Get-AzureRmVMImage** cmdlets can discover these settings.</span></span>

## <span data-ttu-id="2b8b8-117">參數</span><span class="sxs-lookup"><span data-stu-id="2b8b8-117">PARAMETERS</span></span>

### <span data-ttu-id="2b8b8-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2b8b8-118">-Id</span></span>
<span data-ttu-id="2b8b8-119">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-119">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceIdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-120">-優惠</span><span class="sxs-lookup"><span data-stu-id="2b8b8-120">-Offer</span></span>
<span data-ttu-id="2b8b8-121">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-121">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="2b8b8-122">若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-123">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="2b8b8-123">-PublisherName</span></span>
<span data-ttu-id="2b8b8-124">指定 VMImage 發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2b8b8-125">若要取得發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="2b8b8-126">-Skus</span></span>
<span data-ttu-id="2b8b8-127">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-127">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="2b8b8-128">若要取得 Sku，請使用 Get-AzureRmVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-129">-版本</span><span class="sxs-lookup"><span data-stu-id="2b8b8-129">-Version</span></span>
<span data-ttu-id="2b8b8-130">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-130">Specifies a version of a VMImage.</span></span>
<span data-ttu-id="2b8b8-131">若要使用最新版本，請指定最新的值，而不是特定的版本。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: ImageReferenceSkuParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-132">-VM</span><span class="sxs-lookup"><span data-stu-id="2b8b8-132">-VM</span></span>
<span data-ttu-id="2b8b8-133">指定要設定的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-133">Specifies the local virtual machine object to configure.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8b8-134">CommonParameters</span></span>
<span data-ttu-id="2b8b8-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8b8-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8b8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2b8b8-137">INPUTS</span></span>

### <span data-ttu-id="2b8b8-138">所有</span><span class="sxs-lookup"><span data-stu-id="2b8b8-138">None</span></span>
<span data-ttu-id="2b8b8-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2b8b8-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b8b8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2b8b8-140">OUTPUTS</span></span>

## <span data-ttu-id="2b8b8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2b8b8-141">NOTES</span></span>

## <span data-ttu-id="2b8b8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b8b8-142">RELATED LINKS</span></span>

[<span data-ttu-id="2b8b8-143">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2b8b8-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2b8b8-144">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2b8b8-144">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="2b8b8-145">AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="2b8b8-145">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="2b8b8-146">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2b8b8-146">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="2b8b8-147">AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2b8b8-147">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="2b8b8-148">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2b8b8-148">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


