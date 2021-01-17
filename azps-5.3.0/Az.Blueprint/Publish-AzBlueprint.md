---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449970"
---
# <span data-ttu-id="1fe39-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="1fe39-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="1fe39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fe39-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe39-103">發佈新版本的藍圖。</span><span class="sxs-lookup"><span data-stu-id="1fe39-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="1fe39-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fe39-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe39-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fe39-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe39-106">發佈新版本的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="1fe39-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="1fe39-107">示例</span><span class="sxs-lookup"><span data-stu-id="1fe39-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe39-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1fe39-108">Example 1</span></span>
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

<span data-ttu-id="1fe39-109">發佈新版本的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="1fe39-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="1fe39-110">參數</span><span class="sxs-lookup"><span data-stu-id="1fe39-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe39-111">-藍圖</span><span class="sxs-lookup"><span data-stu-id="1fe39-111">-Blueprint</span></span>
<span data-ttu-id="1fe39-112">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="1fe39-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe39-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="1fe39-113">-ChangeNote</span></span>
<span data-ttu-id="1fe39-114">描述此藍圖版本內容的記事。</span><span class="sxs-lookup"><span data-stu-id="1fe39-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="1fe39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe39-115">-DefaultProfile</span></span>
<span data-ttu-id="1fe39-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fe39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe39-117">-版本</span><span class="sxs-lookup"><span data-stu-id="1fe39-117">-Version</span></span>
<span data-ttu-id="1fe39-118">藍圖定義的版本。</span><span class="sxs-lookup"><span data-stu-id="1fe39-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="1fe39-119">-確認</span><span class="sxs-lookup"><span data-stu-id="1fe39-119">-Confirm</span></span>
<span data-ttu-id="1fe39-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1fe39-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe39-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe39-121">-WhatIf</span></span>
<span data-ttu-id="1fe39-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1fe39-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fe39-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1fe39-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe39-124">CommonParameters</span></span>
<span data-ttu-id="1fe39-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fe39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe39-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fe39-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe39-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1fe39-127">INPUTS</span></span>

### <span data-ttu-id="1fe39-128">System.object</span><span class="sxs-lookup"><span data-stu-id="1fe39-128">System.String</span></span>

### <span data-ttu-id="1fe39-129">PSBlueprint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1fe39-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="1fe39-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1fe39-130">OUTPUTS</span></span>

### <span data-ttu-id="1fe39-131">PSPublishedBlueprint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1fe39-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="1fe39-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1fe39-132">NOTES</span></span>

## <span data-ttu-id="1fe39-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fe39-133">RELATED LINKS</span></span>
