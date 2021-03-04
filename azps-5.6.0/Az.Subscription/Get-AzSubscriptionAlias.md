---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: 0cce48f38b669c713f0d3a193deec64cfce649e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911246"
---
# <span data-ttu-id="278b1-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="278b1-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="278b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="278b1-102">SYNOPSIS</span></span>
<span data-ttu-id="278b1-103">獲得訂閱別名詳細資料</span><span class="sxs-lookup"><span data-stu-id="278b1-103">Gets subscription alias details</span></span>

## <span data-ttu-id="278b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="278b1-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="278b1-105">描述</span><span class="sxs-lookup"><span data-stu-id="278b1-105">DESCRIPTION</span></span>
<span data-ttu-id="278b1-106">**Get-AzSubscriptionAlias** Cmdlet 會取得訂閱別名詳細資料。</span><span class="sxs-lookup"><span data-stu-id="278b1-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="278b1-107">例子</span><span class="sxs-lookup"><span data-stu-id="278b1-107">EXAMPLES</span></span>

### <span data-ttu-id="278b1-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="278b1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="278b1-109">獲得訂閱別名詳細資料</span><span class="sxs-lookup"><span data-stu-id="278b1-109">Gets subscription alias details</span></span>

## <span data-ttu-id="278b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="278b1-110">PARAMETERS</span></span>

### <span data-ttu-id="278b1-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="278b1-111">-AliasName</span></span>
<span data-ttu-id="278b1-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="278b1-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="278b1-113">-AsJob</span></span>
<span data-ttu-id="278b1-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="278b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="278b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278b1-115">-DefaultProfile</span></span>
<span data-ttu-id="278b1-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="278b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="278b1-117">-確認</span><span class="sxs-lookup"><span data-stu-id="278b1-117">-Confirm</span></span>
<span data-ttu-id="278b1-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="278b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278b1-119">-WhatIf</span></span>
<span data-ttu-id="278b1-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="278b1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="278b1-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="278b1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="278b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278b1-122">CommonParameters</span></span>
<span data-ttu-id="278b1-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="278b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278b1-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="278b1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278b1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="278b1-125">INPUTS</span></span>

### <span data-ttu-id="278b1-126">沒有</span><span class="sxs-lookup"><span data-stu-id="278b1-126">None</span></span>

## <span data-ttu-id="278b1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="278b1-127">OUTPUTS</span></span>

### <span data-ttu-id="278b1-128">Microsoft.Azure.Commands.subscription.models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="278b1-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="278b1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="278b1-129">NOTES</span></span>

## <span data-ttu-id="278b1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="278b1-130">RELATED LINKS</span></span>
