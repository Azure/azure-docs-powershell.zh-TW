---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: 47d384c6ca55fb428922dc3d9e59de84aa0db166
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444035"
---
# <span data-ttu-id="68f40-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="68f40-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="68f40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68f40-102">SYNOPSIS</span></span>
<span data-ttu-id="68f40-103">修改自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="68f40-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68f40-104">句法</span><span class="sxs-lookup"><span data-stu-id="68f40-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68f40-105">說明</span><span class="sxs-lookup"><span data-stu-id="68f40-105">DESCRIPTION</span></span>
<span data-ttu-id="68f40-106">**AzureRmAutomationWebhook** Cmdlet 會修改 Azure 自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="68f40-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="68f40-107">示例</span><span class="sxs-lookup"><span data-stu-id="68f40-107">EXAMPLES</span></span>

### <span data-ttu-id="68f40-108">範例1：停用 webhook</span><span class="sxs-lookup"><span data-stu-id="68f40-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="68f40-109">這個命令會在名為 AutomationAccount01 的自動化帳戶中，停用一個名為 Webhook01 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="68f40-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="68f40-110">參數</span><span class="sxs-lookup"><span data-stu-id="68f40-110">PARAMETERS</span></span>

### <span data-ttu-id="68f40-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="68f40-111">-AutomationAccountName</span></span>
<span data-ttu-id="68f40-112">指定此 Cmdlet 修改 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="68f40-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="68f40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f40-113">-DefaultProfile</span></span>
<span data-ttu-id="68f40-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="68f40-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68f40-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="68f40-115">-IsEnabled</span></span>
<span data-ttu-id="68f40-116">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="68f40-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="68f40-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="68f40-117">-Name</span></span>
<span data-ttu-id="68f40-118">指定此 Cmdlet 所修改之 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f40-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="68f40-119">-參數</span><span class="sxs-lookup"><span data-stu-id="68f40-119">-Parameters</span></span>
<span data-ttu-id="68f40-120">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="68f40-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="68f40-121">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="68f40-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="68f40-122">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="68f40-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="68f40-123">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="68f40-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="68f40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f40-124">-ResourceGroupName</span></span>
<span data-ttu-id="68f40-125">指定此 Cmdlet 修改 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68f40-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="68f40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f40-126">CommonParameters</span></span>
<span data-ttu-id="68f40-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68f40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f40-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68f40-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f40-129">輸入</span><span class="sxs-lookup"><span data-stu-id="68f40-129">INPUTS</span></span>

### <span data-ttu-id="68f40-130">System.object</span><span class="sxs-lookup"><span data-stu-id="68f40-130">System.String</span></span>

### <span data-ttu-id="68f40-131">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="68f40-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="68f40-132">System.object</span><span class="sxs-lookup"><span data-stu-id="68f40-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="68f40-133">輸出</span><span class="sxs-lookup"><span data-stu-id="68f40-133">OUTPUTS</span></span>

### <span data-ttu-id="68f40-134">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="68f40-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="68f40-135">筆記</span><span class="sxs-lookup"><span data-stu-id="68f40-135">NOTES</span></span>

## <span data-ttu-id="68f40-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="68f40-136">RELATED LINKS</span></span>

[<span data-ttu-id="68f40-137">AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="68f40-137">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="68f40-138">新-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="68f40-138">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="68f40-139">移除-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="68f40-139">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


