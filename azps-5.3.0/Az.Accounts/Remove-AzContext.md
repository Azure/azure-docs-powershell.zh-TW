---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437819"
---
# <span data-ttu-id="c1545-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="c1545-101">Remove-AzContext</span></span>

## <span data-ttu-id="c1545-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1545-102">SYNOPSIS</span></span>
<span data-ttu-id="c1545-103">從可用的上下文集合中移除內容</span><span class="sxs-lookup"><span data-stu-id="c1545-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="c1545-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1545-104">SYNTAX</span></span>

### <span data-ttu-id="c1545-105">RemoveByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="c1545-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1545-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="c1545-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="c1545-107">說明</span><span class="sxs-lookup"><span data-stu-id="c1545-107">DESCRIPTION</span></span>
<span data-ttu-id="c1545-108">從一組內容中移除 azure 內容</span><span class="sxs-lookup"><span data-stu-id="c1545-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="c1545-109">示例</span><span class="sxs-lookup"><span data-stu-id="c1545-109">EXAMPLES</span></span>

### <span data-ttu-id="c1545-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c1545-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="c1545-111">移除名為 [預設值] 的內容</span><span class="sxs-lookup"><span data-stu-id="c1545-111">Remove the context named default</span></span>

## <span data-ttu-id="c1545-112">參數</span><span class="sxs-lookup"><span data-stu-id="c1545-112">PARAMETERS</span></span>

### <span data-ttu-id="c1545-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1545-113">-DefaultProfile</span></span>
<span data-ttu-id="c1545-114">用於與 azure 進行通訊的認證、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1545-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1545-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c1545-115">-Force</span></span>
<span data-ttu-id="c1545-116">移除內容（即使是預設值）</span><span class="sxs-lookup"><span data-stu-id="c1545-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="c1545-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1545-117">-InputObject</span></span>
<span data-ttu-id="c1545-118">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="c1545-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1545-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1545-119">-Name</span></span>
<span data-ttu-id="c1545-120">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="c1545-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1545-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1545-121">-PassThru</span></span>
<span data-ttu-id="c1545-122">傳回移除的內容</span><span class="sxs-lookup"><span data-stu-id="c1545-122">Return the removed context</span></span>

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

### <span data-ttu-id="c1545-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="c1545-123">-Scope</span></span>
<span data-ttu-id="c1545-124">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="c1545-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="c1545-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c1545-125">-Confirm</span></span>
<span data-ttu-id="c1545-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1545-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1545-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1545-127">-WhatIf</span></span>
<span data-ttu-id="c1545-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1545-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1545-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1545-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1545-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1545-130">CommonParameters</span></span>
<span data-ttu-id="c1545-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1545-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1545-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1545-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1545-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c1545-133">INPUTS</span></span>

### <span data-ttu-id="c1545-134">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1545-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c1545-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c1545-135">OUTPUTS</span></span>

### <span data-ttu-id="c1545-136">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="c1545-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c1545-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c1545-137">NOTES</span></span>

## <span data-ttu-id="c1545-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1545-138">RELATED LINKS</span></span>
