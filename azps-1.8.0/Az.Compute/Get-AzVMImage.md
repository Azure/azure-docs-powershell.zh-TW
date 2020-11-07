---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788497"
---
# <span data-ttu-id="9db4a-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9db4a-101">Get-AzVMImage</span></span>

## <span data-ttu-id="9db4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9db4a-102">SYNOPSIS</span></span>
<span data-ttu-id="9db4a-103">取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9db4a-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9db4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9db4a-104">SYNTAX</span></span>

### <span data-ttu-id="9db4a-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9db4a-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9db4a-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9db4a-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9db4a-107">說明</span><span class="sxs-lookup"><span data-stu-id="9db4a-107">DESCRIPTION</span></span>
<span data-ttu-id="9db4a-108">**AzVMImage** Cmdlet 會取得 VMImage 的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9db4a-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9db4a-109">示例</span><span class="sxs-lookup"><span data-stu-id="9db4a-109">EXAMPLES</span></span>

### <span data-ttu-id="9db4a-110">範例1：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="9db4a-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="9db4a-111">這個命令會取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="9db4a-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="9db4a-112">範例2：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="9db4a-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="9db4a-113">這個命令會取得符合指定值的特定 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="9db4a-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="9db4a-114">範例3：取得 VMImage 物件</span><span class="sxs-lookup"><span data-stu-id="9db4a-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="9db4a-115">這個命令會從篩選版本中取得符合指定值的所有 VMImage 版本。</span><span class="sxs-lookup"><span data-stu-id="9db4a-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="9db4a-116">參數</span><span class="sxs-lookup"><span data-stu-id="9db4a-116">PARAMETERS</span></span>

### <span data-ttu-id="9db4a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db4a-117">-DefaultProfile</span></span>
<span data-ttu-id="9db4a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9db4a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db4a-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9db4a-119">-FilterExpression</span></span>
<span data-ttu-id="9db4a-120">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="9db4a-120">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="9db4a-121">-位置</span><span class="sxs-lookup"><span data-stu-id="9db4a-121">-Location</span></span>
<span data-ttu-id="9db4a-122">指定 VMImage 的位置。</span><span class="sxs-lookup"><span data-stu-id="9db4a-122">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9db4a-123">-優惠</span><span class="sxs-lookup"><span data-stu-id="9db4a-123">-Offer</span></span>
<span data-ttu-id="9db4a-124">指定 VMImage 產品類型。</span><span class="sxs-lookup"><span data-stu-id="9db4a-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9db4a-125">若要取得影像優惠，請使用 Get-AzVMImageOffer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9db4a-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9db4a-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9db4a-126">-PublisherName</span></span>
<span data-ttu-id="9db4a-127">指定 VMImage 的發行者。</span><span class="sxs-lookup"><span data-stu-id="9db4a-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9db4a-128">若要取得影像發行商，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9db4a-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9db4a-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="9db4a-129">-Skus</span></span>
<span data-ttu-id="9db4a-130">指定 VMImage SKU。</span><span class="sxs-lookup"><span data-stu-id="9db4a-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9db4a-131">若要取得 SKU，請使用 Get-AzVMImageSku Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9db4a-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9db4a-132">-版本</span><span class="sxs-lookup"><span data-stu-id="9db4a-132">-Version</span></span>
<span data-ttu-id="9db4a-133">指定 VMImage 的版本。</span><span class="sxs-lookup"><span data-stu-id="9db4a-133">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="9db4a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db4a-134">CommonParameters</span></span>
<span data-ttu-id="9db4a-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9db4a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db4a-136">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9db4a-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db4a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9db4a-137">INPUTS</span></span>

### <span data-ttu-id="9db4a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="9db4a-138">System.String</span></span>

## <span data-ttu-id="9db4a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9db4a-139">OUTPUTS</span></span>

### <span data-ttu-id="9db4a-140">PSVirtualMachineImage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9db4a-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="9db4a-141">PSVirtualMachineImageDetail 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9db4a-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="9db4a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9db4a-142">NOTES</span></span>

## <span data-ttu-id="9db4a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9db4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="9db4a-144">AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9db4a-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9db4a-145">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9db4a-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9db4a-146">AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9db4a-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9db4a-147">儲存-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9db4a-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


