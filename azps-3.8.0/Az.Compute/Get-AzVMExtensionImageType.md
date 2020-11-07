---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958828"
---
# <span data-ttu-id="6c943-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="6c943-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="6c943-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c943-102">SYNOPSIS</span></span>
<span data-ttu-id="6c943-103">取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="6c943-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="6c943-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c943-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c943-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c943-105">DESCRIPTION</span></span>
<span data-ttu-id="6c943-106">**AzVMExtensionImageType** Cmdlet 會取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="6c943-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="6c943-107">示例</span><span class="sxs-lookup"><span data-stu-id="6c943-107">EXAMPLES</span></span>

### <span data-ttu-id="6c943-108">範例1：取得延伸圖像類型</span><span class="sxs-lookup"><span data-stu-id="6c943-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="6c943-109">這個命令會取得指定發行者和位置的副檔名影像類型。</span><span class="sxs-lookup"><span data-stu-id="6c943-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="6c943-110">參數</span><span class="sxs-lookup"><span data-stu-id="6c943-110">PARAMETERS</span></span>

### <span data-ttu-id="6c943-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c943-111">-DefaultProfile</span></span>
<span data-ttu-id="6c943-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c943-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c943-113">-位置</span><span class="sxs-lookup"><span data-stu-id="6c943-113">-Location</span></span>
<span data-ttu-id="6c943-114">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="6c943-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="6c943-115">這個 Cmdlet 會取得此參數指定位置的延伸類型。</span><span class="sxs-lookup"><span data-stu-id="6c943-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c943-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="6c943-116">-PublisherName</span></span>
<span data-ttu-id="6c943-117">指定副檔名發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c943-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="6c943-118">若要取得延伸發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c943-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="6c943-119">這個 Cmdlet 會從發行者取得此參數指定之延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="6c943-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c943-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c943-120">CommonParameters</span></span>
<span data-ttu-id="6c943-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c943-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c943-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c943-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c943-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6c943-123">INPUTS</span></span>

### <span data-ttu-id="6c943-124">System.object</span><span class="sxs-lookup"><span data-stu-id="6c943-124">System.String</span></span>

## <span data-ttu-id="6c943-125">輸出</span><span class="sxs-lookup"><span data-stu-id="6c943-125">OUTPUTS</span></span>

### <span data-ttu-id="6c943-126">PSVirtualMachineExtensionImageType 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6c943-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="6c943-127">筆記</span><span class="sxs-lookup"><span data-stu-id="6c943-127">NOTES</span></span>

## <span data-ttu-id="6c943-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c943-128">RELATED LINKS</span></span>

[<span data-ttu-id="6c943-129">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6c943-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="6c943-130">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6c943-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


