---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: e92d167b235c84f5f5e3a6aaa79c4af745158b72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451339"
---
# <span data-ttu-id="6879d-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6879d-101">New-AzureRmImage</span></span>

## <span data-ttu-id="6879d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6879d-102">SYNOPSIS</span></span>
<span data-ttu-id="6879d-103">建立影像。</span><span class="sxs-lookup"><span data-stu-id="6879d-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6879d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6879d-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6879d-105">說明</span><span class="sxs-lookup"><span data-stu-id="6879d-105">DESCRIPTION</span></span>
<span data-ttu-id="6879d-106">**新的-AzureRmImage** Cmdlet 會建立影像。</span><span class="sxs-lookup"><span data-stu-id="6879d-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="6879d-107">示例</span><span class="sxs-lookup"><span data-stu-id="6879d-107">EXAMPLES</span></span>

### <span data-ttu-id="6879d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6879d-108">Example 1</span></span>
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

<span data-ttu-id="6879d-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="6879d-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="6879d-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="6879d-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="6879d-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="6879d-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="6879d-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="6879d-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="6879d-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="6879d-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="6879d-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="6879d-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6879d-115">參數</span><span class="sxs-lookup"><span data-stu-id="6879d-115">PARAMETERS</span></span>

### <span data-ttu-id="6879d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6879d-116">-AsJob</span></span>
<span data-ttu-id="6879d-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6879d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6879d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6879d-118">-DefaultProfile</span></span>
<span data-ttu-id="6879d-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6879d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6879d-120">-影像</span><span class="sxs-lookup"><span data-stu-id="6879d-120">-Image</span></span>
<span data-ttu-id="6879d-121">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="6879d-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6879d-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6879d-122">-ImageName</span></span>
<span data-ttu-id="6879d-123">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="6879d-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6879d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6879d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6879d-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6879d-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6879d-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6879d-126">-Confirm</span></span>
<span data-ttu-id="6879d-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6879d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6879d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6879d-128">-WhatIf</span></span>
<span data-ttu-id="6879d-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6879d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6879d-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6879d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6879d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6879d-131">CommonParameters</span></span>
<span data-ttu-id="6879d-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6879d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6879d-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6879d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6879d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6879d-134">INPUTS</span></span>

### <span data-ttu-id="6879d-135">System.object</span><span class="sxs-lookup"><span data-stu-id="6879d-135">System.String</span></span>

### <span data-ttu-id="6879d-136">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6879d-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>
<span data-ttu-id="6879d-137">參數：影像 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6879d-137">Parameters: Image (ByValue)</span></span>

## <span data-ttu-id="6879d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6879d-138">OUTPUTS</span></span>

### <span data-ttu-id="6879d-139">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="6879d-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="6879d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6879d-140">NOTES</span></span>

## <span data-ttu-id="6879d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6879d-141">RELATED LINKS</span></span>
