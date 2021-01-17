---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447091"
---
# <span data-ttu-id="a9ee3-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9ee3-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="a9ee3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9ee3-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ee3-103">修改自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="a9ee3-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9ee3-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9ee3-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9ee3-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ee3-106">**AzAutomationWebhook** Cmdlet 會修改 Azure 自動化 runbook 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="a9ee3-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9ee3-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ee3-108">範例1：停用 webhook</span><span class="sxs-lookup"><span data-stu-id="a9ee3-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="a9ee3-109">這個命令會在名為 AutomationAccount01 的自動化帳戶中，停用一個名為 Webhook01 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="a9ee3-110">範例2</span><span class="sxs-lookup"><span data-stu-id="a9ee3-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="a9ee3-111">這個命令會設定 webhook 的 [執行物件] 值，並強制在名為 Windows 的混合式輔助角色群組上執行 runbook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="a9ee3-112">範例3</span><span class="sxs-lookup"><span data-stu-id="a9ee3-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="a9ee3-113">這個命令會更新 webhook 的 [執行物件] 值，並強制在 Azure runbook worker 上執行 runbook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="a9ee3-114">參數</span><span class="sxs-lookup"><span data-stu-id="a9ee3-114">PARAMETERS</span></span>

### <span data-ttu-id="a9ee3-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9ee3-115">-AutomationAccountName</span></span>
<span data-ttu-id="a9ee3-116">指定此 Cmdlet 修改 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="a9ee3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ee3-117">-DefaultProfile</span></span>
<span data-ttu-id="a9ee3-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a9ee3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9ee3-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a9ee3-119">-IsEnabled</span></span>
<span data-ttu-id="a9ee3-120">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="a9ee3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9ee3-121">-Name</span></span>
<span data-ttu-id="a9ee3-122">指定此 Cmdlet 所修改之 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a9ee3-123">-參數</span><span class="sxs-lookup"><span data-stu-id="a9ee3-123">-Parameters</span></span>
<span data-ttu-id="a9ee3-124">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="a9ee3-125">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="a9ee3-126">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="a9ee3-127">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="a9ee3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ee3-128">-ResourceGroupName</span></span>
<span data-ttu-id="a9ee3-129">指定此 Cmdlet 修改 webhook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="a9ee3-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="a9ee3-130">-RunOn</span></span>
<span data-ttu-id="a9ee3-131">應執行 runbook 之混合式代理程式的選用名稱</span><span class="sxs-lookup"><span data-stu-id="a9ee3-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ee3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ee3-132">CommonParameters</span></span>
<span data-ttu-id="a9ee3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ee3-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ee3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="a9ee3-135">INPUTS</span></span>

### <span data-ttu-id="a9ee3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="a9ee3-136">System.String</span></span>

### <span data-ttu-id="a9ee3-137">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9ee3-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a9ee3-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a9ee3-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="a9ee3-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a9ee3-139">OUTPUTS</span></span>

### <span data-ttu-id="a9ee3-140">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="a9ee3-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a9ee3-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a9ee3-141">NOTES</span></span>

## <span data-ttu-id="a9ee3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9ee3-142">RELATED LINKS</span></span>

[<span data-ttu-id="a9ee3-143">AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9ee3-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="a9ee3-144">新-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9ee3-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="a9ee3-145">移除-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a9ee3-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


