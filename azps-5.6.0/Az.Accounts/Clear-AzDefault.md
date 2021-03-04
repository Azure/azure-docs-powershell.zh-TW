---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: ac017af710531ff3294f858a8f95ad7529cd1c11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911798"
---
# <span data-ttu-id="cea15-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="cea15-101">Clear-AzDefault</span></span>

## <span data-ttu-id="cea15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cea15-102">SYNOPSIS</span></span>
<span data-ttu-id="cea15-103">清除使用者目前內容中設定的預設設定。</span><span class="sxs-lookup"><span data-stu-id="cea15-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="cea15-104">語法</span><span class="sxs-lookup"><span data-stu-id="cea15-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea15-105">描述</span><span class="sxs-lookup"><span data-stu-id="cea15-105">DESCRIPTION</span></span>
<span data-ttu-id="cea15-106">此Clear-AzDefault Cmdlet 會移除使用者根據使用者指定的參數所設定的預設設定。</span><span class="sxs-lookup"><span data-stu-id="cea15-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="cea15-107">例子</span><span class="sxs-lookup"><span data-stu-id="cea15-107">EXAMPLES</span></span>

### <span data-ttu-id="cea15-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cea15-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="cea15-109">此命令會移除使用者目前內容中設定的所有預設值。</span><span class="sxs-lookup"><span data-stu-id="cea15-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="cea15-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="cea15-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="cea15-111">此命令會移除使用者目前內容中設定的預設資源群組。</span><span class="sxs-lookup"><span data-stu-id="cea15-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="cea15-112">參數</span><span class="sxs-lookup"><span data-stu-id="cea15-112">PARAMETERS</span></span>

### <span data-ttu-id="cea15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea15-113">-DefaultProfile</span></span>
<span data-ttu-id="cea15-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cea15-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea15-115">-強制</span><span class="sxs-lookup"><span data-stu-id="cea15-115">-Force</span></span>
<span data-ttu-id="cea15-116">如果沒有指定預設值，請移除所有預設值</span><span class="sxs-lookup"><span data-stu-id="cea15-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="cea15-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cea15-117">-PassThru</span></span>
<span data-ttu-id="cea15-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cea15-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cea15-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cea15-119">-ResourceGroup</span></span>
<span data-ttu-id="cea15-120">清除預設資源群組</span><span class="sxs-lookup"><span data-stu-id="cea15-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="cea15-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="cea15-121">-Scope</span></span>
<span data-ttu-id="cea15-122">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="cea15-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="cea15-123">-確認</span><span class="sxs-lookup"><span data-stu-id="cea15-123">-Confirm</span></span>
<span data-ttu-id="cea15-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cea15-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea15-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea15-125">-WhatIf</span></span>
<span data-ttu-id="cea15-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cea15-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea15-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cea15-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea15-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea15-128">CommonParameters</span></span>
<span data-ttu-id="cea15-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cea15-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea15-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cea15-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea15-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cea15-131">INPUTS</span></span>

### <span data-ttu-id="cea15-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cea15-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cea15-133">輸出</span><span class="sxs-lookup"><span data-stu-id="cea15-133">OUTPUTS</span></span>

### <span data-ttu-id="cea15-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cea15-134">System.Boolean</span></span>

## <span data-ttu-id="cea15-135">筆記</span><span class="sxs-lookup"><span data-stu-id="cea15-135">NOTES</span></span>

## <span data-ttu-id="cea15-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cea15-136">RELATED LINKS</span></span>
