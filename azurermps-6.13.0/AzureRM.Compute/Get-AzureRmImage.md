---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 761a80feb7cf60479fdaba12605be6d670428641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447438"
---
# <span data-ttu-id="9597b-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="9597b-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="9597b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9597b-102">SYNOPSIS</span></span>
<span data-ttu-id="9597b-103">取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="9597b-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9597b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9597b-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9597b-105">說明</span><span class="sxs-lookup"><span data-stu-id="9597b-105">DESCRIPTION</span></span>
<span data-ttu-id="9597b-106">**AzureRmImage** Cmdlet 會取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="9597b-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="9597b-107">示例</span><span class="sxs-lookup"><span data-stu-id="9597b-107">EXAMPLES</span></span>

### <span data-ttu-id="9597b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9597b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="9597b-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Image01 ' 的影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="9597b-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9597b-110">範例2</span><span class="sxs-lookup"><span data-stu-id="9597b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="9597b-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="9597b-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9597b-112">範例3</span><span class="sxs-lookup"><span data-stu-id="9597b-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="9597b-113">這個命令會取得訂閱下所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="9597b-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="9597b-114">參數</span><span class="sxs-lookup"><span data-stu-id="9597b-114">PARAMETERS</span></span>

### <span data-ttu-id="9597b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9597b-115">-DefaultProfile</span></span>
<span data-ttu-id="9597b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9597b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9597b-117">-展開</span><span class="sxs-lookup"><span data-stu-id="9597b-117">-Expand</span></span>
<span data-ttu-id="9597b-118">指定 [擴大運算式] 查詢。</span><span class="sxs-lookup"><span data-stu-id="9597b-118">Specifies the expand expression query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9597b-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="9597b-119">-ImageName</span></span>
<span data-ttu-id="9597b-120">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="9597b-120">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9597b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9597b-121">-ResourceGroupName</span></span>
<span data-ttu-id="9597b-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9597b-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9597b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9597b-123">CommonParameters</span></span>
<span data-ttu-id="9597b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9597b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9597b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9597b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9597b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9597b-126">INPUTS</span></span>

### <span data-ttu-id="9597b-127">System.object</span><span class="sxs-lookup"><span data-stu-id="9597b-127">System.String</span></span>

## <span data-ttu-id="9597b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9597b-128">OUTPUTS</span></span>

### <span data-ttu-id="9597b-129">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9597b-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="9597b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9597b-130">NOTES</span></span>

## <span data-ttu-id="9597b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9597b-131">RELATED LINKS</span></span>
