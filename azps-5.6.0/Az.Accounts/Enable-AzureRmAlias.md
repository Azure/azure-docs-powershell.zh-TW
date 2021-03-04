---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: e99d7643fe67d4102e9f4eef7f9c10f131594948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916448"
---
# <span data-ttu-id="ba2fc-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ba2fc-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="ba2fc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2fc-103">啟用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="ba2fc-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba2fc-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba2fc-105">描述</span><span class="sxs-lookup"><span data-stu-id="ba2fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ba2fc-106">啟用 Az 模組的 AzureRm 首碼別名。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="ba2fc-107">如果指定 -Module，則只有列出的模組會啟用別名。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="ba2fc-108">否則會啟用所有 AzureRm 別名。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="ba2fc-109">例子</span><span class="sxs-lookup"><span data-stu-id="ba2fc-109">EXAMPLES</span></span>

### <span data-ttu-id="ba2fc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ba2fc-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="ba2fc-111">啟用目前 PowerShell 會話的所有 AzureRm 首碼。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="ba2fc-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="ba2fc-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="ba2fc-113">針對目前程式與目前使用者啟用 Az.Accounts 模組的 AzureRm 別名。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="ba2fc-114">參數</span><span class="sxs-lookup"><span data-stu-id="ba2fc-114">PARAMETERS</span></span>

### <span data-ttu-id="ba2fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2fc-115">-DefaultProfile</span></span>
<span data-ttu-id="ba2fc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba2fc-117">-模組</span><span class="sxs-lookup"><span data-stu-id="ba2fc-117">-Module</span></span>
<span data-ttu-id="ba2fc-118">指出要啟用別名的模組。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="ba2fc-119">如果沒有指定，預設值為所有模組。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="ba2fc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba2fc-120">-PassThru</span></span>
<span data-ttu-id="ba2fc-121">如果指定，Cmdlet 會返回啟用的所有別名</span><span class="sxs-lookup"><span data-stu-id="ba2fc-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="ba2fc-122">-範圍</span><span class="sxs-lookup"><span data-stu-id="ba2fc-122">-Scope</span></span>
<span data-ttu-id="ba2fc-123">指出應該啟用哪些範圍別名。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="ba2fc-124">預設值為 "Local"</span><span class="sxs-lookup"><span data-stu-id="ba2fc-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="ba2fc-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ba2fc-125">-Confirm</span></span>
<span data-ttu-id="ba2fc-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba2fc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba2fc-127">-WhatIf</span></span>
<span data-ttu-id="ba2fc-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba2fc-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba2fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2fc-130">CommonParameters</span></span>
<span data-ttu-id="ba2fc-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba2fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2fc-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba2fc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2fc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ba2fc-133">INPUTS</span></span>

### <span data-ttu-id="ba2fc-134">沒有</span><span class="sxs-lookup"><span data-stu-id="ba2fc-134">None</span></span>

## <span data-ttu-id="ba2fc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ba2fc-135">OUTPUTS</span></span>

### <span data-ttu-id="ba2fc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ba2fc-136">System.String</span></span>

## <span data-ttu-id="ba2fc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ba2fc-137">NOTES</span></span>

## <span data-ttu-id="ba2fc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba2fc-138">RELATED LINKS</span></span>
