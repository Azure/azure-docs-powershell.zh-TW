---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130447"
---
# <span data-ttu-id="a20ec-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="a20ec-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="a20ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a20ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a20ec-103">刪除訂閱別名</span><span class="sxs-lookup"><span data-stu-id="a20ec-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="a20ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="a20ec-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a20ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="a20ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a20ec-106">**AzSubscriptionAlias** Cmdlet 會移除訂閱別名</span><span class="sxs-lookup"><span data-stu-id="a20ec-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="a20ec-107">示例</span><span class="sxs-lookup"><span data-stu-id="a20ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a20ec-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a20ec-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="a20ec-109">刪除訂閱別名</span><span class="sxs-lookup"><span data-stu-id="a20ec-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="a20ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="a20ec-110">PARAMETERS</span></span>

### <span data-ttu-id="a20ec-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="a20ec-111">-AliasName</span></span>
<span data-ttu-id="a20ec-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="a20ec-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="a20ec-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a20ec-113">-AsJob</span></span>
<span data-ttu-id="a20ec-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a20ec-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a20ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20ec-115">-DefaultProfile</span></span>
<span data-ttu-id="a20ec-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a20ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a20ec-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a20ec-117">-Confirm</span></span>
<span data-ttu-id="a20ec-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a20ec-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a20ec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a20ec-119">-WhatIf</span></span>
<span data-ttu-id="a20ec-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a20ec-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a20ec-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a20ec-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a20ec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20ec-122">CommonParameters</span></span>
<span data-ttu-id="a20ec-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a20ec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20ec-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a20ec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20ec-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a20ec-125">INPUTS</span></span>

### <span data-ttu-id="a20ec-126">所有</span><span class="sxs-lookup"><span data-stu-id="a20ec-126">None</span></span>

## <span data-ttu-id="a20ec-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a20ec-127">OUTPUTS</span></span>

### <span data-ttu-id="a20ec-128">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a20ec-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a20ec-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a20ec-129">NOTES</span></span>

## <span data-ttu-id="a20ec-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a20ec-130">RELATED LINKS</span></span>
