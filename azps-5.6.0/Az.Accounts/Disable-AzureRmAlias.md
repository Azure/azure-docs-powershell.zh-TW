---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 1f9f17e03a9b3cf79b2764c7711da9eee6ca104d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914217"
---
# <span data-ttu-id="a5062-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a5062-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="a5062-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a5062-102">SYNOPSIS</span></span>
<span data-ttu-id="a5062-103">停用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="a5062-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="a5062-104">語法</span><span class="sxs-lookup"><span data-stu-id="a5062-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5062-105">描述</span><span class="sxs-lookup"><span data-stu-id="a5062-105">DESCRIPTION</span></span>
<span data-ttu-id="a5062-106">停用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="a5062-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="a5062-107">如果指定 -Module，則只有列出的模組會停用別名。</span><span class="sxs-lookup"><span data-stu-id="a5062-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="a5062-108">否則會停用所有 AzureRm 別名。</span><span class="sxs-lookup"><span data-stu-id="a5062-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="a5062-109">例子</span><span class="sxs-lookup"><span data-stu-id="a5062-109">EXAMPLES</span></span>

### <span data-ttu-id="a5062-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5062-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="a5062-111">停用目前 PowerShell 會話的所有 AzureRm 首碼。</span><span class="sxs-lookup"><span data-stu-id="a5062-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="a5062-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="a5062-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="a5062-113">停用目前程式與目前使用者的 Az.Accounts 模組 AzureRm 別名。</span><span class="sxs-lookup"><span data-stu-id="a5062-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="a5062-114">參數</span><span class="sxs-lookup"><span data-stu-id="a5062-114">PARAMETERS</span></span>

### <span data-ttu-id="a5062-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5062-115">-DefaultProfile</span></span>
<span data-ttu-id="a5062-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5062-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5062-117">-模組</span><span class="sxs-lookup"><span data-stu-id="a5062-117">-Module</span></span>
<span data-ttu-id="a5062-118">指出要停用別名的模組。</span><span class="sxs-lookup"><span data-stu-id="a5062-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="a5062-119">如果沒有指定，預設值為所有啟用模組。</span><span class="sxs-lookup"><span data-stu-id="a5062-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5062-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5062-120">-PassThru</span></span>
<span data-ttu-id="a5062-121">如果指定，Cmdlet 會返回所有停用的別名</span><span class="sxs-lookup"><span data-stu-id="a5062-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="a5062-122">-範圍</span><span class="sxs-lookup"><span data-stu-id="a5062-122">-Scope</span></span>
<span data-ttu-id="a5062-123">指出應該停用哪些範圍別名。</span><span class="sxs-lookup"><span data-stu-id="a5062-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="a5062-124">預設值為'程式'</span><span class="sxs-lookup"><span data-stu-id="a5062-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5062-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a5062-125">-Confirm</span></span>
<span data-ttu-id="a5062-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a5062-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5062-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5062-127">-WhatIf</span></span>
<span data-ttu-id="a5062-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5062-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5062-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5062-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5062-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5062-130">CommonParameters</span></span>
<span data-ttu-id="a5062-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a5062-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5062-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5062-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5062-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a5062-133">INPUTS</span></span>

### <span data-ttu-id="a5062-134">沒有</span><span class="sxs-lookup"><span data-stu-id="a5062-134">None</span></span>

## <span data-ttu-id="a5062-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a5062-135">OUTPUTS</span></span>

### <span data-ttu-id="a5062-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a5062-136">System.String</span></span>

## <span data-ttu-id="a5062-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a5062-137">NOTES</span></span>

## <span data-ttu-id="a5062-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5062-138">RELATED LINKS</span></span>
