---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: f2d5903de64655b79765774f7232790f8a00ffc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626131"
---
# <span data-ttu-id="a9b63-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="a9b63-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="a9b63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9b63-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b63-103">建立可設定的影像物件。</span><span class="sxs-lookup"><span data-stu-id="a9b63-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9b63-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9b63-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9b63-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9b63-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b63-106">**新的-AzureRmImageConfig** Cmdlet 會建立可設定的影像物件。</span><span class="sxs-lookup"><span data-stu-id="a9b63-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="a9b63-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9b63-107">EXAMPLES</span></span>

### <span data-ttu-id="a9b63-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a9b63-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="a9b63-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="a9b63-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="a9b63-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="a9b63-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="a9b63-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="a9b63-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="a9b63-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="a9b63-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="a9b63-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="a9b63-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="a9b63-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="a9b63-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a9b63-115">參數</span><span class="sxs-lookup"><span data-stu-id="a9b63-115">PARAMETERS</span></span>

### <span data-ttu-id="a9b63-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="a9b63-116">-DataDisk</span></span>
<span data-ttu-id="a9b63-117">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="a9b63-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="a9b63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b63-118">-DefaultProfile</span></span>
<span data-ttu-id="a9b63-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9b63-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b63-120">-位置</span><span class="sxs-lookup"><span data-stu-id="a9b63-120">-Location</span></span>
<span data-ttu-id="a9b63-121">指定位置。</span><span class="sxs-lookup"><span data-stu-id="a9b63-121">Specifies a location.</span></span>

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

### <span data-ttu-id="a9b63-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="a9b63-122">-OsDisk</span></span>
<span data-ttu-id="a9b63-123">指定作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="a9b63-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="a9b63-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a9b63-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="a9b63-125">指定來源虛擬電腦 ID。</span><span class="sxs-lookup"><span data-stu-id="a9b63-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="a9b63-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9b63-126">-Tag</span></span>
<span data-ttu-id="a9b63-127">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a9b63-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a9b63-128">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a9b63-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a9b63-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="a9b63-129">-ZoneResilient</span></span>
<span data-ttu-id="a9b63-130">啟用區域彈性</span><span class="sxs-lookup"><span data-stu-id="a9b63-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="a9b63-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a9b63-131">-Confirm</span></span>
<span data-ttu-id="a9b63-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9b63-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9b63-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9b63-133">-WhatIf</span></span>
<span data-ttu-id="a9b63-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9b63-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9b63-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9b63-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9b63-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b63-136">CommonParameters</span></span>
<span data-ttu-id="a9b63-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9b63-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b63-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9b63-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b63-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a9b63-139">INPUTS</span></span>

### <span data-ttu-id="a9b63-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a9b63-140">System.String</span></span>

### <span data-ttu-id="a9b63-141">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a9b63-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a9b63-142">ImageOSDisk 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="a9b63-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="a9b63-143">ImageDataDisk [] 的計算模型。</span><span class="sxs-lookup"><span data-stu-id="a9b63-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="a9b63-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a9b63-144">OUTPUTS</span></span>

### <span data-ttu-id="a9b63-145">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a9b63-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="a9b63-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a9b63-146">NOTES</span></span>

## <span data-ttu-id="a9b63-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9b63-147">RELATED LINKS</span></span>
