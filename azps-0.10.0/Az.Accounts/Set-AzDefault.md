---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 8abb473eb5def0d2ca360e0b6116069aecc21b16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794106"
---
# <span data-ttu-id="67ba5-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="67ba5-101">Set-AzDefault</span></span>

## <span data-ttu-id="67ba5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="67ba5-103">在目前的內容中設定預設值</span><span class="sxs-lookup"><span data-stu-id="67ba5-103">Sets a default in the current context</span></span>

## <span data-ttu-id="67ba5-104">句法</span><span class="sxs-lookup"><span data-stu-id="67ba5-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ba5-105">說明</span><span class="sxs-lookup"><span data-stu-id="67ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="67ba5-106">Set-AzDefault Cmdlet 會在目前的內容中新增或變更預設值。</span><span class="sxs-lookup"><span data-stu-id="67ba5-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="67ba5-107">示例</span><span class="sxs-lookup"><span data-stu-id="67ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="67ba5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="67ba5-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="67ba5-109">這個命令會將預設資源群組設定為使用者指定的資源群組。</span><span class="sxs-lookup"><span data-stu-id="67ba5-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="67ba5-110">參數</span><span class="sxs-lookup"><span data-stu-id="67ba5-110">PARAMETERS</span></span>

### <span data-ttu-id="67ba5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ba5-111">-DefaultProfile</span></span>
<span data-ttu-id="67ba5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67ba5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67ba5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="67ba5-113">-Force</span></span>
<span data-ttu-id="67ba5-114">如果指定的預設值不存在，請建立新的資源群組</span><span class="sxs-lookup"><span data-stu-id="67ba5-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="67ba5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ba5-115">-ResourceGroupName</span></span>
<span data-ttu-id="67ba5-116">設為預設值的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="67ba5-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="67ba5-117">-範圍</span><span class="sxs-lookup"><span data-stu-id="67ba5-117">-Scope</span></span>
<span data-ttu-id="67ba5-118">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="67ba5-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="67ba5-119">-確認</span><span class="sxs-lookup"><span data-stu-id="67ba5-119">-Confirm</span></span>
<span data-ttu-id="67ba5-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67ba5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ba5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ba5-121">-WhatIf</span></span>
<span data-ttu-id="67ba5-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67ba5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ba5-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67ba5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ba5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ba5-124">CommonParameters</span></span>
<span data-ttu-id="67ba5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67ba5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ba5-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67ba5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ba5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="67ba5-127">INPUTS</span></span>

### <span data-ttu-id="67ba5-128">System.object</span><span class="sxs-lookup"><span data-stu-id="67ba5-128">System.String</span></span>

## <span data-ttu-id="67ba5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="67ba5-129">OUTPUTS</span></span>

### <span data-ttu-id="67ba5-130">PSResourceGroup 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="67ba5-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="67ba5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="67ba5-131">NOTES</span></span>

## <span data-ttu-id="67ba5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="67ba5-132">RELATED LINKS</span></span>
