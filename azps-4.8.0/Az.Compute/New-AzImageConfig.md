---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969861"
---
# <span data-ttu-id="41b1f-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="41b1f-101">New-AzImageConfig</span></span>

## <span data-ttu-id="41b1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="41b1f-103">建立可設定的影像物件。</span><span class="sxs-lookup"><span data-stu-id="41b1f-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="41b1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="41b1f-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41b1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="41b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="41b1f-106">**新的-AzImageConfig** Cmdlet 會建立可設定的影像物件。</span><span class="sxs-lookup"><span data-stu-id="41b1f-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="41b1f-107">示例</span><span class="sxs-lookup"><span data-stu-id="41b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="41b1f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="41b1f-108">Example 1</span></span>
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

<span data-ttu-id="41b1f-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="41b1f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="41b1f-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="41b1f-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="41b1f-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="41b1f-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="41b1f-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="41b1f-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="41b1f-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="41b1f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="41b1f-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="41b1f-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="41b1f-115">參數</span><span class="sxs-lookup"><span data-stu-id="41b1f-115">PARAMETERS</span></span>

### <span data-ttu-id="41b1f-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="41b1f-116">-DataDisk</span></span>
<span data-ttu-id="41b1f-117">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="41b1f-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="41b1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b1f-118">-DefaultProfile</span></span>
<span data-ttu-id="41b1f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41b1f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41b1f-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="41b1f-120">-HyperVGeneration</span></span>
<span data-ttu-id="41b1f-121">指定從影像建立之虛擬機器的 HyperVGeneration 類型。</span><span class="sxs-lookup"><span data-stu-id="41b1f-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="41b1f-122">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="41b1f-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="41b1f-123">-位置</span><span class="sxs-lookup"><span data-stu-id="41b1f-123">-Location</span></span>
<span data-ttu-id="41b1f-124">指定位置。</span><span class="sxs-lookup"><span data-stu-id="41b1f-124">Specifies a location.</span></span>

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

### <span data-ttu-id="41b1f-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="41b1f-125">-OsDisk</span></span>
<span data-ttu-id="41b1f-126">指定作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="41b1f-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="41b1f-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="41b1f-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="41b1f-128">指定來源虛擬電腦 ID。</span><span class="sxs-lookup"><span data-stu-id="41b1f-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="41b1f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="41b1f-129">-Tag</span></span>
<span data-ttu-id="41b1f-130">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="41b1f-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="41b1f-131">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="41b1f-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="41b1f-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="41b1f-132">-ZoneResilient</span></span>
<span data-ttu-id="41b1f-133">啟用區域彈性</span><span class="sxs-lookup"><span data-stu-id="41b1f-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="41b1f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="41b1f-134">-Confirm</span></span>
<span data-ttu-id="41b1f-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41b1f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41b1f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41b1f-136">-WhatIf</span></span>
<span data-ttu-id="41b1f-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41b1f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41b1f-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41b1f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41b1f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b1f-139">CommonParameters</span></span>
<span data-ttu-id="41b1f-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41b1f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b1f-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41b1f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b1f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="41b1f-142">INPUTS</span></span>

### <span data-ttu-id="41b1f-143">System.object</span><span class="sxs-lookup"><span data-stu-id="41b1f-143">System.String</span></span>

### <span data-ttu-id="41b1f-144">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="41b1f-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="41b1f-145">ImageOSDisk 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="41b1f-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="41b1f-146">ImageDataDisk [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="41b1f-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="41b1f-147">輸出</span><span class="sxs-lookup"><span data-stu-id="41b1f-147">OUTPUTS</span></span>

### <span data-ttu-id="41b1f-148">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="41b1f-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="41b1f-149">筆記</span><span class="sxs-lookup"><span data-stu-id="41b1f-149">NOTES</span></span>

## <span data-ttu-id="41b1f-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="41b1f-150">RELATED LINKS</span></span>
