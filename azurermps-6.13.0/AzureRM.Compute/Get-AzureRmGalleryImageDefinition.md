---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447441"
---
# <span data-ttu-id="b1d1a-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b1d1a-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="b1d1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d1a-103">[取得] 或 [清單] 圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1d1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1d1a-104">SYNTAX</span></span>

### <span data-ttu-id="b1d1a-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b1d1a-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1d1a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b1d1a-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1d1a-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1d1a-107">DESCRIPTION</span></span>
<span data-ttu-id="b1d1a-108">[取得] 或 [清單] 圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="b1d1a-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1d1a-109">EXAMPLES</span></span>

### <span data-ttu-id="b1d1a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b1d1a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="b1d1a-111">取得圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="b1d1a-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1d1a-112">PARAMETERS</span></span>

### <span data-ttu-id="b1d1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d1a-113">-DefaultProfile</span></span>
<span data-ttu-id="b1d1a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1d1a-115">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b1d1a-115">-GalleryName</span></span>
<span data-ttu-id="b1d1a-116">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d1a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1d1a-117">-Name</span></span>
<span data-ttu-id="b1d1a-118">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b1d1a-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d1a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1d1a-121">-ResourceId</span></span>
<span data-ttu-id="b1d1a-122">畫廊影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b1d1a-122">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1d1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d1a-123">CommonParameters</span></span>
<span data-ttu-id="b1d1a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d1a-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d1a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b1d1a-126">INPUTS</span></span>

### <span data-ttu-id="b1d1a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b1d1a-127">System.String</span></span>

## <span data-ttu-id="b1d1a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b1d1a-128">OUTPUTS</span></span>

### <span data-ttu-id="b1d1a-129">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b1d1a-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="b1d1a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b1d1a-130">NOTES</span></span>

## <span data-ttu-id="b1d1a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1d1a-131">RELATED LINKS</span></span>
