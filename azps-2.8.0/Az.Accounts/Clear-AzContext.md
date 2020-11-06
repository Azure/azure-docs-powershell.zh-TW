---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b54cfdc68c1f6c400decdac9a1ef0f49823a1712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614222"
---
# <span data-ttu-id="576ea-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="576ea-101">Clear-AzContext</span></span>

## <span data-ttu-id="576ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="576ea-102">SYNOPSIS</span></span>
<span data-ttu-id="576ea-103">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="576ea-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="576ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="576ea-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="576ea-105">DESCRIPTION</span></span>
<span data-ttu-id="576ea-106">移除所有 Azure 認證、帳戶及訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="576ea-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="576ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="576ea-107">EXAMPLES</span></span>

### <span data-ttu-id="576ea-108">清除全域內容</span><span class="sxs-lookup"><span data-stu-id="576ea-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="576ea-109">移除任何 powershell 會話的所有帳戶、訂閱及認證資訊。</span><span class="sxs-lookup"><span data-stu-id="576ea-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="576ea-110">參數</span><span class="sxs-lookup"><span data-stu-id="576ea-110">PARAMETERS</span></span>

### <span data-ttu-id="576ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576ea-111">-DefaultProfile</span></span>
<span data-ttu-id="576ea-112">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="576ea-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="576ea-113">-Force</span><span class="sxs-lookup"><span data-stu-id="576ea-113">-Force</span></span>
<span data-ttu-id="576ea-114">刪除全域範圍中的所有使用者和群組，但不提示</span><span class="sxs-lookup"><span data-stu-id="576ea-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="576ea-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="576ea-115">-PassThru</span></span>
<span data-ttu-id="576ea-116">傳回表示成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="576ea-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="576ea-117">-範圍</span><span class="sxs-lookup"><span data-stu-id="576ea-117">-Scope</span></span>
<span data-ttu-id="576ea-118">清除目前 PowerShell 會話或所有會話的內容。</span><span class="sxs-lookup"><span data-stu-id="576ea-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="576ea-119">-確認</span><span class="sxs-lookup"><span data-stu-id="576ea-119">-Confirm</span></span>
<span data-ttu-id="576ea-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="576ea-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576ea-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576ea-121">-WhatIf</span></span>
<span data-ttu-id="576ea-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="576ea-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576ea-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="576ea-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576ea-124">CommonParameters</span></span>
<span data-ttu-id="576ea-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="576ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576ea-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="576ea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576ea-127">輸入</span><span class="sxs-lookup"><span data-stu-id="576ea-127">INPUTS</span></span>

### <span data-ttu-id="576ea-128">所有</span><span class="sxs-lookup"><span data-stu-id="576ea-128">None</span></span>

## <span data-ttu-id="576ea-129">輸出</span><span class="sxs-lookup"><span data-stu-id="576ea-129">OUTPUTS</span></span>

### <span data-ttu-id="576ea-130">System.object</span><span class="sxs-lookup"><span data-stu-id="576ea-130">System.Boolean</span></span>

## <span data-ttu-id="576ea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="576ea-131">NOTES</span></span>

## <span data-ttu-id="576ea-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="576ea-132">RELATED LINKS</span></span>