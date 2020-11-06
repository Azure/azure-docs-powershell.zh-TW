---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 5286b8953a9f28c5e63fe176f19d9d885e9c1d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613576"
---
# <span data-ttu-id="94d12-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="94d12-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="94d12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94d12-102">SYNOPSIS</span></span>
<span data-ttu-id="94d12-103">發佈新版本的藍圖。</span><span class="sxs-lookup"><span data-stu-id="94d12-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="94d12-104">句法</span><span class="sxs-lookup"><span data-stu-id="94d12-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94d12-105">說明</span><span class="sxs-lookup"><span data-stu-id="94d12-105">DESCRIPTION</span></span>
<span data-ttu-id="94d12-106">發佈新版本的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="94d12-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="94d12-107">示例</span><span class="sxs-lookup"><span data-stu-id="94d12-107">EXAMPLES</span></span>

### <span data-ttu-id="94d12-108">範例1</span><span class="sxs-lookup"><span data-stu-id="94d12-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="94d12-109">發佈新版本的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="94d12-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="94d12-110">參數</span><span class="sxs-lookup"><span data-stu-id="94d12-110">PARAMETERS</span></span>

### <span data-ttu-id="94d12-111">-藍圖</span><span class="sxs-lookup"><span data-stu-id="94d12-111">-Blueprint</span></span>
<span data-ttu-id="94d12-112">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="94d12-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94d12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d12-113">-DefaultProfile</span></span>
<span data-ttu-id="94d12-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94d12-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d12-115">-版本</span><span class="sxs-lookup"><span data-stu-id="94d12-115">-Version</span></span>
<span data-ttu-id="94d12-116">藍圖定義的版本。</span><span class="sxs-lookup"><span data-stu-id="94d12-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="94d12-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="94d12-117">-ChangeNote</span></span>
<span data-ttu-id="94d12-118">描述此藍圖版本內容的記事。</span><span class="sxs-lookup"><span data-stu-id="94d12-118">Notes to describe the contents of this blueprint version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d12-119">CommonParameters</span></span>
<span data-ttu-id="94d12-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94d12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="94d12-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94d12-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d12-122">輸入</span><span class="sxs-lookup"><span data-stu-id="94d12-122">INPUTS</span></span>

### <span data-ttu-id="94d12-123">System.object</span><span class="sxs-lookup"><span data-stu-id="94d12-123">System.String</span></span>

### <span data-ttu-id="94d12-124">PSBlueprint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94d12-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="94d12-125">輸出</span><span class="sxs-lookup"><span data-stu-id="94d12-125">OUTPUTS</span></span>

### <span data-ttu-id="94d12-126">PSPublishedBlueprint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94d12-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="94d12-127">筆記</span><span class="sxs-lookup"><span data-stu-id="94d12-127">NOTES</span></span>

## <span data-ttu-id="94d12-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="94d12-128">RELATED LINKS</span></span>
