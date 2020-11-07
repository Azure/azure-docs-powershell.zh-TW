---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: c5d01fcc7ba007a0336fac5c08db44b840e75806
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958972"
---
# <span data-ttu-id="978a3-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="978a3-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="978a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="978a3-102">SYNOPSIS</span></span>
<span data-ttu-id="978a3-103">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="978a3-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="978a3-104">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="978a3-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="978a3-105">句法</span><span class="sxs-lookup"><span data-stu-id="978a3-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978a3-106">說明</span><span class="sxs-lookup"><span data-stu-id="978a3-106">DESCRIPTION</span></span>
<span data-ttu-id="978a3-107">關閉 autosaving Azure 認證。</span><span class="sxs-lookup"><span data-stu-id="978a3-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="978a3-108">下次開啟 PowerShell 視窗時，系統會忘記您的登入資訊</span><span class="sxs-lookup"><span data-stu-id="978a3-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="978a3-109">示例</span><span class="sxs-lookup"><span data-stu-id="978a3-109">EXAMPLES</span></span>

### <span data-ttu-id="978a3-110">停用 autosaving 內容</span><span class="sxs-lookup"><span data-stu-id="978a3-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="978a3-111">停用目前使用者的自動儲存功能。</span><span class="sxs-lookup"><span data-stu-id="978a3-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="978a3-112">參數</span><span class="sxs-lookup"><span data-stu-id="978a3-112">PARAMETERS</span></span>

### <span data-ttu-id="978a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978a3-113">-DefaultProfile</span></span>
<span data-ttu-id="978a3-114">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="978a3-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="978a3-115">-範圍</span><span class="sxs-lookup"><span data-stu-id="978a3-115">-Scope</span></span>
<span data-ttu-id="978a3-116">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="978a3-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="978a3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="978a3-117">-Confirm</span></span>
<span data-ttu-id="978a3-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="978a3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978a3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978a3-119">-WhatIf</span></span>
<span data-ttu-id="978a3-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="978a3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978a3-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="978a3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978a3-122">CommonParameters</span></span>
<span data-ttu-id="978a3-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="978a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978a3-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="978a3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978a3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="978a3-125">INPUTS</span></span>

### <span data-ttu-id="978a3-126">所有</span><span class="sxs-lookup"><span data-stu-id="978a3-126">None</span></span>

## <span data-ttu-id="978a3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="978a3-127">OUTPUTS</span></span>

### <span data-ttu-id="978a3-128">CoNtextAutosaveSettings 的常見驗證。</span><span class="sxs-lookup"><span data-stu-id="978a3-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="978a3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="978a3-129">NOTES</span></span>

## <span data-ttu-id="978a3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="978a3-130">RELATED LINKS</span></span>
