---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447824"
---
# <span data-ttu-id="b613c-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="b613c-101">Clear-AzDefault</span></span>

## <span data-ttu-id="b613c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b613c-102">SYNOPSIS</span></span>
<span data-ttu-id="b613c-103">清除目前內容中由使用者設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="b613c-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="b613c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b613c-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b613c-105">說明</span><span class="sxs-lookup"><span data-stu-id="b613c-105">DESCRIPTION</span></span>
<span data-ttu-id="b613c-106">Clear-AzDefault Cmdlet 會根據使用者指定的切換參數，移除使用者所設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="b613c-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="b613c-107">示例</span><span class="sxs-lookup"><span data-stu-id="b613c-107">EXAMPLES</span></span>

### <span data-ttu-id="b613c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b613c-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="b613c-109">這個命令會移除使用者在目前內容中設定的所有預設值。</span><span class="sxs-lookup"><span data-stu-id="b613c-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="b613c-110">範例2</span><span class="sxs-lookup"><span data-stu-id="b613c-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="b613c-111">這個命令會移除目前內容中由使用者所設定的預設資源群組。</span><span class="sxs-lookup"><span data-stu-id="b613c-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="b613c-112">參數</span><span class="sxs-lookup"><span data-stu-id="b613c-112">PARAMETERS</span></span>

### <span data-ttu-id="b613c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b613c-113">-DefaultProfile</span></span>
<span data-ttu-id="b613c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b613c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b613c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b613c-115">-Force</span></span>
<span data-ttu-id="b613c-116">如果沒有指定預設值，則移除所有預設值</span><span class="sxs-lookup"><span data-stu-id="b613c-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="b613c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b613c-117">-PassThru</span></span>
<span data-ttu-id="b613c-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="b613c-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b613c-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b613c-119">-ResourceGroup</span></span>
<span data-ttu-id="b613c-120">清除預設資源群組</span><span class="sxs-lookup"><span data-stu-id="b613c-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b613c-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="b613c-121">-Scope</span></span>
<span data-ttu-id="b613c-122">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="b613c-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b613c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b613c-123">-Confirm</span></span>
<span data-ttu-id="b613c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b613c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b613c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b613c-125">-WhatIf</span></span>
<span data-ttu-id="b613c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b613c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b613c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b613c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b613c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b613c-128">CommonParameters</span></span>
<span data-ttu-id="b613c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b613c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b613c-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b613c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b613c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b613c-131">INPUTS</span></span>

### <span data-ttu-id="b613c-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b613c-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b613c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b613c-133">OUTPUTS</span></span>

### <span data-ttu-id="b613c-134">System.object</span><span class="sxs-lookup"><span data-stu-id="b613c-134">System.Boolean</span></span>

## <span data-ttu-id="b613c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="b613c-135">NOTES</span></span>

## <span data-ttu-id="b613c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="b613c-136">RELATED LINKS</span></span>
