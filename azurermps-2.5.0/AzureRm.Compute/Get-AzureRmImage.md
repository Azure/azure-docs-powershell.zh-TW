---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermimage
schema: 2.0.0
ms.openlocfilehash: 8508a7353924342449324588e90abf3807d7f7ac
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801057"
---
# <span data-ttu-id="1b334-101">Get-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="1b334-101">Get-AzureRmImage</span></span>

## <span data-ttu-id="1b334-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b334-102">SYNOPSIS</span></span>
<span data-ttu-id="1b334-103">取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b334-103">Gets the properties of an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b334-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b334-104">SYNTAX</span></span>

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b334-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b334-105">DESCRIPTION</span></span>
<span data-ttu-id="1b334-106">**AzureRmImage** Cmdlet 會取得影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b334-106">The **Get-AzureRmImage** cmdlet gets the properties of an image.</span></span>

## <span data-ttu-id="1b334-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b334-107">EXAMPLES</span></span>

### <span data-ttu-id="1b334-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1b334-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

<span data-ttu-id="1b334-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Image01 ' 的影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b334-109">This command gets the properties of the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1b334-110">範例2</span><span class="sxs-lookup"><span data-stu-id="1b334-110">Example 2</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="1b334-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b334-111">This command gets the properties of all images in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1b334-112">範例3</span><span class="sxs-lookup"><span data-stu-id="1b334-112">Example 3</span></span>
```
PS C:\> Get-AzureRmImage
```

<span data-ttu-id="1b334-113">這個命令會取得訂閱下所有影像的屬性。</span><span class="sxs-lookup"><span data-stu-id="1b334-113">This command gets the properties of all images under the subscription.</span></span>

## <span data-ttu-id="1b334-114">參數</span><span class="sxs-lookup"><span data-stu-id="1b334-114">PARAMETERS</span></span>

### <span data-ttu-id="1b334-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b334-115">-DefaultProfile</span></span>
<span data-ttu-id="1b334-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b334-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b334-117">-展開</span><span class="sxs-lookup"><span data-stu-id="1b334-117">-Expand</span></span>
<span data-ttu-id="1b334-118">指定 [擴大運算式] 查詢。</span><span class="sxs-lookup"><span data-stu-id="1b334-118">Specifies the expand expression query.</span></span>

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

### <span data-ttu-id="1b334-119">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1b334-119">-ImageName</span></span>
<span data-ttu-id="1b334-120">指定影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b334-120">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="1b334-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b334-121">-ResourceGroupName</span></span>
<span data-ttu-id="1b334-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1b334-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1b334-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b334-123">CommonParameters</span></span>
<span data-ttu-id="1b334-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b334-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b334-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b334-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b334-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1b334-126">INPUTS</span></span>

### <span data-ttu-id="1b334-127">System.object</span><span class="sxs-lookup"><span data-stu-id="1b334-127">System.String</span></span>

## <span data-ttu-id="1b334-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1b334-128">OUTPUTS</span></span>

### <span data-ttu-id="1b334-129">PSImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1b334-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1b334-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1b334-130">NOTES</span></span>

## <span data-ttu-id="1b334-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b334-131">RELATED LINKS</span></span>

