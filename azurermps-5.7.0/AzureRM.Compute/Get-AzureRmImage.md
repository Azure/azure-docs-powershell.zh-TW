---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449946"
---
# <span data-ttu-id="18b89-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="18b89-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="18b89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18b89-102">SYNOPSIS</span></span>
<span data-ttu-id="18b89-103">取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b89-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b89-104">句法</span><span class="sxs-lookup"><span data-stu-id="18b89-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="18b89-105">說明</span><span class="sxs-lookup"><span data-stu-id="18b89-105">DESCRIPTION</span></span>
<span data-ttu-id="18b89-106">**AzureRmImage** Cmdlet 會取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b89-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="18b89-107">示例</span><span class="sxs-lookup"><span data-stu-id="18b89-107">EXAMPLES</span></span>

### <span data-ttu-id="18b89-108">範例1</span><span class="sxs-lookup"><span data-stu-id="18b89-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="18b89-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Image01 ' 的影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b89-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="18b89-110">範例2</span><span class="sxs-lookup"><span data-stu-id="18b89-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="18b89-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b89-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="18b89-112">範例3</span><span class="sxs-lookup"><span data-stu-id="18b89-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="18b89-113">這個命令會取得訂閱下所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="18b89-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="18b89-114">參數</span><span class="sxs-lookup"><span data-stu-id="18b89-114">PARAMETERS</span></span>

### <span data-ttu-id="18b89-115">-展開</span><span class="sxs-lookup"><span data-stu-id="18b89-115">-Expand</span></span>
<span data-ttu-id="18b89-116">指定 [擴大運算式] 查詢。</span><span class="sxs-lookup"><span data-stu-id="18b89-116">Specifies the expand expression query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b89-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="18b89-117">-ImageName</span></span>
<span data-ttu-id="18b89-118">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="18b89-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b89-119">-ResourceGroupName</span></span>
<span data-ttu-id="18b89-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="18b89-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b89-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b89-121">CommonParameters</span></span>
<span data-ttu-id="18b89-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18b89-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b89-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18b89-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b89-124">輸入</span><span class="sxs-lookup"><span data-stu-id="18b89-124">INPUTS</span></span>

### <span data-ttu-id="18b89-125">System.object</span><span class="sxs-lookup"><span data-stu-id="18b89-125">System.String</span></span>

## <span data-ttu-id="18b89-126">輸出</span><span class="sxs-lookup"><span data-stu-id="18b89-126">OUTPUTS</span></span>

### <span data-ttu-id="18b89-127">System.object</span><span class="sxs-lookup"><span data-stu-id="18b89-127">System.Object</span></span>

## <span data-ttu-id="18b89-128">筆記</span><span class="sxs-lookup"><span data-stu-id="18b89-128">NOTES</span></span>

## <span data-ttu-id="18b89-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="18b89-129">RELATED LINKS</span></span>

