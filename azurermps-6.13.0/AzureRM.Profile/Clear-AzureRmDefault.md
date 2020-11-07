---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: a29bf86b4104fb9a3936daad055da0eab4368690
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626050"
---
# <span data-ttu-id="eea84-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="eea84-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="eea84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eea84-102">SYNOPSIS</span></span>
<span data-ttu-id="eea84-103">清除目前內容中由使用者設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="eea84-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eea84-104">句法</span><span class="sxs-lookup"><span data-stu-id="eea84-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea84-105">說明</span><span class="sxs-lookup"><span data-stu-id="eea84-105">DESCRIPTION</span></span>
<span data-ttu-id="eea84-106">Clear-AzureRmDefault Cmdlet 會根據使用者指定的切換參數，移除使用者所設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="eea84-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="eea84-107">示例</span><span class="sxs-lookup"><span data-stu-id="eea84-107">EXAMPLES</span></span>

### <span data-ttu-id="eea84-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eea84-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="eea84-109">這個命令會移除使用者在目前內容中設定的所有預設值。</span><span class="sxs-lookup"><span data-stu-id="eea84-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="eea84-110">範例1</span><span class="sxs-lookup"><span data-stu-id="eea84-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="eea84-111">這個命令會移除目前內容中由使用者所設定的預設資源群組。</span><span class="sxs-lookup"><span data-stu-id="eea84-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="eea84-112">參數</span><span class="sxs-lookup"><span data-stu-id="eea84-112">PARAMETERS</span></span>

### <span data-ttu-id="eea84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea84-113">-DefaultProfile</span></span>
<span data-ttu-id="eea84-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eea84-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eea84-115">-Force</span></span>
<span data-ttu-id="eea84-116">如果沒有指定預設值，則移除所有預設值</span><span class="sxs-lookup"><span data-stu-id="eea84-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="eea84-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eea84-117">-PassThru</span></span>
<span data-ttu-id="eea84-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="eea84-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eea84-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eea84-119">-ResourceGroup</span></span>
<span data-ttu-id="eea84-120">清除預設資源群組</span><span class="sxs-lookup"><span data-stu-id="eea84-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="eea84-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="eea84-121">-Scope</span></span>
<span data-ttu-id="eea84-122">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="eea84-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="eea84-123">-確認</span><span class="sxs-lookup"><span data-stu-id="eea84-123">-Confirm</span></span>
<span data-ttu-id="eea84-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eea84-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea84-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea84-125">-WhatIf</span></span>
<span data-ttu-id="eea84-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eea84-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eea84-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eea84-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea84-128">CommonParameters</span></span>
<span data-ttu-id="eea84-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eea84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea84-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eea84-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea84-131">輸入</span><span class="sxs-lookup"><span data-stu-id="eea84-131">INPUTS</span></span>

### <span data-ttu-id="eea84-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="eea84-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eea84-133">輸出</span><span class="sxs-lookup"><span data-stu-id="eea84-133">OUTPUTS</span></span>

### <span data-ttu-id="eea84-134">System.object</span><span class="sxs-lookup"><span data-stu-id="eea84-134">System.Boolean</span></span>

## <span data-ttu-id="eea84-135">筆記</span><span class="sxs-lookup"><span data-stu-id="eea84-135">NOTES</span></span>

## <span data-ttu-id="eea84-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="eea84-136">RELATED LINKS</span></span>
