---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: c38be0f49e899379d93fc39a2531bcef219c3c29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794111"
---
# <span data-ttu-id="c7cc6-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="c7cc6-101">Select-AzContext</span></span>

## <span data-ttu-id="c7cc6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cc6-103">選取 Azure PowerShell Cmdlet 中的目標訂閱與帳戶</span><span class="sxs-lookup"><span data-stu-id="c7cc6-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="c7cc6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7cc6-104">SYNTAX</span></span>

### <span data-ttu-id="c7cc6-105">SelectByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c7cc6-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7cc6-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="c7cc6-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="c7cc6-107">說明</span><span class="sxs-lookup"><span data-stu-id="c7cc6-107">DESCRIPTION</span></span>
<span data-ttu-id="c7cc6-108">選取訂閱以針對 Azure PowerShell Cmdlet 中的 (或帳戶或租使用者) 。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="c7cc6-109">在這個 Cmdlet 之後，未來的 Cmdlet 會以所選的內容為目標。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="c7cc6-110">示例</span><span class="sxs-lookup"><span data-stu-id="c7cc6-110">EXAMPLES</span></span>

### <span data-ttu-id="c7cc6-111">範例1：以命名的內容為目標</span><span class="sxs-lookup"><span data-stu-id="c7cc6-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="c7cc6-112">在「工作」內容的帳戶、租使用者和訂閱中，以未來的 Azure PowerShell Cmdlet 為目標。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="c7cc6-113">參數</span><span class="sxs-lookup"><span data-stu-id="c7cc6-113">PARAMETERS</span></span>

### <span data-ttu-id="c7cc6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cc6-114">-DefaultProfile</span></span>
<span data-ttu-id="c7cc6-115">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="c7cc6-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7cc6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7cc6-116">-InputObject</span></span>
<span data-ttu-id="c7cc6-117">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7cc6-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7cc6-118">-Name</span></span>
<span data-ttu-id="c7cc6-119">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="c7cc6-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7cc6-120">-範圍</span><span class="sxs-lookup"><span data-stu-id="c7cc6-120">-Scope</span></span>
<span data-ttu-id="c7cc6-121">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="c7cc6-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7cc6-122">-確認</span><span class="sxs-lookup"><span data-stu-id="c7cc6-122">-Confirm</span></span>
<span data-ttu-id="c7cc6-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7cc6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7cc6-124">-WhatIf</span></span>
<span data-ttu-id="c7cc6-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7cc6-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7cc6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cc6-127">CommonParameters</span></span>
<span data-ttu-id="c7cc6-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cc6-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cc6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="c7cc6-130">INPUTS</span></span>

### <span data-ttu-id="c7cc6-131">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c7cc6-132">輸出</span><span class="sxs-lookup"><span data-stu-id="c7cc6-132">OUTPUTS</span></span>

### <span data-ttu-id="c7cc6-133">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="c7cc6-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c7cc6-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c7cc6-134">NOTES</span></span>

## <span data-ttu-id="c7cc6-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7cc6-135">RELATED LINKS</span></span>
