---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: fddf20c748591f339ffa3cf66f3aba4a189ec3db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450255"
---
# <span data-ttu-id="66095-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="66095-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="66095-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66095-102">SYNOPSIS</span></span>
<span data-ttu-id="66095-103">將資料磁片新增至影像物件。</span><span class="sxs-lookup"><span data-stu-id="66095-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66095-104">句法</span><span class="sxs-lookup"><span data-stu-id="66095-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66095-105">說明</span><span class="sxs-lookup"><span data-stu-id="66095-105">DESCRIPTION</span></span>
<span data-ttu-id="66095-106">**AzureRmImageDataDisk** Cmdlet 會將資料磁片新增到 image 物件。</span><span class="sxs-lookup"><span data-stu-id="66095-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="66095-107">示例</span><span class="sxs-lookup"><span data-stu-id="66095-107">EXAMPLES</span></span>

### <span data-ttu-id="66095-108">範例1</span><span class="sxs-lookup"><span data-stu-id="66095-108">Example 1</span></span>
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

<span data-ttu-id="66095-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="66095-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="66095-110">接下來的三個命令會將作業系統磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="66095-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="66095-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="66095-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="66095-112">接下來的三個命令會將作業系統磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="66095-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="66095-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="66095-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="66095-114">最後一個命令會在資源群組 ResourceGroup01 中建立名為 ImageName01 的影像。</span><span class="sxs-lookup"><span data-stu-id="66095-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="66095-115">參數</span><span class="sxs-lookup"><span data-stu-id="66095-115">PARAMETERS</span></span>

### <span data-ttu-id="66095-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="66095-116">-BlobUri</span></span>
<span data-ttu-id="66095-117">指定 blob 的連結（作為 URI）。</span><span class="sxs-lookup"><span data-stu-id="66095-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="66095-118">-快取</span><span class="sxs-lookup"><span data-stu-id="66095-118">-Caching</span></span>
<span data-ttu-id="66095-119">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="66095-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66095-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66095-120">-DefaultProfile</span></span>
<span data-ttu-id="66095-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66095-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66095-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="66095-122">-DiskSizeGB</span></span>
<span data-ttu-id="66095-123">以 Gb (GB) 指定磁片的大小。</span><span class="sxs-lookup"><span data-stu-id="66095-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66095-124">-影像</span><span class="sxs-lookup"><span data-stu-id="66095-124">-Image</span></span>
<span data-ttu-id="66095-125">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="66095-125">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66095-126">-Lun</span><span class="sxs-lookup"><span data-stu-id="66095-126">-Lun</span></span>
<span data-ttu-id="66095-127">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="66095-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66095-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="66095-128">-ManagedDiskId</span></span>
<span data-ttu-id="66095-129">指定受管理磁片的 ID。</span><span class="sxs-lookup"><span data-stu-id="66095-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="66095-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="66095-130">-SnapshotId</span></span>
<span data-ttu-id="66095-131">指定快照的識別碼。</span><span class="sxs-lookup"><span data-stu-id="66095-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="66095-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="66095-132">-StorageAccountType</span></span>
<span data-ttu-id="66095-133">資料影像磁片的儲存帳戶類型</span><span class="sxs-lookup"><span data-stu-id="66095-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="66095-134">-確認</span><span class="sxs-lookup"><span data-stu-id="66095-134">-Confirm</span></span>
<span data-ttu-id="66095-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66095-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66095-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66095-136">-WhatIf</span></span>
<span data-ttu-id="66095-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66095-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66095-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66095-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66095-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66095-139">CommonParameters</span></span>
<span data-ttu-id="66095-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66095-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66095-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66095-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66095-142">輸入</span><span class="sxs-lookup"><span data-stu-id="66095-142">INPUTS</span></span>

### <span data-ttu-id="66095-143">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="66095-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="66095-144">System.object</span><span class="sxs-lookup"><span data-stu-id="66095-144">System.Int32</span></span>

### <span data-ttu-id="66095-145">System.object</span><span class="sxs-lookup"><span data-stu-id="66095-145">System.String</span></span>

### <span data-ttu-id="66095-146">"CachingTypes" 1 [[21.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="66095-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="66095-147">輸出</span><span class="sxs-lookup"><span data-stu-id="66095-147">OUTPUTS</span></span>

### <span data-ttu-id="66095-148">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="66095-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="66095-149">筆記</span><span class="sxs-lookup"><span data-stu-id="66095-149">NOTES</span></span>

## <span data-ttu-id="66095-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="66095-150">RELATED LINKS</span></span>