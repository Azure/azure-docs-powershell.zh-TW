---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276292"
---
# <span data-ttu-id="99feb-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="99feb-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="99feb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99feb-102">SYNOPSIS</span></span>
<span data-ttu-id="99feb-103">啟用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="99feb-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="99feb-104">句法</span><span class="sxs-lookup"><span data-stu-id="99feb-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99feb-105">說明</span><span class="sxs-lookup"><span data-stu-id="99feb-105">DESCRIPTION</span></span>
<span data-ttu-id="99feb-106">啟用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="99feb-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="99feb-107">如果指定了-Module，則只有列出的模組才會啟用別名。</span><span class="sxs-lookup"><span data-stu-id="99feb-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="99feb-108">否則，所有的 AzureRm 別名都是啟用的。</span><span class="sxs-lookup"><span data-stu-id="99feb-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="99feb-109">示例</span><span class="sxs-lookup"><span data-stu-id="99feb-109">EXAMPLES</span></span>

### <span data-ttu-id="99feb-110">範例1</span><span class="sxs-lookup"><span data-stu-id="99feb-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="99feb-111">啟用目前 PowerShell 會話的所有 AzureRm 首碼。</span><span class="sxs-lookup"><span data-stu-id="99feb-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="99feb-112">範例2</span><span class="sxs-lookup"><span data-stu-id="99feb-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="99feb-113">針對目前的程式和目前的使用者，啟用 Az 的 AzureRm 別名。</span><span class="sxs-lookup"><span data-stu-id="99feb-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="99feb-114">參數</span><span class="sxs-lookup"><span data-stu-id="99feb-114">PARAMETERS</span></span>

### <span data-ttu-id="99feb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99feb-115">-DefaultProfile</span></span>
<span data-ttu-id="99feb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99feb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99feb-117">-模組</span><span class="sxs-lookup"><span data-stu-id="99feb-117">-Module</span></span>
<span data-ttu-id="99feb-118">指示要啟用別名的模組。</span><span class="sxs-lookup"><span data-stu-id="99feb-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="99feb-119">如果沒有指定，則預設值為 [所有模組]。</span><span class="sxs-lookup"><span data-stu-id="99feb-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="99feb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99feb-120">-PassThru</span></span>
<span data-ttu-id="99feb-121">如果已指定，Cmdlet 會傳回所有啟用的別名</span><span class="sxs-lookup"><span data-stu-id="99feb-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="99feb-122">-範圍</span><span class="sxs-lookup"><span data-stu-id="99feb-122">-Scope</span></span>
<span data-ttu-id="99feb-123">指出應該啟用何種範圍的別名。</span><span class="sxs-lookup"><span data-stu-id="99feb-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="99feb-124">預設值為「本機」</span><span class="sxs-lookup"><span data-stu-id="99feb-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99feb-125">-確認</span><span class="sxs-lookup"><span data-stu-id="99feb-125">-Confirm</span></span>
<span data-ttu-id="99feb-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99feb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99feb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99feb-127">-WhatIf</span></span>
<span data-ttu-id="99feb-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99feb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99feb-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99feb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99feb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99feb-130">CommonParameters</span></span>
<span data-ttu-id="99feb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99feb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99feb-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99feb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99feb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="99feb-133">INPUTS</span></span>

### <span data-ttu-id="99feb-134">所有</span><span class="sxs-lookup"><span data-stu-id="99feb-134">None</span></span>

## <span data-ttu-id="99feb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="99feb-135">OUTPUTS</span></span>

### <span data-ttu-id="99feb-136">System.object</span><span class="sxs-lookup"><span data-stu-id="99feb-136">System.String</span></span>

## <span data-ttu-id="99feb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="99feb-137">NOTES</span></span>

## <span data-ttu-id="99feb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="99feb-138">RELATED LINKS</span></span>
