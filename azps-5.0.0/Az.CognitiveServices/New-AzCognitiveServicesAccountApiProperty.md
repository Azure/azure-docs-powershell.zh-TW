---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285628"
---
# <span data-ttu-id="10869-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="10869-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="10869-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10869-102">SYNOPSIS</span></span>
<span data-ttu-id="10869-103">產生認知服務帳戶 ApiProperties 的新實例</span><span class="sxs-lookup"><span data-stu-id="10869-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="10869-104">句法</span><span class="sxs-lookup"><span data-stu-id="10869-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10869-105">說明</span><span class="sxs-lookup"><span data-stu-id="10869-105">DESCRIPTION</span></span>
<span data-ttu-id="10869-106">產生新的認知服務帳戶 ApiProperties 實例。</span><span class="sxs-lookup"><span data-stu-id="10869-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="10869-107">在建立新的帳戶或更新現有的帳戶時，可以使用 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="10869-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="10869-108">某些帳戶類型需要 ApiProperties。</span><span class="sxs-lookup"><span data-stu-id="10869-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="10869-109">示例</span><span class="sxs-lookup"><span data-stu-id="10869-109">EXAMPLES</span></span>

### <span data-ttu-id="10869-110">範例1</span><span class="sxs-lookup"><span data-stu-id="10869-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="10869-111">上述範例會建立 API 屬性為 "QnaRuntimeEndpoint" 的 QnAMaker 帳戶。</span><span class="sxs-lookup"><span data-stu-id="10869-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="10869-112">參數</span><span class="sxs-lookup"><span data-stu-id="10869-112">PARAMETERS</span></span>

### <span data-ttu-id="10869-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10869-113">-DefaultProfile</span></span>
<span data-ttu-id="10869-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10869-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10869-115">-確認</span><span class="sxs-lookup"><span data-stu-id="10869-115">-Confirm</span></span>
<span data-ttu-id="10869-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10869-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10869-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10869-117">-WhatIf</span></span>
<span data-ttu-id="10869-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10869-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10869-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10869-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10869-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10869-120">CommonParameters</span></span>
<span data-ttu-id="10869-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10869-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10869-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="10869-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10869-123">輸入</span><span class="sxs-lookup"><span data-stu-id="10869-123">INPUTS</span></span>

### <span data-ttu-id="10869-124">所有</span><span class="sxs-lookup"><span data-stu-id="10869-124">None</span></span>

## <span data-ttu-id="10869-125">輸出</span><span class="sxs-lookup"><span data-stu-id="10869-125">OUTPUTS</span></span>

### <span data-ttu-id="10869-126">CognitiveServicesAccountApiProperties 中的 CognitiveServices。</span><span class="sxs-lookup"><span data-stu-id="10869-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="10869-127">筆記</span><span class="sxs-lookup"><span data-stu-id="10869-127">NOTES</span></span>

## <span data-ttu-id="10869-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="10869-128">RELATED LINKS</span></span>
