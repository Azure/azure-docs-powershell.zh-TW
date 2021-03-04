---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 8db930fe362d25a7b1069af6c3855ef71644e874
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911802"
---
# <span data-ttu-id="8b148-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="8b148-101">Clear-AzContext</span></span>

## <span data-ttu-id="8b148-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b148-102">SYNOPSIS</span></span>
<span data-ttu-id="8b148-103">移除所有 Azure 認證、帳戶和訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="8b148-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="8b148-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b148-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b148-105">描述</span><span class="sxs-lookup"><span data-stu-id="8b148-105">DESCRIPTION</span></span>
<span data-ttu-id="8b148-106">移除所有 Azure 認證、帳戶和訂閱資訊。</span><span class="sxs-lookup"><span data-stu-id="8b148-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="8b148-107">例子</span><span class="sxs-lookup"><span data-stu-id="8b148-107">EXAMPLES</span></span>

### <span data-ttu-id="8b148-108">範例 1：清除全域上下文</span><span class="sxs-lookup"><span data-stu-id="8b148-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="8b148-109">移除任何 Powershell 會話的所有帳戶、訂閱和認證資訊。</span><span class="sxs-lookup"><span data-stu-id="8b148-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="8b148-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b148-110">PARAMETERS</span></span>

### <span data-ttu-id="8b148-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b148-111">-DefaultProfile</span></span>
<span data-ttu-id="8b148-112">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8b148-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b148-113">-強制</span><span class="sxs-lookup"><span data-stu-id="8b148-113">-Force</span></span>
<span data-ttu-id="8b148-114">刪除全域範圍中的所有使用者和群組，而不提示</span><span class="sxs-lookup"><span data-stu-id="8b148-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="8b148-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b148-115">-PassThru</span></span>
<span data-ttu-id="8b148-116">返回指出成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="8b148-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="8b148-117">-範圍</span><span class="sxs-lookup"><span data-stu-id="8b148-117">-Scope</span></span>
<span data-ttu-id="8b148-118">僅清除目前 PowerShell 會話或所有會話的上下文。</span><span class="sxs-lookup"><span data-stu-id="8b148-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="8b148-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8b148-119">-Confirm</span></span>
<span data-ttu-id="8b148-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8b148-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b148-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b148-121">-WhatIf</span></span>
<span data-ttu-id="8b148-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b148-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b148-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b148-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b148-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b148-124">CommonParameters</span></span>
<span data-ttu-id="8b148-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b148-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b148-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b148-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b148-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8b148-127">INPUTS</span></span>

### <span data-ttu-id="8b148-128">沒有</span><span class="sxs-lookup"><span data-stu-id="8b148-128">None</span></span>

## <span data-ttu-id="8b148-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8b148-129">OUTPUTS</span></span>

### <span data-ttu-id="8b148-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b148-130">System.Boolean</span></span>

## <span data-ttu-id="8b148-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8b148-131">NOTES</span></span>

## <span data-ttu-id="8b148-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b148-132">RELATED LINKS</span></span>
