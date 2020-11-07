---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626558"
---
# <span data-ttu-id="5e0ac-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5e0ac-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="5e0ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0ac-103">從自動化 runbook 移除 webhook。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e0ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e0ac-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e0ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e0ac-105">DESCRIPTION</span></span>
<span data-ttu-id="5e0ac-106">**AzureRmAutomationWebhook** Cmdlet 會從 Azure 自動化 runbook 中移除 webhook。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="5e0ac-107">已刪除 webhook。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-107">The webhook is deleted.</span></span>

## <span data-ttu-id="5e0ac-108">示例</span><span class="sxs-lookup"><span data-stu-id="5e0ac-108">EXAMPLES</span></span>

### <span data-ttu-id="5e0ac-109">範例1：移除 webhook</span><span class="sxs-lookup"><span data-stu-id="5e0ac-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="5e0ac-110">這個命令會在名為 AutomationAccount01 的自動化帳戶中，移除一個名為 Webhook11 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5e0ac-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5e0ac-112">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5e0ac-113">參數</span><span class="sxs-lookup"><span data-stu-id="5e0ac-113">PARAMETERS</span></span>

### <span data-ttu-id="5e0ac-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e0ac-114">-AutomationAccountName</span></span>
<span data-ttu-id="5e0ac-115">指定此 Cmdlet 移除 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0ac-116">-DefaultProfile</span></span>
<span data-ttu-id="5e0ac-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5e0ac-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0ac-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e0ac-118">-Name</span></span>
<span data-ttu-id="5e0ac-119">指定此 Cmdlet 移除的 webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="5e0ac-121">指定此 Cmdlet 移除 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0ac-122">-確認</span><span class="sxs-lookup"><span data-stu-id="5e0ac-122">-Confirm</span></span>
<span data-ttu-id="5e0ac-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0ac-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e0ac-124">-WhatIf</span></span>
<span data-ttu-id="5e0ac-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e0ac-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0ac-127">CommonParameters</span></span>
<span data-ttu-id="5e0ac-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0ac-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0ac-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5e0ac-130">INPUTS</span></span>

### <span data-ttu-id="5e0ac-131">所有</span><span class="sxs-lookup"><span data-stu-id="5e0ac-131">None</span></span>
<span data-ttu-id="5e0ac-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5e0ac-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e0ac-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5e0ac-133">OUTPUTS</span></span>

## <span data-ttu-id="5e0ac-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5e0ac-134">NOTES</span></span>

## <span data-ttu-id="5e0ac-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e0ac-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e0ac-136">AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5e0ac-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="5e0ac-137">新-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5e0ac-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="5e0ac-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5e0ac-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


