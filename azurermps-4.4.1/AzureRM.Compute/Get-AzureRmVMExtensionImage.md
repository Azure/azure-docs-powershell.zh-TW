---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtensionImage.md
ms.openlocfilehash: 7010808e1879566d3b0fc78f82d0e9f82bdd626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624845"
---
# <span data-ttu-id="9bdb9-101">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="9bdb9-101">Get-AzureRmVMExtensionImage</span></span>

## <span data-ttu-id="9bdb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9bdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdb9-103">取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-103">Gets all versions for an Azure extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bdb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="9bdb9-104">SYNTAX</span></span>

```
Get-AzureRmVMExtensionImage -Location <String> -PublisherName <String> -Type <String>
 [-FilterExpression <String>] [-Version <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bdb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="9bdb9-105">DESCRIPTION</span></span>
<span data-ttu-id="9bdb9-106">**AzureRmVMExtensionImage** Cmdlet 會取得 Azure 延伸的所有版本。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-106">The **Get-AzureRmVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="9bdb9-107">示例</span><span class="sxs-lookup"><span data-stu-id="9bdb9-107">EXAMPLES</span></span>

### <span data-ttu-id="9bdb9-108">範例1：取得副檔名影像的版本</span><span class="sxs-lookup"><span data-stu-id="9bdb9-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzureRmVMExtensionImage -Location "Central US" -PublisherName "Fabrikam" -Type "FabrikamEndpointProtection"
```

<span data-ttu-id="9bdb9-109">這個命令會取得指定位置、發行者及類型的所有副檔名影像版本。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

## <span data-ttu-id="9bdb9-110">參數</span><span class="sxs-lookup"><span data-stu-id="9bdb9-110">PARAMETERS</span></span>

### <span data-ttu-id="9bdb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdb9-111">-DefaultProfile</span></span>
<span data-ttu-id="9bdb9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bdb9-113">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9bdb9-113">-FilterExpression</span></span>
<span data-ttu-id="9bdb9-114">指定篩選運算式。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-114">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bdb9-115">-位置</span><span class="sxs-lookup"><span data-stu-id="9bdb9-115">-Location</span></span>
<span data-ttu-id="9bdb9-116">指定延伸的位置。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-116">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="9bdb9-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9bdb9-117">-PublisherName</span></span>
<span data-ttu-id="9bdb9-118">指定延伸發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-118">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="9bdb9-119">若要取得延伸發行者，請使用 Get-AzureRmVMImagePublisher Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-119">To obtain an extension publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9bdb9-120">-類型</span><span class="sxs-lookup"><span data-stu-id="9bdb9-120">-Type</span></span>
<span data-ttu-id="9bdb9-121">指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-121">Specifies the type of the extension.</span></span>
<span data-ttu-id="9bdb9-122">若要取得延伸類型，請使用 Get-AzureRmVMExtensionImageType Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-122">To obtain an extension type, use the Get-AzureRmVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="9bdb9-123">-版本</span><span class="sxs-lookup"><span data-stu-id="9bdb9-123">-Version</span></span>
<span data-ttu-id="9bdb9-124">指定此 Cmdlet 取得的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-124">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9bdb9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdb9-125">CommonParameters</span></span>
<span data-ttu-id="9bdb9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdb9-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9bdb9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdb9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9bdb9-128">INPUTS</span></span>

## <span data-ttu-id="9bdb9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9bdb9-129">OUTPUTS</span></span>

## <span data-ttu-id="9bdb9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9bdb9-130">NOTES</span></span>

## <span data-ttu-id="9bdb9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9bdb9-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bdb9-132">AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="9bdb9-132">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="9bdb9-133">AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="9bdb9-133">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="9bdb9-134">AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9bdb9-134">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)


