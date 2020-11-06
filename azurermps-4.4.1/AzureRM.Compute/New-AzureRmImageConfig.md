---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: a18fe089cba54f6cbf0d70469a17f2d8f797b2e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445092"
---
# <span data-ttu-id="8de37-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="8de37-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="8de37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8de37-102">SYNOPSIS</span></span>
<span data-ttu-id="8de37-103">建立可設定的影像物件。</span><span class="sxs-lookup"><span data-stu-id="8de37-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8de37-104">句法</span><span class="sxs-lookup"><span data-stu-id="8de37-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de37-105">說明</span><span class="sxs-lookup"><span data-stu-id="8de37-105">DESCRIPTION</span></span>
<span data-ttu-id="8de37-106">**新的-AzureRmImageConfig** Cmdlet 會建立可設定的影像物件。</span><span class="sxs-lookup"><span data-stu-id="8de37-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="8de37-107">示例</span><span class="sxs-lookup"><span data-stu-id="8de37-107">EXAMPLES</span></span>

### <span data-ttu-id="8de37-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8de37-108">Example 1</span></span>
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

<span data-ttu-id="8de37-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="8de37-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="8de37-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="8de37-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="8de37-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="8de37-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="8de37-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="8de37-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="8de37-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="8de37-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="8de37-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="8de37-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8de37-115">參數</span><span class="sxs-lookup"><span data-stu-id="8de37-115">PARAMETERS</span></span>

### <span data-ttu-id="8de37-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="8de37-116">-DataDisk</span></span>
<span data-ttu-id="8de37-117">指定資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="8de37-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="8de37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de37-118">-DefaultProfile</span></span>
<span data-ttu-id="8de37-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8de37-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8de37-120">-位置</span><span class="sxs-lookup"><span data-stu-id="8de37-120">-Location</span></span>
<span data-ttu-id="8de37-121">指定位置。</span><span class="sxs-lookup"><span data-stu-id="8de37-121">Specifies a location.</span></span>

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

### <span data-ttu-id="8de37-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="8de37-122">-OsDisk</span></span>
<span data-ttu-id="8de37-123">指定作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="8de37-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="8de37-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8de37-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="8de37-125">指定來源虛擬電腦 ID。</span><span class="sxs-lookup"><span data-stu-id="8de37-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="8de37-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8de37-126">-Tag</span></span>
<span data-ttu-id="8de37-127">指定可以使用一組名稱值對來標記資源和資源群組。</span><span class="sxs-lookup"><span data-stu-id="8de37-127">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="8de37-128">-確認</span><span class="sxs-lookup"><span data-stu-id="8de37-128">-Confirm</span></span>
<span data-ttu-id="8de37-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8de37-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de37-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de37-130">-WhatIf</span></span>
<span data-ttu-id="8de37-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8de37-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8de37-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8de37-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de37-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de37-133">CommonParameters</span></span>
<span data-ttu-id="8de37-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8de37-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de37-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8de37-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de37-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8de37-136">INPUTS</span></span>

### <span data-ttu-id="8de37-137">System.object</span><span class="sxs-lookup"><span data-stu-id="8de37-137">System.String</span></span>
<span data-ttu-id="8de37-138">[System.object]。 ImageOSDisk ImageDataDisk [] [] 的計算模型. []）</span><span class="sxs-lookup"><span data-stu-id="8de37-138">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="8de37-139">輸出</span><span class="sxs-lookup"><span data-stu-id="8de37-139">OUTPUTS</span></span>

### <span data-ttu-id="8de37-140">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="8de37-140">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="8de37-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8de37-141">NOTES</span></span>

## <span data-ttu-id="8de37-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8de37-142">RELATED LINKS</span></span>

