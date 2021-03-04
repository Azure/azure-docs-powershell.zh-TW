---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: bc1ec66846037a7081af85809f2187b5d35aecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916780"
---
# <span data-ttu-id="2e057-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="2e057-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="2e057-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2e057-102">SYNOPSIS</span></span>
<span data-ttu-id="2e057-103">發佈新版本的藍圖。</span><span class="sxs-lookup"><span data-stu-id="2e057-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="2e057-104">語法</span><span class="sxs-lookup"><span data-stu-id="2e057-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e057-105">描述</span><span class="sxs-lookup"><span data-stu-id="2e057-105">DESCRIPTION</span></span>
<span data-ttu-id="2e057-106">發佈新版本的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="2e057-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="2e057-107">例子</span><span class="sxs-lookup"><span data-stu-id="2e057-107">EXAMPLES</span></span>

### <span data-ttu-id="2e057-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2e057-108">Example 1</span></span>
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

<span data-ttu-id="2e057-109">發佈新版本的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="2e057-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="2e057-110">參數</span><span class="sxs-lookup"><span data-stu-id="2e057-110">PARAMETERS</span></span>

### <span data-ttu-id="2e057-111">-藍圖</span><span class="sxs-lookup"><span data-stu-id="2e057-111">-Blueprint</span></span>
<span data-ttu-id="2e057-112">藍圖物件。</span><span class="sxs-lookup"><span data-stu-id="2e057-112">Blueprint object.</span></span>

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

### <span data-ttu-id="2e057-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="2e057-113">-ChangeNote</span></span>
<span data-ttu-id="2e057-114">說明此藍圖版本內容的附注。</span><span class="sxs-lookup"><span data-stu-id="2e057-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="2e057-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e057-115">-DefaultProfile</span></span>
<span data-ttu-id="2e057-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e057-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e057-117">-版本</span><span class="sxs-lookup"><span data-stu-id="2e057-117">-Version</span></span>
<span data-ttu-id="2e057-118">藍圖定義的版本。</span><span class="sxs-lookup"><span data-stu-id="2e057-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="2e057-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2e057-119">-Confirm</span></span>
<span data-ttu-id="2e057-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2e057-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e057-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e057-121">-WhatIf</span></span>
<span data-ttu-id="2e057-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2e057-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e057-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2e057-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e057-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e057-124">CommonParameters</span></span>
<span data-ttu-id="2e057-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2e057-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e057-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e057-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e057-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2e057-127">INPUTS</span></span>

### <span data-ttu-id="2e057-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2e057-128">System.String</span></span>

### <span data-ttu-id="2e057-129">Microsoft.Azure.Commands.藍圖.models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="2e057-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="2e057-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2e057-130">OUTPUTS</span></span>

### <span data-ttu-id="2e057-131">Microsoft.Azure.Commands.藍圖.models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="2e057-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="2e057-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2e057-132">NOTES</span></span>

## <span data-ttu-id="2e057-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e057-133">RELATED LINKS</span></span>
