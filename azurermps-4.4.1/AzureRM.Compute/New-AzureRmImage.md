---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 02255fd8fd4db5747c820755bfd46ee3251aab9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445095"
---
# <span data-ttu-id="4617b-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="4617b-101">New-AzureRmImage</span></span>

## <span data-ttu-id="4617b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4617b-102">SYNOPSIS</span></span>
<span data-ttu-id="4617b-103">建立影像。</span><span class="sxs-lookup"><span data-stu-id="4617b-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4617b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4617b-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4617b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4617b-105">DESCRIPTION</span></span>
<span data-ttu-id="4617b-106">**新的-AzureRmImage** Cmdlet 會建立影像。</span><span class="sxs-lookup"><span data-stu-id="4617b-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="4617b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4617b-107">EXAMPLES</span></span>

### <span data-ttu-id="4617b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4617b-108">Example 1</span></span>
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

<span data-ttu-id="4617b-109">第一個命令會建立 image 物件，然後將它儲存在 $imageConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="4617b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="4617b-110">接下來的三個命令會將 os 磁片和兩個數據磁片的路徑指派給 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2 個變數。</span><span class="sxs-lookup"><span data-stu-id="4617b-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="4617b-111">這個方法只是為了讓您瞭解下列命令的可讀性。</span><span class="sxs-lookup"><span data-stu-id="4617b-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="4617b-112">接下來的三個命令會將 os 磁片和兩個數據磁片新增至儲存在 $imageConfig 的影像中。</span><span class="sxs-lookup"><span data-stu-id="4617b-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="4617b-113">每個磁片的 URI 都儲存在 $osDiskVhdUri、$dataDiskVhdUri 1 及 $dataDiskVhdUri 2。</span><span class="sxs-lookup"><span data-stu-id="4617b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="4617b-114">最後一個命令會在資源群組 "ResourceGroup01" 中建立名為 "ImageName01" 的影像。</span><span class="sxs-lookup"><span data-stu-id="4617b-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4617b-115">參數</span><span class="sxs-lookup"><span data-stu-id="4617b-115">PARAMETERS</span></span>

### <span data-ttu-id="4617b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4617b-116">-DefaultProfile</span></span>
<span data-ttu-id="4617b-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4617b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4617b-118">-影像</span><span class="sxs-lookup"><span data-stu-id="4617b-118">-Image</span></span>
<span data-ttu-id="4617b-119">指定本機影像物件。</span><span class="sxs-lookup"><span data-stu-id="4617b-119">Specifies a local image object.</span></span>

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

### <span data-ttu-id="4617b-120">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4617b-120">-ImageName</span></span>
<span data-ttu-id="4617b-121">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="4617b-121">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="4617b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4617b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4617b-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4617b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4617b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="4617b-124">-Confirm</span></span>
<span data-ttu-id="4617b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4617b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4617b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4617b-126">-WhatIf</span></span>
<span data-ttu-id="4617b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4617b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4617b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4617b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4617b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4617b-129">CommonParameters</span></span>
<span data-ttu-id="4617b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4617b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4617b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4617b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4617b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4617b-132">INPUTS</span></span>

### <span data-ttu-id="4617b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="4617b-133">System.String</span></span>
<span data-ttu-id="4617b-134">[Azure. 管理]-[計算] 模型。</span><span class="sxs-lookup"><span data-stu-id="4617b-134">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="4617b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4617b-135">OUTPUTS</span></span>

### <span data-ttu-id="4617b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4617b-136">System.Object</span></span>

## <span data-ttu-id="4617b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4617b-137">NOTES</span></span>

## <span data-ttu-id="4617b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4617b-138">RELATED LINKS</span></span>

