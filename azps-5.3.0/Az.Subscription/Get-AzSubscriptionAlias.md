---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447944"
---
# <span data-ttu-id="16ce7-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="16ce7-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="16ce7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="16ce7-103">取得訂閱別名詳細資料</span><span class="sxs-lookup"><span data-stu-id="16ce7-103">Gets subscription alias details</span></span>

## <span data-ttu-id="16ce7-104">句法</span><span class="sxs-lookup"><span data-stu-id="16ce7-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ce7-105">說明</span><span class="sxs-lookup"><span data-stu-id="16ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="16ce7-106">**AzSubscriptionAlias** Cmdlet 會取得訂閱別名詳細資料。</span><span class="sxs-lookup"><span data-stu-id="16ce7-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="16ce7-107">示例</span><span class="sxs-lookup"><span data-stu-id="16ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="16ce7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="16ce7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="16ce7-109">取得訂閱別名詳細資料</span><span class="sxs-lookup"><span data-stu-id="16ce7-109">Gets subscription alias details</span></span>

## <span data-ttu-id="16ce7-110">參數</span><span class="sxs-lookup"><span data-stu-id="16ce7-110">PARAMETERS</span></span>

### <span data-ttu-id="16ce7-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="16ce7-111">-AliasName</span></span>
<span data-ttu-id="16ce7-112">訂閱的別名</span><span class="sxs-lookup"><span data-stu-id="16ce7-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="16ce7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16ce7-113">-AsJob</span></span>
<span data-ttu-id="16ce7-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16ce7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16ce7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ce7-115">-DefaultProfile</span></span>
<span data-ttu-id="16ce7-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16ce7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ce7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="16ce7-117">-Confirm</span></span>
<span data-ttu-id="16ce7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16ce7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ce7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ce7-119">-WhatIf</span></span>
<span data-ttu-id="16ce7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16ce7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ce7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16ce7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ce7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ce7-122">CommonParameters</span></span>
<span data-ttu-id="16ce7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16ce7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ce7-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16ce7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ce7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="16ce7-125">INPUTS</span></span>

### <span data-ttu-id="16ce7-126">所有</span><span class="sxs-lookup"><span data-stu-id="16ce7-126">None</span></span>

## <span data-ttu-id="16ce7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="16ce7-127">OUTPUTS</span></span>

### <span data-ttu-id="16ce7-128">PSAzureSubscription 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="16ce7-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="16ce7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="16ce7-129">NOTES</span></span>

## <span data-ttu-id="16ce7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="16ce7-130">RELATED LINKS</span></span>
