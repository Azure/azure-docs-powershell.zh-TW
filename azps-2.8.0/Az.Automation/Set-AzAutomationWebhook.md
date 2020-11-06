---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613666"
---
# <span data-ttu-id="72bd9-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="72bd9-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="72bd9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="72bd9-103">修改自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="72bd9-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="72bd9-104">句法</span><span class="sxs-lookup"><span data-stu-id="72bd9-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72bd9-105">說明</span><span class="sxs-lookup"><span data-stu-id="72bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="72bd9-106">**AzAutomationWebhook** Cmdlet 會修改 Azure 自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="72bd9-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="72bd9-107">示例</span><span class="sxs-lookup"><span data-stu-id="72bd9-107">EXAMPLES</span></span>

### <span data-ttu-id="72bd9-108">範例1：停用 webhook</span><span class="sxs-lookup"><span data-stu-id="72bd9-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="72bd9-109">這個命令會在名為 AutomationAccount01 的自動化帳戶中，停用一個名為 Webhook01 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="72bd9-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="72bd9-110">參數</span><span class="sxs-lookup"><span data-stu-id="72bd9-110">PARAMETERS</span></span>

### <span data-ttu-id="72bd9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72bd9-111">-AutomationAccountName</span></span>
<span data-ttu-id="72bd9-112">指定此 Cmdlet 修改 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="72bd9-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="72bd9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bd9-113">-DefaultProfile</span></span>
<span data-ttu-id="72bd9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="72bd9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72bd9-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="72bd9-115">-IsEnabled</span></span>
<span data-ttu-id="72bd9-116">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="72bd9-116">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72bd9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="72bd9-117">-Name</span></span>
<span data-ttu-id="72bd9-118">指定此 Cmdlet 所修改之 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="72bd9-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="72bd9-119">-參數</span><span class="sxs-lookup"><span data-stu-id="72bd9-119">-Parameters</span></span>
<span data-ttu-id="72bd9-120">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="72bd9-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="72bd9-121">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="72bd9-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="72bd9-122">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="72bd9-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="72bd9-123">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="72bd9-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72bd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72bd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="72bd9-125">指定此 Cmdlet 修改 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="72bd9-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="72bd9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bd9-126">CommonParameters</span></span>
<span data-ttu-id="72bd9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72bd9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bd9-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72bd9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bd9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="72bd9-129">INPUTS</span></span>

### <span data-ttu-id="72bd9-130">System.object</span><span class="sxs-lookup"><span data-stu-id="72bd9-130">System.String</span></span>

### <span data-ttu-id="72bd9-131">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="72bd9-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="72bd9-132">System.object</span><span class="sxs-lookup"><span data-stu-id="72bd9-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="72bd9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="72bd9-133">OUTPUTS</span></span>

### <span data-ttu-id="72bd9-134">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="72bd9-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="72bd9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="72bd9-135">NOTES</span></span>

## <span data-ttu-id="72bd9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="72bd9-136">RELATED LINKS</span></span>

[<span data-ttu-id="72bd9-137">AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="72bd9-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="72bd9-138">新-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="72bd9-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="72bd9-139">移除-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="72bd9-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


