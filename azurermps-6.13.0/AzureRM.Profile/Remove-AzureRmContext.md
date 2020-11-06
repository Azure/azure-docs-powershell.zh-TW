---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 0e102d6c0c4db5bd3d93d4349a2a0e06284cd8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448971"
---
# <span data-ttu-id="4f347-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4f347-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="4f347-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f347-102">SYNOPSIS</span></span>
<span data-ttu-id="4f347-103">從可用的上下文集合中移除內容</span><span class="sxs-lookup"><span data-stu-id="4f347-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f347-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f347-104">SYNTAX</span></span>

### <span data-ttu-id="4f347-105">RemoveByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="4f347-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f347-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="4f347-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="4f347-107">說明</span><span class="sxs-lookup"><span data-stu-id="4f347-107">DESCRIPTION</span></span>
<span data-ttu-id="4f347-108">從一組內容中移除 azure 內容</span><span class="sxs-lookup"><span data-stu-id="4f347-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="4f347-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f347-109">EXAMPLES</span></span>

### <span data-ttu-id="4f347-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4f347-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="4f347-111">移除名為 [預設值] 的內容</span><span class="sxs-lookup"><span data-stu-id="4f347-111">Remove the context named default</span></span>

## <span data-ttu-id="4f347-112">參數</span><span class="sxs-lookup"><span data-stu-id="4f347-112">PARAMETERS</span></span>

### <span data-ttu-id="4f347-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f347-113">-DefaultProfile</span></span>
<span data-ttu-id="4f347-114">用於與 azure 進行通訊的認證、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f347-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f347-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4f347-115">-Force</span></span>
<span data-ttu-id="4f347-116">移除內容，即使是 defualt</span><span class="sxs-lookup"><span data-stu-id="4f347-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="4f347-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f347-117">-InputObject</span></span>
<span data-ttu-id="4f347-118">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="4f347-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f347-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f347-119">-Name</span></span>
<span data-ttu-id="4f347-120">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="4f347-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f347-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f347-121">-PassThru</span></span>
<span data-ttu-id="4f347-122">傳回移除的內容</span><span class="sxs-lookup"><span data-stu-id="4f347-122">Return the removed context</span></span>

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

### <span data-ttu-id="4f347-123">-範圍</span><span class="sxs-lookup"><span data-stu-id="4f347-123">-Scope</span></span>
<span data-ttu-id="4f347-124">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="4f347-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="4f347-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4f347-125">-Confirm</span></span>
<span data-ttu-id="4f347-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f347-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f347-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f347-127">-WhatIf</span></span>
<span data-ttu-id="4f347-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f347-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f347-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f347-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f347-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f347-130">CommonParameters</span></span>
<span data-ttu-id="4f347-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f347-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f347-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f347-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f347-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4f347-133">INPUTS</span></span>

### <span data-ttu-id="4f347-134">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4f347-134">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="4f347-135">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4f347-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4f347-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4f347-136">OUTPUTS</span></span>

### <span data-ttu-id="4f347-137">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4f347-137">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="4f347-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4f347-138">NOTES</span></span>

## <span data-ttu-id="4f347-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f347-139">RELATED LINKS</span></span>
