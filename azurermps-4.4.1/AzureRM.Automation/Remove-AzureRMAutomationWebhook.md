---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: f191176433a5ac12507d2b29a6d52c73a1d61e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450879"
---
# <span data-ttu-id="3374f-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="3374f-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="3374f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3374f-102">SYNOPSIS</span></span>
<span data-ttu-id="3374f-103">從自動化 runbook 移除 webhook。</span><span class="sxs-lookup"><span data-stu-id="3374f-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3374f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3374f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3374f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3374f-105">DESCRIPTION</span></span>
<span data-ttu-id="3374f-106">**AzureRmAutomationWebhook** Cmdlet 會從 Azure 自動化 runbook 中移除 webhook。</span><span class="sxs-lookup"><span data-stu-id="3374f-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="3374f-107">已刪除 webhook。</span><span class="sxs-lookup"><span data-stu-id="3374f-107">The webhook is deleted.</span></span>

## <span data-ttu-id="3374f-108">示例</span><span class="sxs-lookup"><span data-stu-id="3374f-108">EXAMPLES</span></span>

### <span data-ttu-id="3374f-109">範例1：移除 webhook</span><span class="sxs-lookup"><span data-stu-id="3374f-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="3374f-110">這個命令會在名為 AutomationAccount01 的自動化帳戶中，移除一個名為 Webhook11 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="3374f-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="3374f-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="3374f-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3374f-112">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3374f-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3374f-113">參數</span><span class="sxs-lookup"><span data-stu-id="3374f-113">PARAMETERS</span></span>

### <span data-ttu-id="3374f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3374f-114">-AutomationAccountName</span></span>
<span data-ttu-id="3374f-115">指定此 Cmdlet 移除 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3374f-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="3374f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3374f-116">-Name</span></span>
<span data-ttu-id="3374f-117">指定此 Cmdlet 移除的 webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="3374f-117">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3374f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3374f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3374f-119">指定此 Cmdlet 移除 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3374f-119">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="3374f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="3374f-120">-Confirm</span></span>
<span data-ttu-id="3374f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3374f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3374f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3374f-122">-WhatIf</span></span>
<span data-ttu-id="3374f-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3374f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3374f-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3374f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3374f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3374f-125">-DefaultProfile</span></span>
<span data-ttu-id="3374f-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3374f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3374f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3374f-127">CommonParameters</span></span>
<span data-ttu-id="3374f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3374f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3374f-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3374f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3374f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3374f-130">INPUTS</span></span>

## <span data-ttu-id="3374f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3374f-131">OUTPUTS</span></span>

## <span data-ttu-id="3374f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3374f-132">NOTES</span></span>

## <span data-ttu-id="3374f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3374f-133">RELATED LINKS</span></span>

[<span data-ttu-id="3374f-134">AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="3374f-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="3374f-135">新-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="3374f-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="3374f-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="3374f-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


