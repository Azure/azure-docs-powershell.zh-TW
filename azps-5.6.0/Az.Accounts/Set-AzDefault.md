---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 98e7877ba075aacc1da00291bb557c2e94e276e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916688"
---
# <span data-ttu-id="951b8-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="951b8-101">Set-AzDefault</span></span>

## <span data-ttu-id="951b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="951b8-102">SYNOPSIS</span></span>
<span data-ttu-id="951b8-103">在目前的情境中設定預設值</span><span class="sxs-lookup"><span data-stu-id="951b8-103">Sets a default in the current context</span></span>

## <span data-ttu-id="951b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="951b8-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="951b8-105">描述</span><span class="sxs-lookup"><span data-stu-id="951b8-105">DESCRIPTION</span></span>
<span data-ttu-id="951b8-106">Cmdlet Set-AzDefault或變更目前內容中的預設值。</span><span class="sxs-lookup"><span data-stu-id="951b8-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="951b8-107">例子</span><span class="sxs-lookup"><span data-stu-id="951b8-107">EXAMPLES</span></span>

### <span data-ttu-id="951b8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="951b8-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="951b8-109">此命令將預設資源群組設定為使用者指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="951b8-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="951b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="951b8-110">PARAMETERS</span></span>

### <span data-ttu-id="951b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951b8-111">-DefaultProfile</span></span>
<span data-ttu-id="951b8-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="951b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="951b8-113">-強制</span><span class="sxs-lookup"><span data-stu-id="951b8-113">-Force</span></span>
<span data-ttu-id="951b8-114">如果指定的預設值不存在，請建立新資源群組</span><span class="sxs-lookup"><span data-stu-id="951b8-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="951b8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951b8-115">-ResourceGroupName</span></span>
<span data-ttu-id="951b8-116">設為預設值的資源組名</span><span class="sxs-lookup"><span data-stu-id="951b8-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="951b8-117">-範圍</span><span class="sxs-lookup"><span data-stu-id="951b8-117">-Scope</span></span>
<span data-ttu-id="951b8-118">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="951b8-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="951b8-119">-確認</span><span class="sxs-lookup"><span data-stu-id="951b8-119">-Confirm</span></span>
<span data-ttu-id="951b8-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="951b8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951b8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951b8-121">-WhatIf</span></span>
<span data-ttu-id="951b8-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="951b8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="951b8-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="951b8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951b8-124">CommonParameters</span></span>
<span data-ttu-id="951b8-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="951b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951b8-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="951b8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951b8-127">輸入</span><span class="sxs-lookup"><span data-stu-id="951b8-127">INPUTS</span></span>

### <span data-ttu-id="951b8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="951b8-128">System.String</span></span>

## <span data-ttu-id="951b8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="951b8-129">OUTPUTS</span></span>

### <span data-ttu-id="951b8-130">Microsoft.Azure.Commands.Profile.models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="951b8-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="951b8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="951b8-131">NOTES</span></span>

## <span data-ttu-id="951b8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="951b8-132">RELATED LINKS</span></span>
