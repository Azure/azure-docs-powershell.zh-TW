---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 50e62158d4b24282753c726845e7dd88d492843c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909221"
---
# <span data-ttu-id="2f32a-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="2f32a-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="2f32a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f32a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f32a-103">產生新認知服務帳戶 ApiProperties 實例</span><span class="sxs-lookup"><span data-stu-id="2f32a-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="2f32a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f32a-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f32a-105">描述</span><span class="sxs-lookup"><span data-stu-id="2f32a-105">DESCRIPTION</span></span>
<span data-ttu-id="2f32a-106">產生新認知服務帳戶 ApiProperties 實例。</span><span class="sxs-lookup"><span data-stu-id="2f32a-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="2f32a-107">建立新帳戶或更新現有帳戶時，可以使用 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="2f32a-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="2f32a-108">特定帳戶類型需要 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="2f32a-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="2f32a-109">例子</span><span class="sxs-lookup"><span data-stu-id="2f32a-109">EXAMPLES</span></span>

### <span data-ttu-id="2f32a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f32a-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="2f32a-111">上述範例會建立 QnAMaker 帳戶，其 API 屬性為 "QnaRuntimeEndpoint"。</span><span class="sxs-lookup"><span data-stu-id="2f32a-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="2f32a-112">參數</span><span class="sxs-lookup"><span data-stu-id="2f32a-112">PARAMETERS</span></span>

### <span data-ttu-id="2f32a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f32a-113">-DefaultProfile</span></span>
<span data-ttu-id="2f32a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f32a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f32a-115">-確認</span><span class="sxs-lookup"><span data-stu-id="2f32a-115">-Confirm</span></span>
<span data-ttu-id="2f32a-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f32a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f32a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f32a-117">-WhatIf</span></span>
<span data-ttu-id="2f32a-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f32a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f32a-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f32a-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f32a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f32a-120">CommonParameters</span></span>
<span data-ttu-id="2f32a-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f32a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f32a-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f32a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f32a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2f32a-123">INPUTS</span></span>

### <span data-ttu-id="2f32a-124">沒有</span><span class="sxs-lookup"><span data-stu-id="2f32a-124">None</span></span>

## <span data-ttu-id="2f32a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2f32a-125">OUTPUTS</span></span>

### <span data-ttu-id="2f32a-126">Microsoft.Azure.management.CognitiveServices.models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="2f32a-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="2f32a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2f32a-127">NOTES</span></span>

## <span data-ttu-id="2f32a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f32a-128">RELATED LINKS</span></span>
