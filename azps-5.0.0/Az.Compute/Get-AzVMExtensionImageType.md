---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 45F35BDD-969E-4521-9E8D-3499A15434A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimagetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImageType.md
ms.openlocfilehash: eb2c92b0efcbcd5333c600fe481e21752a96be9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287543"
---
# <span data-ttu-id="d220c-101">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="d220c-101">Get-AzVMExtensionImageType</span></span>

## <span data-ttu-id="d220c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d220c-102">SYNOPSIS</span></span>
<span data-ttu-id="d220c-103">取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="d220c-103">Gets the type of an Azure extension.</span></span>

## <span data-ttu-id="d220c-104">句法</span><span class="sxs-lookup"><span data-stu-id="d220c-104">SYNTAX</span></span>

```
Get-AzVMExtensionImageType -Location <String> -PublisherName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d220c-105">說明</span><span class="sxs-lookup"><span data-stu-id="d220c-105">DESCRIPTION</span></span>
<span data-ttu-id="d220c-106">**AzVMExtensionImageType** Cmdlet 會取得 Azure 延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="d220c-106">The **Get-AzVMExtensionImageType** cmdlet gets the type of an Azure extension.</span></span>

## <span data-ttu-id="d220c-107">示例</span><span class="sxs-lookup"><span data-stu-id="d220c-107">EXAMPLES</span></span>

### <span data-ttu-id="d220c-108">範例1：取得延伸圖像類型</span><span class="sxs-lookup"><span data-stu-id="d220c-108">Example 1: Get an extension image type</span></span>
```
PS C:\> Get-AzVMExtensionImageType -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="d220c-109">這個命令會取得指定發行者和位置的副檔名影像類型。</span><span class="sxs-lookup"><span data-stu-id="d220c-109">This command gets the extension image type for the specified publisher and location.</span></span>

## <span data-ttu-id="d220c-110">參數</span><span class="sxs-lookup"><span data-stu-id="d220c-110">PARAMETERS</span></span>

### <span data-ttu-id="d220c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d220c-111">-DefaultProfile</span></span>
<span data-ttu-id="d220c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d220c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d220c-113">-位置</span><span class="sxs-lookup"><span data-stu-id="d220c-113">-Location</span></span>
<span data-ttu-id="d220c-114">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="d220c-114">Specifies the location of an extension.</span></span>
<span data-ttu-id="d220c-115">這個 Cmdlet 會取得此參數指定位置的延伸類型。</span><span class="sxs-lookup"><span data-stu-id="d220c-115">This cmdlet gets the type for an extension at the location that this parameter specifies.</span></span>

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

### <span data-ttu-id="d220c-116">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="d220c-116">-PublisherName</span></span>
<span data-ttu-id="d220c-117">指定副檔名發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="d220c-117">Specifies the name of a publisher of an extension.</span></span>
<span data-ttu-id="d220c-118">若要取得延伸發行者，請使用 Get-AzVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d220c-118">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>
<span data-ttu-id="d220c-119">這個 Cmdlet 會從發行者取得此參數指定之延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="d220c-119">This cmdlet gets the type for an extension from the publisher that this parameter specifies.</span></span>

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

### <span data-ttu-id="d220c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d220c-120">CommonParameters</span></span>
<span data-ttu-id="d220c-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d220c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d220c-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d220c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d220c-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d220c-123">INPUTS</span></span>

### <span data-ttu-id="d220c-124">System.object</span><span class="sxs-lookup"><span data-stu-id="d220c-124">System.String</span></span>

## <span data-ttu-id="d220c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="d220c-125">OUTPUTS</span></span>

### <span data-ttu-id="d220c-126">PSVirtualMachineExtensionImageType 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d220c-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageType</span></span>

## <span data-ttu-id="d220c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d220c-127">NOTES</span></span>

## <span data-ttu-id="d220c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="d220c-128">RELATED LINKS</span></span>

[<span data-ttu-id="d220c-129">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d220c-129">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="d220c-130">AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d220c-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


