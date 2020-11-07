---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: d5fd6e6dea5af9ed3d8bc02e69f155e74a4bb3f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958827"
---
# <span data-ttu-id="b7c8e-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b7c8e-101">Get-AzVMImage</span></span>

## <span data-ttu-id="b7c8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c8e-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b7c8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7c8e-104">SYNTAX</span></span>

### <span data-ttu-id="b7c8e-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="b7c8e-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7c8e-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="b7c8e-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c8e-107">說明</span><span class="sxs-lookup"><span data-stu-id="b7c8e-107">DESCRIPTION</span></span>
<span data-ttu-id="b7c8e-108">**AzVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b7c8e-109">示例</span><span class="sxs-lookup"><span data-stu-id="b7c8e-109">EXAMPLES</span></span>

### <span data-ttu-id="b7c8e-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="b7c8e-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="b7c8e-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="b7c8e-112">範例2：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="b7c8e-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="b7c8e-113">這個命令會取得符合指定值的特定 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="b7c8e-114">範例3：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="b7c8e-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="b7c8e-115">這個命令會從篩選版本中取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="b7c8e-116">參數</span><span class="sxs-lookup"><span data-stu-id="b7c8e-116">PARAMETERS</span></span>

### <span data-ttu-id="b7c8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c8e-117">-DefaultProfile</span></span>
<span data-ttu-id="b7c8e-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c8e-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="b7c8e-119">-FilterExpression</span></span>
<span data-ttu-id="b7c8e-120">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-121">-位置</span><span class="sxs-lookup"><span data-stu-id="b7c8e-121">-Location</span></span>
<span data-ttu-id="b7c8e-122">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-122">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-123">-優惠</span><span class="sxs-lookup"><span data-stu-id="b7c8e-123">-Offer</span></span>
<span data-ttu-id="b7c8e-124">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="b7c8e-125">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b7c8e-126">-PublisherName</span></span>
<span data-ttu-id="b7c8e-127">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="b7c8e-128">若要取得影像發行商，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="b7c8e-129">-Skus</span></span>
<span data-ttu-id="b7c8e-130">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="b7c8e-131">若要取得 SKU，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-132">-版本</span><span class="sxs-lookup"><span data-stu-id="b7c8e-132">-Version</span></span>
<span data-ttu-id="b7c8e-133">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="b7c8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c8e-134">CommonParameters</span></span>
<span data-ttu-id="b7c8e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c8e-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b7c8e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c8e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b7c8e-137">INPUTS</span></span>

### <span data-ttu-id="b7c8e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b7c8e-138">System.String</span></span>

## <span data-ttu-id="b7c8e-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b7c8e-139">OUTPUTS</span></span>

### <span data-ttu-id="b7c8e-140">PSVirtualMachineImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b7c8e-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="b7c8e-141">PSVirtualMachineImageDetail 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b7c8e-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="b7c8e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b7c8e-142">NOTES</span></span>

## <span data-ttu-id="b7c8e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7c8e-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7c8e-144">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="b7c8e-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="b7c8e-145">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b7c8e-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b7c8e-146">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="b7c8e-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="b7c8e-147">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b7c8e-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


