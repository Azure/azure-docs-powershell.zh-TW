---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 749507ba0bc0eec8aac7600c5262533ceb02a46b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283532"
---
# <span data-ttu-id="4e4ff-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4e4ff-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="4e4ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4ff-103">針對 Az 模組停用 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="4e4ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e4ff-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e4ff-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4ff-106">針對 Az 模組停用 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="4e4ff-107">如果指定了-Module，則只有列出的模組才會停用別名。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="4e4ff-108">否則，系統會停用所有 AzureRm 的別名。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="4e4ff-109">示例</span><span class="sxs-lookup"><span data-stu-id="4e4ff-109">EXAMPLES</span></span>

### <span data-ttu-id="4e4ff-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4e4ff-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="4e4ff-111">針對目前的 PowerShell 會話停用所有 AzureRm 首碼。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="4e4ff-112">範例1</span><span class="sxs-lookup"><span data-stu-id="4e4ff-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="4e4ff-113">針對目前的程式和目前的使用者，停用 [Az] 模組的 AzureRm 別名。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="4e4ff-114">參數</span><span class="sxs-lookup"><span data-stu-id="4e4ff-114">PARAMETERS</span></span>

### <span data-ttu-id="4e4ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4ff-115">-DefaultProfile</span></span>
<span data-ttu-id="4e4ff-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4ff-117">-模組</span><span class="sxs-lookup"><span data-stu-id="4e4ff-117">-Module</span></span>
<span data-ttu-id="4e4ff-118">指示要停用別名的模組。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="4e4ff-119">如果沒有指定，則預設值為所有啟用的模組。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="4e4ff-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e4ff-120">-PassThru</span></span>
<span data-ttu-id="4e4ff-121">如果已指定，Cmdlet 會傳回所有停用的別名</span><span class="sxs-lookup"><span data-stu-id="4e4ff-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="4e4ff-122">-範圍</span><span class="sxs-lookup"><span data-stu-id="4e4ff-122">-Scope</span></span>
<span data-ttu-id="4e4ff-123">指出應該停用哪些範圍的別名。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="4e4ff-124">預設值為 "Process"</span><span class="sxs-lookup"><span data-stu-id="4e4ff-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="4e4ff-125">-確認</span><span class="sxs-lookup"><span data-stu-id="4e4ff-125">-Confirm</span></span>
<span data-ttu-id="4e4ff-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4ff-127">-WhatIf</span></span>
<span data-ttu-id="4e4ff-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4ff-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4ff-130">CommonParameters</span></span>
<span data-ttu-id="4e4ff-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4ff-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e4ff-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4ff-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4e4ff-133">INPUTS</span></span>

### <span data-ttu-id="4e4ff-134">所有</span><span class="sxs-lookup"><span data-stu-id="4e4ff-134">None</span></span>

## <span data-ttu-id="4e4ff-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4e4ff-135">OUTPUTS</span></span>

### <span data-ttu-id="4e4ff-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4e4ff-136">System.String</span></span>

## <span data-ttu-id="4e4ff-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4e4ff-137">NOTES</span></span>

## <span data-ttu-id="4e4ff-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e4ff-138">RELATED LINKS</span></span>
