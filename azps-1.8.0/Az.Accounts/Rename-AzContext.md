---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 809ec5bb5388447e5f20fe267598660ac0e49ec8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611724"
---
# <span data-ttu-id="90d14-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="90d14-101">Rename-AzContext</span></span>

## <span data-ttu-id="90d14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90d14-102">SYNOPSIS</span></span>
<span data-ttu-id="90d14-103">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="90d14-103">Rename an Azure context.</span></span>  <span data-ttu-id="90d14-104">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="90d14-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="90d14-105">句法</span><span class="sxs-lookup"><span data-stu-id="90d14-105">SYNTAX</span></span>

### <span data-ttu-id="90d14-106">RenameByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="90d14-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="90d14-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="90d14-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="90d14-108">說明</span><span class="sxs-lookup"><span data-stu-id="90d14-108">DESCRIPTION</span></span>
<span data-ttu-id="90d14-109">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="90d14-109">Rename an Azure context.</span></span>  <span data-ttu-id="90d14-110">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="90d14-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="90d14-111">示例</span><span class="sxs-lookup"><span data-stu-id="90d14-111">EXAMPLES</span></span>

### <span data-ttu-id="90d14-112">使用具名引數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="90d14-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="90d14-113">將 "" 的內容重新命名 user1@contoso.org 為 "12345-6789-2345-3567890" 到 "Work"。</span><span class="sxs-lookup"><span data-stu-id="90d14-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="90d14-114">此命令之後，您就可以使用 [Select-AzCoNtext Work] 來設定內容的目標。</span><span class="sxs-lookup"><span data-stu-id="90d14-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="90d14-115">請注意，您可以使用 tab 完成，以 tab 鍵在 [</span><span class="sxs-lookup"><span data-stu-id="90d14-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="90d14-116">使用位置參數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="90d14-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="90d14-117">將名為「我的內容」的內容重新命名為「工作」。</span><span class="sxs-lookup"><span data-stu-id="90d14-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="90d14-118">此命令之後，您就可以使用 Select-AzContext 的工作來設定內容的目標</span><span class="sxs-lookup"><span data-stu-id="90d14-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="90d14-119">參數</span><span class="sxs-lookup"><span data-stu-id="90d14-119">PARAMETERS</span></span>

### <span data-ttu-id="90d14-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d14-120">-DefaultProfile</span></span>
<span data-ttu-id="90d14-121">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="90d14-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90d14-122">-Force</span><span class="sxs-lookup"><span data-stu-id="90d14-122">-Force</span></span>
<span data-ttu-id="90d14-123">即使目標內容已存在，也要重新命名內容</span><span class="sxs-lookup"><span data-stu-id="90d14-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="90d14-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90d14-124">-InputObject</span></span>
<span data-ttu-id="90d14-125">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="90d14-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="90d14-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90d14-126">-PassThru</span></span>
<span data-ttu-id="90d14-127">傳回重新命名的內容。</span><span class="sxs-lookup"><span data-stu-id="90d14-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="90d14-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="90d14-128">-Scope</span></span>
<span data-ttu-id="90d14-129">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="90d14-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="90d14-130">-已</span><span class="sxs-lookup"><span data-stu-id="90d14-130">-SourceName</span></span>
<span data-ttu-id="90d14-131">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="90d14-131">The name of the context</span></span>

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

### <span data-ttu-id="90d14-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="90d14-132">-TargetName</span></span>
<span data-ttu-id="90d14-133">內容的新名稱</span><span class="sxs-lookup"><span data-stu-id="90d14-133">The new name of the context</span></span>

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

### <span data-ttu-id="90d14-134">-確認</span><span class="sxs-lookup"><span data-stu-id="90d14-134">-Confirm</span></span>
<span data-ttu-id="90d14-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90d14-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d14-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d14-136">-WhatIf</span></span>
<span data-ttu-id="90d14-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90d14-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d14-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90d14-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d14-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d14-139">CommonParameters</span></span>
<span data-ttu-id="90d14-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90d14-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d14-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90d14-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d14-142">輸入</span><span class="sxs-lookup"><span data-stu-id="90d14-142">INPUTS</span></span>

### <span data-ttu-id="90d14-143">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="90d14-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="90d14-144">輸出</span><span class="sxs-lookup"><span data-stu-id="90d14-144">OUTPUTS</span></span>

### <span data-ttu-id="90d14-145">PSAzureCoNtext 的基本設定檔。</span><span class="sxs-lookup"><span data-stu-id="90d14-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="90d14-146">筆記</span><span class="sxs-lookup"><span data-stu-id="90d14-146">NOTES</span></span>

## <span data-ttu-id="90d14-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="90d14-147">RELATED LINKS</span></span>