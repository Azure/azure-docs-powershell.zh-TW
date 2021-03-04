---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: f5307df3a91503f072c8292fe37957ce9af0df49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902654"
---
# <span data-ttu-id="333b3-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="333b3-101">Remove-AzContext</span></span>

## <span data-ttu-id="333b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="333b3-102">SYNOPSIS</span></span>
<span data-ttu-id="333b3-103">從一組可用的上下文移除內容</span><span class="sxs-lookup"><span data-stu-id="333b3-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="333b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="333b3-104">SYNTAX</span></span>

### <span data-ttu-id="333b3-105">RemoveByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="333b3-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333b3-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="333b3-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="333b3-107">描述</span><span class="sxs-lookup"><span data-stu-id="333b3-107">DESCRIPTION</span></span>
<span data-ttu-id="333b3-108">從一組上下文移除 Azure 上下文</span><span class="sxs-lookup"><span data-stu-id="333b3-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="333b3-109">例子</span><span class="sxs-lookup"><span data-stu-id="333b3-109">EXAMPLES</span></span>

### <span data-ttu-id="333b3-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="333b3-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="333b3-111">移除名稱為 default 的上下文</span><span class="sxs-lookup"><span data-stu-id="333b3-111">Remove the context named default</span></span>

## <span data-ttu-id="333b3-112">參數</span><span class="sxs-lookup"><span data-stu-id="333b3-112">PARAMETERS</span></span>

### <span data-ttu-id="333b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b3-113">-DefaultProfile</span></span>
<span data-ttu-id="333b3-114">用於與 Azure 通訊的認證、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="333b3-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333b3-115">-強制</span><span class="sxs-lookup"><span data-stu-id="333b3-115">-Force</span></span>
<span data-ttu-id="333b3-116">移除上下文 ，即使它是預設內容</span><span class="sxs-lookup"><span data-stu-id="333b3-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="333b3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="333b3-117">-InputObject</span></span>
<span data-ttu-id="333b3-118">操作物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="333b3-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="333b3-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="333b3-119">-Name</span></span>
<span data-ttu-id="333b3-120">內容名稱</span><span class="sxs-lookup"><span data-stu-id="333b3-120">The name of the context</span></span>

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

### <span data-ttu-id="333b3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="333b3-121">-PassThru</span></span>
<span data-ttu-id="333b3-122">返回移除的上下文</span><span class="sxs-lookup"><span data-stu-id="333b3-122">Return the removed context</span></span>

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

### <span data-ttu-id="333b3-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="333b3-123">-Scope</span></span>
<span data-ttu-id="333b3-124">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或是否適用于此使用者啟動的所有會話</span><span class="sxs-lookup"><span data-stu-id="333b3-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="333b3-125">-確認</span><span class="sxs-lookup"><span data-stu-id="333b3-125">-Confirm</span></span>
<span data-ttu-id="333b3-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="333b3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333b3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333b3-127">-WhatIf</span></span>
<span data-ttu-id="333b3-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="333b3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333b3-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="333b3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b3-130">CommonParameters</span></span>
<span data-ttu-id="333b3-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="333b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b3-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="333b3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b3-133">輸入</span><span class="sxs-lookup"><span data-stu-id="333b3-133">INPUTS</span></span>

### <span data-ttu-id="333b3-134">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="333b3-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="333b3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="333b3-135">OUTPUTS</span></span>

### <span data-ttu-id="333b3-136">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="333b3-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="333b3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="333b3-137">NOTES</span></span>

## <span data-ttu-id="333b3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="333b3-138">RELATED LINKS</span></span>
