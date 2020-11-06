---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 5f3ba7d2bdc573e7a08976e575e86dcf05ae3400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613687"
---
# <span data-ttu-id="0953a-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0953a-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="0953a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0953a-102">SYNOPSIS</span></span>
<span data-ttu-id="0953a-103">從自動化 runbook 移除 webhook。</span><span class="sxs-lookup"><span data-stu-id="0953a-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="0953a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0953a-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0953a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0953a-105">DESCRIPTION</span></span>
<span data-ttu-id="0953a-106">**AzAutomationWebhook** Cmdlet 會從 Azure 自動化 runbook 中移除 webhook。</span><span class="sxs-lookup"><span data-stu-id="0953a-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="0953a-107">已刪除 webhook。</span><span class="sxs-lookup"><span data-stu-id="0953a-107">The webhook is deleted.</span></span>

## <span data-ttu-id="0953a-108">示例</span><span class="sxs-lookup"><span data-stu-id="0953a-108">EXAMPLES</span></span>

### <span data-ttu-id="0953a-109">範例1：移除 webhook</span><span class="sxs-lookup"><span data-stu-id="0953a-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="0953a-110">這個命令會在名為 AutomationAccount01 的自動化帳戶中，移除一個名為 Webhook11 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="0953a-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="0953a-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="0953a-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0953a-112">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0953a-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0953a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0953a-113">PARAMETERS</span></span>

### <span data-ttu-id="0953a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0953a-114">-AutomationAccountName</span></span>
<span data-ttu-id="0953a-115">指定此 Cmdlet 移除 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0953a-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="0953a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0953a-116">-DefaultProfile</span></span>
<span data-ttu-id="0953a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0953a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0953a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0953a-118">-Name</span></span>
<span data-ttu-id="0953a-119">指定此 Cmdlet 移除的 webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="0953a-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0953a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0953a-120">-ResourceGroupName</span></span>
<span data-ttu-id="0953a-121">指定此 Cmdlet 移除 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0953a-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="0953a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="0953a-122">-Confirm</span></span>
<span data-ttu-id="0953a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0953a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0953a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0953a-124">-WhatIf</span></span>
<span data-ttu-id="0953a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0953a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0953a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0953a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0953a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0953a-127">CommonParameters</span></span>
<span data-ttu-id="0953a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0953a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0953a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0953a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0953a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0953a-130">INPUTS</span></span>

### <span data-ttu-id="0953a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="0953a-131">System.String</span></span>

## <span data-ttu-id="0953a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0953a-132">OUTPUTS</span></span>

### <span data-ttu-id="0953a-133">System.void</span><span class="sxs-lookup"><span data-stu-id="0953a-133">System.Void</span></span>

## <span data-ttu-id="0953a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0953a-134">NOTES</span></span>

## <span data-ttu-id="0953a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0953a-135">RELATED LINKS</span></span>

[<span data-ttu-id="0953a-136">AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0953a-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="0953a-137">新-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0953a-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="0953a-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0953a-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


