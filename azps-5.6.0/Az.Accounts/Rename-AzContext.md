---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 2ff8297ff04f18a903cca3a262d5232ace7c6ef1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905306"
---
# <span data-ttu-id="26d0f-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="26d0f-101">Rename-AzContext</span></span>

## <span data-ttu-id="26d0f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="26d0f-103">重新命名 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="26d0f-103">Rename an Azure context.</span></span>  <span data-ttu-id="26d0f-104">根據預設，上下文會以使用者帳戶和訂閱命名。</span><span class="sxs-lookup"><span data-stu-id="26d0f-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="26d0f-105">語法</span><span class="sxs-lookup"><span data-stu-id="26d0f-105">SYNTAX</span></span>

### <span data-ttu-id="26d0f-106">RenameByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="26d0f-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="26d0f-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="26d0f-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="26d0f-108">描述</span><span class="sxs-lookup"><span data-stu-id="26d0f-108">DESCRIPTION</span></span>
<span data-ttu-id="26d0f-109">重新命名 Azure 上下文。</span><span class="sxs-lookup"><span data-stu-id="26d0f-109">Rename an Azure context.</span></span>  <span data-ttu-id="26d0f-110">根據預設，上下文會以使用者帳戶和訂閱命名。</span><span class="sxs-lookup"><span data-stu-id="26d0f-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="26d0f-111">例子</span><span class="sxs-lookup"><span data-stu-id="26d0f-111">EXAMPLES</span></span>

### <span data-ttu-id="26d0f-112">範例 1：使用具名引數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="26d0f-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="26d0f-113">將訂閱 user1@contoso.org '12345-6789-2345-3567890' 的 '內容重新命名為 'Work'。</span><span class="sxs-lookup"><span data-stu-id="26d0f-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="26d0f-114">此命令之後，您將可以使用 [Select-AzCoNtext Work」 來鎖定內容。</span><span class="sxs-lookup"><span data-stu-id="26d0f-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="26d0f-115">請注意，您可以使用 Tab completion 在 "SourceName" 的值中按 Tab 鍵。</span><span class="sxs-lookup"><span data-stu-id="26d0f-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="26d0f-116">範例 2：使用位置參數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="26d0f-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="26d0f-117">將名為「我的上下文」的上下文重新命名為「工作」。</span><span class="sxs-lookup"><span data-stu-id="26d0f-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="26d0f-118">此命令之後，您就能使用工作來Select-AzContext內容</span><span class="sxs-lookup"><span data-stu-id="26d0f-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="26d0f-119">參數</span><span class="sxs-lookup"><span data-stu-id="26d0f-119">PARAMETERS</span></span>

### <span data-ttu-id="26d0f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d0f-120">-DefaultProfile</span></span>
<span data-ttu-id="26d0f-121">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="26d0f-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26d0f-122">-強制</span><span class="sxs-lookup"><span data-stu-id="26d0f-122">-Force</span></span>
<span data-ttu-id="26d0f-123">重新命名內容，即使目標上下文已存在</span><span class="sxs-lookup"><span data-stu-id="26d0f-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="26d0f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26d0f-124">-InputObject</span></span>
<span data-ttu-id="26d0f-125">操作物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="26d0f-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26d0f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26d0f-126">-PassThru</span></span>
<span data-ttu-id="26d0f-127">返回重新命名的上下文。</span><span class="sxs-lookup"><span data-stu-id="26d0f-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="26d0f-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="26d0f-128">-Scope</span></span>
<span data-ttu-id="26d0f-129">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或是否適用于此使用者啟動的所有會話</span><span class="sxs-lookup"><span data-stu-id="26d0f-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="26d0f-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="26d0f-130">-SourceName</span></span>
<span data-ttu-id="26d0f-131">內容名稱</span><span class="sxs-lookup"><span data-stu-id="26d0f-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d0f-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="26d0f-132">-TargetName</span></span>
<span data-ttu-id="26d0f-133">內容的新名稱</span><span class="sxs-lookup"><span data-stu-id="26d0f-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d0f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="26d0f-134">-Confirm</span></span>
<span data-ttu-id="26d0f-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="26d0f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d0f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d0f-136">-WhatIf</span></span>
<span data-ttu-id="26d0f-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26d0f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26d0f-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26d0f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d0f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d0f-139">CommonParameters</span></span>
<span data-ttu-id="26d0f-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26d0f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d0f-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26d0f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d0f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="26d0f-142">INPUTS</span></span>

### <span data-ttu-id="26d0f-143">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="26d0f-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="26d0f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="26d0f-144">OUTPUTS</span></span>

### <span data-ttu-id="26d0f-145">Microsoft.Azure.Commands.Profile.models.Core.PSAzureCoNtext</span><span class="sxs-lookup"><span data-stu-id="26d0f-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="26d0f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="26d0f-146">NOTES</span></span>

## <span data-ttu-id="26d0f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="26d0f-147">RELATED LINKS</span></span>
