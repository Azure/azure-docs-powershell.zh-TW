---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284459"
---
# <span data-ttu-id="87d3f-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="87d3f-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="87d3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="87d3f-103">取得訂閱別名詳細資料</span><span class="sxs-lookup"><span data-stu-id="87d3f-103">Gets subscription alias details</span></span>

## <span data-ttu-id="87d3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="87d3f-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="87d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="87d3f-106">**AzSubscriptionAlias** Cmdlet 會取得訂閱別名詳細資料。</span><span class="sxs-lookup"><span data-stu-id="87d3f-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="87d3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="87d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="87d3f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="87d3f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="87d3f-109">取得訂閱別名詳細資料</span><span class="sxs-lookup"><span data-stu-id="87d3f-109">Gets subscription alias details</span></span>

## <span data-ttu-id="87d3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="87d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="87d3f-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="87d3f-111">-AliasName</span></span>
<span data-ttu-id="87d3f-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="87d3f-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="87d3f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87d3f-113">-AsJob</span></span>
<span data-ttu-id="87d3f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="87d3f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87d3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d3f-115">-DefaultProfile</span></span>
<span data-ttu-id="87d3f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87d3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87d3f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="87d3f-117">-Confirm</span></span>
<span data-ttu-id="87d3f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87d3f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d3f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d3f-119">-WhatIf</span></span>
<span data-ttu-id="87d3f-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87d3f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d3f-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87d3f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d3f-122">CommonParameters</span></span>
<span data-ttu-id="87d3f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87d3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d3f-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="87d3f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d3f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="87d3f-125">INPUTS</span></span>

### <span data-ttu-id="87d3f-126">所有</span><span class="sxs-lookup"><span data-stu-id="87d3f-126">None</span></span>

## <span data-ttu-id="87d3f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="87d3f-127">OUTPUTS</span></span>

### <span data-ttu-id="87d3f-128">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87d3f-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="87d3f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="87d3f-129">NOTES</span></span>

## <span data-ttu-id="87d3f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="87d3f-130">RELATED LINKS</span></span>
