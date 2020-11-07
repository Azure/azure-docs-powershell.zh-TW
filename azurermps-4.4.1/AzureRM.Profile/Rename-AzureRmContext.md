---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626246"
---
# <span data-ttu-id="60f77-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="60f77-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="60f77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60f77-102">SYNOPSIS</span></span>
<span data-ttu-id="60f77-103">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="60f77-103">Rename an Azure context.</span></span>  <span data-ttu-id="60f77-104">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="60f77-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60f77-105">句法</span><span class="sxs-lookup"><span data-stu-id="60f77-105">SYNTAX</span></span>

### <span data-ttu-id="60f77-106">輸入物件 (預設) </span><span class="sxs-lookup"><span data-stu-id="60f77-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="60f77-107">內容名稱</span><span class="sxs-lookup"><span data-stu-id="60f77-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="60f77-108">說明</span><span class="sxs-lookup"><span data-stu-id="60f77-108">DESCRIPTION</span></span>
<span data-ttu-id="60f77-109">重新命名 Azure 內容。</span><span class="sxs-lookup"><span data-stu-id="60f77-109">Rename an Azure context.</span></span>  <span data-ttu-id="60f77-110">根據預設，上下文是依使用者帳戶和訂閱來命名。</span><span class="sxs-lookup"><span data-stu-id="60f77-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="60f77-111">示例</span><span class="sxs-lookup"><span data-stu-id="60f77-111">EXAMPLES</span></span>

### <span data-ttu-id="60f77-112">使用具名引數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="60f77-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="60f77-113">將 "" 的內容重新命名 user1@contoso.org 為 "12345-6789-2345-3567890" 到 "Work"。</span><span class="sxs-lookup"><span data-stu-id="60f77-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="60f77-114">此命令之後，您就可以使用 [Select-AzureRmCoNtext Work] 來設定內容的目標。</span><span class="sxs-lookup"><span data-stu-id="60f77-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="60f77-115">請注意，您可以使用 tab 完成，以 tab 鍵在 [</span><span class="sxs-lookup"><span data-stu-id="60f77-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="60f77-116">使用位置參數重新命名內容</span><span class="sxs-lookup"><span data-stu-id="60f77-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="60f77-117">將名為「我的內容」的內容重新命名為「工作」。</span><span class="sxs-lookup"><span data-stu-id="60f77-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="60f77-118">此命令之後，您就可以使用 Select-AzureRmContext 的工作來設定內容的目標</span><span class="sxs-lookup"><span data-stu-id="60f77-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="60f77-119">參數</span><span class="sxs-lookup"><span data-stu-id="60f77-119">PARAMETERS</span></span>

### <span data-ttu-id="60f77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f77-120">-DefaultProfile</span></span>
<span data-ttu-id="60f77-121">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="60f77-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f77-122">-Force</span><span class="sxs-lookup"><span data-stu-id="60f77-122">-Force</span></span>
<span data-ttu-id="60f77-123">即使目標內容已存在，也要重新命名內容</span><span class="sxs-lookup"><span data-stu-id="60f77-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="60f77-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60f77-124">-InputObject</span></span>
<span data-ttu-id="60f77-125">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="60f77-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60f77-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60f77-126">-PassThru</span></span>
<span data-ttu-id="60f77-127">傳回重新命名的內容。</span><span class="sxs-lookup"><span data-stu-id="60f77-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="60f77-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="60f77-128">-Scope</span></span>
<span data-ttu-id="60f77-129">決定內容變更的範圍，例如，wheher 變更只適用于 cusrrent 進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="60f77-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="60f77-130">-已</span><span class="sxs-lookup"><span data-stu-id="60f77-130">-SourceName</span></span>
<span data-ttu-id="60f77-131">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="60f77-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60f77-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="60f77-132">-TargetName</span></span>
<span data-ttu-id="60f77-133">內容的新名稱</span><span class="sxs-lookup"><span data-stu-id="60f77-133">The new name of the context</span></span>

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

### <span data-ttu-id="60f77-134">-確認</span><span class="sxs-lookup"><span data-stu-id="60f77-134">-Confirm</span></span>
<span data-ttu-id="60f77-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60f77-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f77-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f77-136">-WhatIf</span></span>
<span data-ttu-id="60f77-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60f77-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f77-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60f77-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f77-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f77-139">CommonParameters</span></span>
<span data-ttu-id="60f77-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60f77-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f77-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60f77-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f77-142">輸入</span><span class="sxs-lookup"><span data-stu-id="60f77-142">INPUTS</span></span>

### <span data-ttu-id="60f77-143">所有</span><span class="sxs-lookup"><span data-stu-id="60f77-143">None</span></span>

## <span data-ttu-id="60f77-144">輸出</span><span class="sxs-lookup"><span data-stu-id="60f77-144">OUTPUTS</span></span>

### <span data-ttu-id="60f77-145">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="60f77-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="60f77-146">筆記</span><span class="sxs-lookup"><span data-stu-id="60f77-146">NOTES</span></span>

## <span data-ttu-id="60f77-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="60f77-147">RELATED LINKS</span></span>

