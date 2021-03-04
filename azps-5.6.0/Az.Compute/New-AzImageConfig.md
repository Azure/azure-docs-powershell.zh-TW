---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de59e8a9dc2fdcc4fa29409eaffc7f82e7d57b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908302"
---
# <span data-ttu-id="c502b-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="c502b-101">New-AzImageConfig</span></span>

## <span data-ttu-id="c502b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c502b-102">SYNOPSIS</span></span>
<span data-ttu-id="c502b-103">建立可配置的影像物件。</span><span class="sxs-lookup"><span data-stu-id="c502b-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="c502b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c502b-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c502b-105">描述</span><span class="sxs-lookup"><span data-stu-id="c502b-105">DESCRIPTION</span></span>
<span data-ttu-id="c502b-106">**New-AzImageConfig** Cmdlet 會建立可配置的影像物件。</span><span class="sxs-lookup"><span data-stu-id="c502b-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="c502b-107">例子</span><span class="sxs-lookup"><span data-stu-id="c502b-107">EXAMPLES</span></span>

### <span data-ttu-id="c502b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c502b-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="c502b-109">第一個命令會建立影像物件，然後將它儲存在$imageConfig變數中。</span><span class="sxs-lookup"><span data-stu-id="c502b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="c502b-110">接下來三個命令會指派 os 磁片的路徑和兩個數據磁片$osDiskVhdUri、$dataDiskVhdUri 1 及$dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="c502b-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="c502b-111">此方法僅適用于下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="c502b-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="c502b-112">接下來三個命令會各自新增作業系統磁片和兩個數據磁片磁片至儲存在 $imageConfig。</span><span class="sxs-lookup"><span data-stu-id="c502b-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c502b-113">每個磁片的 URI 會儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 和 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="c502b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="c502b-114">最後一個命令會建立資源群組 'ResourceGroup01' 中名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="c502b-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c502b-115">參數</span><span class="sxs-lookup"><span data-stu-id="c502b-115">PARAMETERS</span></span>

### <span data-ttu-id="c502b-116">-Data至上</span><span class="sxs-lookup"><span data-stu-id="c502b-116">-DataDisk</span></span>
<span data-ttu-id="c502b-117">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="c502b-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c502b-118">-DefaultProfile</span></span>
<span data-ttu-id="c502b-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c502b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c502b-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="c502b-120">-HyperVGeneration</span></span>
<span data-ttu-id="c502b-121">指定從影像建立之虛擬機器的 HyperVGeneration 類型。</span><span class="sxs-lookup"><span data-stu-id="c502b-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="c502b-122">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="c502b-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-123">-位置</span><span class="sxs-lookup"><span data-stu-id="c502b-123">-Location</span></span>
<span data-ttu-id="c502b-124">指定位置。</span><span class="sxs-lookup"><span data-stu-id="c502b-124">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-125">-Os至上</span><span class="sxs-lookup"><span data-stu-id="c502b-125">-OsDisk</span></span>
<span data-ttu-id="c502b-126">指定作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="c502b-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c502b-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="c502b-128">指定來源虛擬機器識別碼。</span><span class="sxs-lookup"><span data-stu-id="c502b-128">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-129">-標記</span><span class="sxs-lookup"><span data-stu-id="c502b-129">-Tag</span></span>
<span data-ttu-id="c502b-130">以雜湊表格形式建立索引鍵值組。</span><span class="sxs-lookup"><span data-stu-id="c502b-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c502b-131">例如：@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c502b-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="c502b-132">-ZoneResilient</span></span>
<span data-ttu-id="c502b-133">啟用區域彈性</span><span class="sxs-lookup"><span data-stu-id="c502b-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="c502b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c502b-134">-Confirm</span></span>
<span data-ttu-id="c502b-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c502b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c502b-136">-WhatIf</span></span>
<span data-ttu-id="c502b-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c502b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c502b-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c502b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c502b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c502b-139">CommonParameters</span></span>
<span data-ttu-id="c502b-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c502b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c502b-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c502b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c502b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c502b-142">INPUTS</span></span>

### <span data-ttu-id="c502b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c502b-143">System.String</span></span>

### <span data-ttu-id="c502b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c502b-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c502b-145">Microsoft.Azure.management.Compute.models.ImageOSAz</span><span class="sxs-lookup"><span data-stu-id="c502b-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="c502b-146">Microsoft.Azure.management.Compute.models.ImageDataAz[]</span><span class="sxs-lookup"><span data-stu-id="c502b-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="c502b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="c502b-147">OUTPUTS</span></span>

### <span data-ttu-id="c502b-148">Microsoft.Azure.Commands.Compute.Automation.models.PSImage</span><span class="sxs-lookup"><span data-stu-id="c502b-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c502b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="c502b-149">NOTES</span></span>

## <span data-ttu-id="c502b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="c502b-150">RELATED LINKS</span></span>
