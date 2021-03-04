---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 0075b057cecb91b618d06ad36788801a672268aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903661"
---
# <span data-ttu-id="b9aa5-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="b9aa5-101">Get-AzVMImage</span></span>

## <span data-ttu-id="b9aa5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b9aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="b9aa5-103">獲得所有版本的 VMImage。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b9aa5-104">語法</span><span class="sxs-lookup"><span data-stu-id="b9aa5-104">SYNTAX</span></span>

### <span data-ttu-id="b9aa5-105">ListMSIMage</span><span class="sxs-lookup"><span data-stu-id="b9aa5-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9aa5-106">Get部IMageDetail</span><span class="sxs-lookup"><span data-stu-id="b9aa5-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9aa5-107">描述</span><span class="sxs-lookup"><span data-stu-id="b9aa5-107">DESCRIPTION</span></span>
<span data-ttu-id="b9aa5-108">**Get-Az VMImage Cmdlet** 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="b9aa5-109">例子</span><span class="sxs-lookup"><span data-stu-id="b9aa5-109">EXAMPLES</span></span>

### <span data-ttu-id="b9aa5-110">範例 1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="b9aa5-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="b9aa5-111">此命令會獲得符合指定值的所有版本的 VMImage。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="b9aa5-112">範例 2：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="b9aa5-112">Example 2: Get VMImage object</span></span>
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
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="b9aa5-113">此命令會獲得符合指定值的特定的 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="b9aa5-114">範例 3：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="b9aa5-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="b9aa5-115">此命令會獲得所有符合指定值的 VMImage 版本，以及根據版本篩選。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="b9aa5-116">參數</span><span class="sxs-lookup"><span data-stu-id="b9aa5-116">PARAMETERS</span></span>

### <span data-ttu-id="b9aa5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9aa5-117">-DefaultProfile</span></span>
<span data-ttu-id="b9aa5-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9aa5-119">-位置</span><span class="sxs-lookup"><span data-stu-id="b9aa5-119">-Location</span></span>
<span data-ttu-id="b9aa5-120">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="b9aa5-121">-優惠</span><span class="sxs-lookup"><span data-stu-id="b9aa5-121">-Offer</span></span>
<span data-ttu-id="b9aa5-122">指定 VMImage 優惠的類型。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="b9aa5-123">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="b9aa5-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="b9aa5-124">-OrderBy</span></span>
<span data-ttu-id="b9aa5-125">指定結果的返回順序。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="b9aa5-126">格式化為 OData 查詢。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9aa5-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="b9aa5-127">-PublisherName</span></span>
<span data-ttu-id="b9aa5-128">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="b9aa5-129">若要取得影像發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="b9aa5-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="b9aa5-130">-Skus</span></span>
<span data-ttu-id="b9aa5-131">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="b9aa5-132">若要取得 SKU，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="b9aa5-133">-頂端</span><span class="sxs-lookup"><span data-stu-id="b9aa5-133">-Top</span></span>
<span data-ttu-id="b9aa5-134">指定所退回虛擬機器映射的數量上限。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9aa5-135">-版本</span><span class="sxs-lookup"><span data-stu-id="b9aa5-135">-Version</span></span>
<span data-ttu-id="b9aa5-136">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9aa5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9aa5-137">CommonParameters</span></span>
<span data-ttu-id="b9aa5-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b9aa5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9aa5-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9aa5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9aa5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b9aa5-140">INPUTS</span></span>

### <span data-ttu-id="b9aa5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b9aa5-141">System.String</span></span>

## <span data-ttu-id="b9aa5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b9aa5-142">OUTPUTS</span></span>

### <span data-ttu-id="b9aa5-143">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="b9aa5-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="b9aa5-144">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="b9aa5-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="b9aa5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b9aa5-145">NOTES</span></span>

## <span data-ttu-id="b9aa5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9aa5-146">RELATED LINKS</span></span>

[<span data-ttu-id="b9aa5-147">Get-AzEVImageOffer</span><span class="sxs-lookup"><span data-stu-id="b9aa5-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="b9aa5-148">Get-AzMSIMagePublisher</span><span class="sxs-lookup"><span data-stu-id="b9aa5-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="b9aa5-149">Get-AzKUImageSku</span><span class="sxs-lookup"><span data-stu-id="b9aa5-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="b9aa5-150">Save-AzMSIMage</span><span class="sxs-lookup"><span data-stu-id="b9aa5-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


