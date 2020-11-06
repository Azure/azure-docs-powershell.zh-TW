---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: aea1fac4450a8625eb3d31e9f951a465344a3bd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448969"
---
# <span data-ttu-id="34980-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="34980-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="34980-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34980-102">SYNOPSIS</span></span>
<span data-ttu-id="34980-103">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="34980-103">Rename an Azure context.</span></span>  <span data-ttu-id="34980-104">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="34980-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34980-105">句法</span><span class="sxs-lookup"><span data-stu-id="34980-105">SYNTAX</span></span>

### <span data-ttu-id="34980-106">RenameByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="34980-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="34980-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="34980-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="34980-108">說明</span><span class="sxs-lookup"><span data-stu-id="34980-108">DESCRIPTION</span></span>
<span data-ttu-id="34980-109">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="34980-109">Rename an Azure context.</span></span>  <span data-ttu-id="34980-110">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="34980-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="34980-111">示例</span><span class="sxs-lookup"><span data-stu-id="34980-111">EXAMPLES</span></span>

### <span data-ttu-id="34980-112">使用具名引數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="34980-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="34980-113">將 "" 的內容重新命名 user1@contoso.org 為 "12345-6789-2345-3567890" 到 "Work"。</span><span class="sxs-lookup"><span data-stu-id="34980-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="34980-114">此命令之後，您就可以使用 [Select-AzureRmCoNtext Work] 來設定內容的目標。</span><span class="sxs-lookup"><span data-stu-id="34980-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="34980-115">請注意，您可以使用 tab 完成，以 tab 鍵在 [</span><span class="sxs-lookup"><span data-stu-id="34980-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="34980-116">使用位置參數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="34980-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="34980-117">將名為「我的內容」的內容重新命名為「工作」。</span><span class="sxs-lookup"><span data-stu-id="34980-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="34980-118">此命令之後，您就可以使用 Select-AzureRmContext 的工作來設定內容的目標</span><span class="sxs-lookup"><span data-stu-id="34980-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="34980-119">參數</span><span class="sxs-lookup"><span data-stu-id="34980-119">PARAMETERS</span></span>

### <span data-ttu-id="34980-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34980-120">-DefaultProfile</span></span>
<span data-ttu-id="34980-121">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="34980-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34980-122">-Force</span><span class="sxs-lookup"><span data-stu-id="34980-122">-Force</span></span>
<span data-ttu-id="34980-123">即使目標內容已存在，也要重新命名內容</span><span class="sxs-lookup"><span data-stu-id="34980-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="34980-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34980-124">-InputObject</span></span>
<span data-ttu-id="34980-125">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="34980-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34980-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34980-126">-PassThru</span></span>
<span data-ttu-id="34980-127">傳回重新命名的內容。</span><span class="sxs-lookup"><span data-stu-id="34980-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="34980-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="34980-128">-Scope</span></span>
<span data-ttu-id="34980-129">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="34980-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="34980-130">-已</span><span class="sxs-lookup"><span data-stu-id="34980-130">-SourceName</span></span>
<span data-ttu-id="34980-131">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="34980-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34980-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="34980-132">-TargetName</span></span>
<span data-ttu-id="34980-133">內容的新名稱</span><span class="sxs-lookup"><span data-stu-id="34980-133">The new name of the context</span></span>

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

### <span data-ttu-id="34980-134">-確認</span><span class="sxs-lookup"><span data-stu-id="34980-134">-Confirm</span></span>
<span data-ttu-id="34980-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34980-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34980-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34980-136">-WhatIf</span></span>
<span data-ttu-id="34980-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34980-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34980-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34980-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34980-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34980-139">CommonParameters</span></span>
<span data-ttu-id="34980-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34980-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34980-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="34980-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34980-142">輸入</span><span class="sxs-lookup"><span data-stu-id="34980-142">INPUTS</span></span>

### <span data-ttu-id="34980-143">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="34980-143">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="34980-144">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="34980-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="34980-145">輸出</span><span class="sxs-lookup"><span data-stu-id="34980-145">OUTPUTS</span></span>

### <span data-ttu-id="34980-146">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="34980-146">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="34980-147">筆記</span><span class="sxs-lookup"><span data-stu-id="34980-147">NOTES</span></span>

## <span data-ttu-id="34980-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="34980-148">RELATED LINKS</span></span>
