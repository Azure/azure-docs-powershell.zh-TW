---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447816"
---
# <span data-ttu-id="aa0f4-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="aa0f4-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="aa0f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0f4-103">Azure 內容是代表您的作用中訂閱執行命令的 PowerShell 物件，以及連線至 Azure 雲端所需的驗證資訊。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="aa0f4-104">如果是 Azure 內容，則在您每次切換訂閱時，Azure PowerShell 不需要重新驗證您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="aa0f4-105">如需詳細資訊，請參閱 [Azure PowerShell 內容物件](https://docs.microsoft.com/powershell/azure/context-persistence)。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="aa0f4-106">這個 Cmdlet 可讓 Azure 內容資訊在您啟動 PowerShell 進程時儲存並自動載入。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="aa0f4-107">例如，開啟新視窗時。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="aa0f4-108">句法</span><span class="sxs-lookup"><span data-stu-id="aa0f4-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa0f4-109">說明</span><span class="sxs-lookup"><span data-stu-id="aa0f4-109">DESCRIPTION</span></span>

<span data-ttu-id="aa0f4-110">允許在 PowerShell 程式啟動時，儲存 Azure 內容資訊並自動載入。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="aa0f4-111">內容會在執行任何影響內容的 Cmdlet 結束時儲存。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="aa0f4-112">例如，任何設定檔 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="aa0f4-113">如果您使用的是使用者驗證，則可以在執行任何 Cmdlet 期間更新權杖。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="aa0f4-114">示例</span><span class="sxs-lookup"><span data-stu-id="aa0f4-114">EXAMPLES</span></span>

### <span data-ttu-id="aa0f4-115">範例1：為目前的使用者啟用 autosaving 認證</span><span class="sxs-lookup"><span data-stu-id="aa0f4-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="aa0f4-116">針對目前的使用者開啟認證自動儲存。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="aa0f4-117">每當開啟 PowerShell 視窗時，就會記住您目前的內容，而不需要登入。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="aa0f4-118">範例2</span><span class="sxs-lookup"><span data-stu-id="aa0f4-118">Example 2</span></span>

<span data-ttu-id="aa0f4-119">當您在這個 PowerShell 會話中開啟 PowerShell 視窗時，允許儲存及自動載入 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="aa0f4-120"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="aa0f4-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="aa0f4-121">參數</span><span class="sxs-lookup"><span data-stu-id="aa0f4-121">PARAMETERS</span></span>

### <span data-ttu-id="aa0f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0f4-122">-DefaultProfile</span></span>

<span data-ttu-id="aa0f4-123">用於與 Azure 進行通訊的認證、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aa0f4-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="aa0f4-124">-範圍</span><span class="sxs-lookup"><span data-stu-id="aa0f4-124">-Scope</span></span>

<span data-ttu-id="aa0f4-125">決定內容變更的範圍。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-125">Determines the scope of context changes.</span></span> <span data-ttu-id="aa0f4-126">例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="aa0f4-127">對範圍所做的變更 `CurrentUser` 會影響使用者開始的所有 PowerShell 會話。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="aa0f4-128">如果特定會話需要有不同的設定，請使用範圍 `Process` 。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa0f4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="aa0f4-129">-Confirm</span></span>

<span data-ttu-id="aa0f4-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa0f4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa0f4-131">-WhatIf</span></span>

<span data-ttu-id="aa0f4-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa0f4-133">無法執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="aa0f4-134">一般參數</span><span class="sxs-lookup"><span data-stu-id="aa0f4-134">Common Parameters</span></span>

<span data-ttu-id="aa0f4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0f4-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0f4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="aa0f4-137">INPUTS</span></span>

### <span data-ttu-id="aa0f4-138">所有</span><span class="sxs-lookup"><span data-stu-id="aa0f4-138">None</span></span>

## <span data-ttu-id="aa0f4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="aa0f4-139">OUTPUTS</span></span>

### <span data-ttu-id="aa0f4-140">CoNtextAutosaveSettings 的常見驗證。</span><span class="sxs-lookup"><span data-stu-id="aa0f4-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="aa0f4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="aa0f4-141">NOTES</span></span>

## <span data-ttu-id="aa0f4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa0f4-142">RELATED LINKS</span></span>
