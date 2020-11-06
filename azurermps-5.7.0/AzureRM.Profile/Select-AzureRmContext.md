---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: c002db2d04905c19c3229a45feb9e00b5dc15754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454175"
---
# <span data-ttu-id="295e8-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="295e8-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="295e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="295e8-102">SYNOPSIS</span></span>
<span data-ttu-id="295e8-103">選取 Azure PowerShell Cmdlet 中的目標訂閱與帳戶</span><span class="sxs-lookup"><span data-stu-id="295e8-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="295e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="295e8-104">SYNTAX</span></span>

### <span data-ttu-id="295e8-105">SelectByInputObject (預設) </span><span class="sxs-lookup"><span data-stu-id="295e8-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="295e8-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="295e8-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="295e8-107">說明</span><span class="sxs-lookup"><span data-stu-id="295e8-107">DESCRIPTION</span></span>
<span data-ttu-id="295e8-108">選取訂閱以針對 Azure PowerShell Cmdlet 中的 (或帳戶或租使用者) 。</span><span class="sxs-lookup"><span data-stu-id="295e8-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="295e8-109">在這個 Cmdlet 之後，未來的 Cmdlet 會以所選的內容為目標。</span><span class="sxs-lookup"><span data-stu-id="295e8-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="295e8-110">示例</span><span class="sxs-lookup"><span data-stu-id="295e8-110">EXAMPLES</span></span>

### <span data-ttu-id="295e8-111">範例1：以命名的內容為目標</span><span class="sxs-lookup"><span data-stu-id="295e8-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="295e8-112">在「工作」內容的帳戶、租使用者和訂閱中，以未來的 Azure PowerShell Cmdlet 為目標。</span><span class="sxs-lookup"><span data-stu-id="295e8-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="295e8-113">參數</span><span class="sxs-lookup"><span data-stu-id="295e8-113">PARAMETERS</span></span>

### <span data-ttu-id="295e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="295e8-114">-DefaultProfile</span></span>
<span data-ttu-id="295e8-115">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="295e8-115">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="295e8-116">-InputObject</span></span>
<span data-ttu-id="295e8-117">內容物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="295e8-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: SelectByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="295e8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="295e8-118">-Name</span></span>
<span data-ttu-id="295e8-119">內容的名稱</span><span class="sxs-lookup"><span data-stu-id="295e8-119">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: SelectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e8-120">-範圍</span><span class="sxs-lookup"><span data-stu-id="295e8-120">-Scope</span></span>
<span data-ttu-id="295e8-121">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話</span><span class="sxs-lookup"><span data-stu-id="295e8-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="295e8-122">-Confirm</span></span>
<span data-ttu-id="295e8-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="295e8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="295e8-124">-WhatIf</span></span>
<span data-ttu-id="295e8-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="295e8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="295e8-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="295e8-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="295e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="295e8-127">CommonParameters</span></span>
<span data-ttu-id="295e8-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="295e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="295e8-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="295e8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="295e8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="295e8-130">INPUTS</span></span>

### <span data-ttu-id="295e8-131">所有</span><span class="sxs-lookup"><span data-stu-id="295e8-131">None</span></span>

## <span data-ttu-id="295e8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="295e8-132">OUTPUTS</span></span>

### <span data-ttu-id="295e8-133">PSAzureCoNtext 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="295e8-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="295e8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="295e8-134">NOTES</span></span>

## <span data-ttu-id="295e8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="295e8-135">RELATED LINKS</span></span>

