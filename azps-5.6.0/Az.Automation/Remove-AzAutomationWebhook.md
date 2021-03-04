---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 93c370eaefa83c5e1be4692cb41ea0793b8f4681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916656"
---
# <span data-ttu-id="20274-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="20274-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="20274-102">簡介</span><span class="sxs-lookup"><span data-stu-id="20274-102">SYNOPSIS</span></span>
<span data-ttu-id="20274-103">移除自動化 runbook 中的 Web上。</span><span class="sxs-lookup"><span data-stu-id="20274-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="20274-104">語法</span><span class="sxs-lookup"><span data-stu-id="20274-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20274-105">描述</span><span class="sxs-lookup"><span data-stu-id="20274-105">DESCRIPTION</span></span>
<span data-ttu-id="20274-106">**Remove-AzAutomationWebtomation Cmdlet** 會從 Azure 自動化執行手冊移除 Webaz。</span><span class="sxs-lookup"><span data-stu-id="20274-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="20274-107">網頁設計會被刪除。</span><span class="sxs-lookup"><span data-stu-id="20274-107">The webhook is deleted.</span></span>

## <span data-ttu-id="20274-108">例子</span><span class="sxs-lookup"><span data-stu-id="20274-108">EXAMPLES</span></span>

### <span data-ttu-id="20274-109">範例 1：移除網頁</span><span class="sxs-lookup"><span data-stu-id="20274-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="20274-110">此命令會移除自動化帳戶中名為 AutomationAccount01 的 Web一個名為 Web一11 的網頁。</span><span class="sxs-lookup"><span data-stu-id="20274-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="20274-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="20274-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="20274-112">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="20274-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="20274-113">參數</span><span class="sxs-lookup"><span data-stu-id="20274-113">PARAMETERS</span></span>

### <span data-ttu-id="20274-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20274-114">-AutomationAccountName</span></span>
<span data-ttu-id="20274-115">指定自動化帳戶的名稱，此 Cmdlet 會從該帳戶移除網頁。</span><span class="sxs-lookup"><span data-stu-id="20274-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20274-116">-DefaultProfile</span></span>
<span data-ttu-id="20274-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="20274-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20274-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="20274-118">-Name</span></span>
<span data-ttu-id="20274-119">指定此 Cmdlet 移除的網頁網站名稱。</span><span class="sxs-lookup"><span data-stu-id="20274-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20274-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20274-120">-ResourceGroupName</span></span>
<span data-ttu-id="20274-121">指定此 Cmdlet 會移除 Web一個網頁組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="20274-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20274-122">-確認</span><span class="sxs-lookup"><span data-stu-id="20274-122">-Confirm</span></span>
<span data-ttu-id="20274-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="20274-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20274-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20274-124">-WhatIf</span></span>
<span data-ttu-id="20274-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20274-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20274-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20274-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20274-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20274-127">CommonParameters</span></span>
<span data-ttu-id="20274-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="20274-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20274-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="20274-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20274-130">輸入</span><span class="sxs-lookup"><span data-stu-id="20274-130">INPUTS</span></span>

### <span data-ttu-id="20274-131">System.String</span><span class="sxs-lookup"><span data-stu-id="20274-131">System.String</span></span>

## <span data-ttu-id="20274-132">輸出</span><span class="sxs-lookup"><span data-stu-id="20274-132">OUTPUTS</span></span>

### <span data-ttu-id="20274-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="20274-133">System.Void</span></span>

## <span data-ttu-id="20274-134">筆記</span><span class="sxs-lookup"><span data-stu-id="20274-134">NOTES</span></span>

## <span data-ttu-id="20274-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="20274-135">RELATED LINKS</span></span>

[<span data-ttu-id="20274-136">Get-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="20274-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="20274-137">New-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="20274-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="20274-138">Set-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="20274-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


