---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447182"
---
# <span data-ttu-id="1e4c8-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4c8-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="1e4c8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4c8-103">修改自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e4c8-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e4c8-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e4c8-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e4c8-105">DESCRIPTION</span></span>
<span data-ttu-id="1e4c8-106">**AzureRmAutomationWebhook** Cmdlet 會修改 Azure 自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="1e4c8-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e4c8-107">EXAMPLES</span></span>

### <span data-ttu-id="1e4c8-108">範例1：停用 webhook</span><span class="sxs-lookup"><span data-stu-id="1e4c8-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="1e4c8-109">這個命令會在名為 AutomationAccount01 的自動化帳戶中，停用一個名為 Webhook01 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="1e4c8-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e4c8-110">PARAMETERS</span></span>

### <span data-ttu-id="1e4c8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e4c8-111">-AutomationAccountName</span></span>
<span data-ttu-id="1e4c8-112">指定此 Cmdlet 修改 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="1e4c8-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="1e4c8-113">-IsEnabled</span></span>
<span data-ttu-id="1e4c8-114">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-114">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="1e4c8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e4c8-115">-Name</span></span>
<span data-ttu-id="1e4c8-116">指定此 Cmdlet 所修改之 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1e4c8-117">-參數</span><span class="sxs-lookup"><span data-stu-id="1e4c8-117">-Parameters</span></span>
<span data-ttu-id="1e4c8-118">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="1e4c8-119">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="1e4c8-120">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="1e4c8-121">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="1e4c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e4c8-123">指定此 Cmdlet 修改 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="1e4c8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4c8-124">-DefaultProfile</span></span>
<span data-ttu-id="1e4c8-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e4c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4c8-126">CommonParameters</span></span>
<span data-ttu-id="1e4c8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4c8-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4c8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1e4c8-129">INPUTS</span></span>

## <span data-ttu-id="1e4c8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1e4c8-130">OUTPUTS</span></span>

### <span data-ttu-id="1e4c8-131">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="1e4c8-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="1e4c8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1e4c8-132">NOTES</span></span>

## <span data-ttu-id="1e4c8-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e4c8-133">RELATED LINKS</span></span>

[<span data-ttu-id="1e4c8-134">AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4c8-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="1e4c8-135">新-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4c8-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="1e4c8-136">移除-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4c8-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


