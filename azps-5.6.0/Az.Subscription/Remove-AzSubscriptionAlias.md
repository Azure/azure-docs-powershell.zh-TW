---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 2acca5ede1d6ef7e4a3767b87053fb356555993d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906834"
---
# <span data-ttu-id="69696-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="69696-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="69696-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69696-102">SYNOPSIS</span></span>
<span data-ttu-id="69696-103">刪除訂閱別名</span><span class="sxs-lookup"><span data-stu-id="69696-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="69696-104">語法</span><span class="sxs-lookup"><span data-stu-id="69696-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69696-105">描述</span><span class="sxs-lookup"><span data-stu-id="69696-105">DESCRIPTION</span></span>
<span data-ttu-id="69696-106">**Remove-AzSubscriptionAlias** Cmdlet 會移除訂閱別名</span><span class="sxs-lookup"><span data-stu-id="69696-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="69696-107">例子</span><span class="sxs-lookup"><span data-stu-id="69696-107">EXAMPLES</span></span>

### <span data-ttu-id="69696-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="69696-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="69696-109">刪除訂閱別名</span><span class="sxs-lookup"><span data-stu-id="69696-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="69696-110">參數</span><span class="sxs-lookup"><span data-stu-id="69696-110">PARAMETERS</span></span>

### <span data-ttu-id="69696-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="69696-111">-AliasName</span></span>
<span data-ttu-id="69696-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="69696-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69696-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69696-113">-AsJob</span></span>
<span data-ttu-id="69696-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="69696-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69696-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69696-115">-DefaultProfile</span></span>
<span data-ttu-id="69696-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69696-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69696-117">-確認</span><span class="sxs-lookup"><span data-stu-id="69696-117">-Confirm</span></span>
<span data-ttu-id="69696-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69696-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69696-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69696-119">-WhatIf</span></span>
<span data-ttu-id="69696-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69696-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69696-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69696-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69696-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69696-122">CommonParameters</span></span>
<span data-ttu-id="69696-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69696-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69696-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69696-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69696-125">輸入</span><span class="sxs-lookup"><span data-stu-id="69696-125">INPUTS</span></span>

### <span data-ttu-id="69696-126">沒有</span><span class="sxs-lookup"><span data-stu-id="69696-126">None</span></span>

## <span data-ttu-id="69696-127">輸出</span><span class="sxs-lookup"><span data-stu-id="69696-127">OUTPUTS</span></span>

### <span data-ttu-id="69696-128">Microsoft.Azure.Commands.subscription.models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="69696-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="69696-129">筆記</span><span class="sxs-lookup"><span data-stu-id="69696-129">NOTES</span></span>

## <span data-ttu-id="69696-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="69696-130">RELATED LINKS</span></span>
