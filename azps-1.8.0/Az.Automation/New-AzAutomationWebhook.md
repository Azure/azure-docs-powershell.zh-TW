---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 94bc498caa5052df5aa9a9e7724ecb87d253d9f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622998"
---
# <span data-ttu-id="16f23-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="16f23-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="16f23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16f23-102">SYNOPSIS</span></span>
<span data-ttu-id="16f23-103">為自動化 runbook 建立 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="16f23-104">句法</span><span class="sxs-lookup"><span data-stu-id="16f23-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16f23-105">說明</span><span class="sxs-lookup"><span data-stu-id="16f23-105">DESCRIPTION</span></span>
<span data-ttu-id="16f23-106">**新的-AzAutomationWebhook** Cmdlet 會為 Azure 自動化 runbook 建立 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="16f23-107">請務必儲存此 Cmdlet 傳回的 webhook URL，因為無法再次檢索它。</span><span class="sxs-lookup"><span data-stu-id="16f23-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="16f23-108">示例</span><span class="sxs-lookup"><span data-stu-id="16f23-108">EXAMPLES</span></span>

### <span data-ttu-id="16f23-109">範例1：建立 webhook</span><span class="sxs-lookup"><span data-stu-id="16f23-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="16f23-110">這個命令會針對自動化帳戶（名為 AutomationAccount01）中名為 ContosoRunbook 的 runbook，建立一個名為 Webhook06 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="16f23-111">該命令會將 webhook 儲存在 $Webhook 變數中。</span><span class="sxs-lookup"><span data-stu-id="16f23-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="16f23-112">已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-112">The webhook is enabled.</span></span>
<span data-ttu-id="16f23-113">Webhook 會在指定的時間到期。</span><span class="sxs-lookup"><span data-stu-id="16f23-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="16f23-114">這個命令不會提供 webhook 參數的任何值。</span><span class="sxs-lookup"><span data-stu-id="16f23-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="16f23-115">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="16f23-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="16f23-116">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16f23-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="16f23-117">範例2：使用參數建立 webhook</span><span class="sxs-lookup"><span data-stu-id="16f23-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="16f23-118">第一個命令會建立參數字典，並將它們儲存在 $Params 變數中。</span><span class="sxs-lookup"><span data-stu-id="16f23-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="16f23-119">第二個命令會針對自動化帳戶（名為 AutomationAccount01）中名為 ContosoRunbook 的 runbook，建立一個名為 Webhook11 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="16f23-120">命令會將 $Params 中的參數指派給 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="16f23-121">參數</span><span class="sxs-lookup"><span data-stu-id="16f23-121">PARAMETERS</span></span>

### <span data-ttu-id="16f23-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16f23-122">-AutomationAccountName</span></span>
<span data-ttu-id="16f23-123">指定此 Cmdlet 建立 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="16f23-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="16f23-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f23-124">-DefaultProfile</span></span>
<span data-ttu-id="16f23-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="16f23-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16f23-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="16f23-126">-ExpiryTime</span></span>
<span data-ttu-id="16f23-127">將 webhook 的到期時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="16f23-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="16f23-128">您可以指定可轉換成有效 **DateTimeOffset** 的字串或 **日期時間** 。</span><span class="sxs-lookup"><span data-stu-id="16f23-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f23-129">-Force</span><span class="sxs-lookup"><span data-stu-id="16f23-129">-Force</span></span>
<span data-ttu-id="16f23-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="16f23-130">ps_force</span></span>

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

### <span data-ttu-id="16f23-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="16f23-131">-IsEnabled</span></span>
<span data-ttu-id="16f23-132">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="16f23-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f23-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="16f23-133">-Name</span></span>
<span data-ttu-id="16f23-134">指定 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="16f23-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="16f23-135">-參數</span><span class="sxs-lookup"><span data-stu-id="16f23-135">-Parameters</span></span>
<span data-ttu-id="16f23-136">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="16f23-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="16f23-137">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="16f23-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="16f23-138">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="16f23-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="16f23-139">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="16f23-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f23-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f23-140">-ResourceGroupName</span></span>
<span data-ttu-id="16f23-141">指定此 Cmdlet 建立 webhook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16f23-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="16f23-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="16f23-142">-RunbookName</span></span>
<span data-ttu-id="16f23-143">指定要與 webhook 相關聯的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="16f23-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16f23-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="16f23-144">-RunOn</span></span>
<span data-ttu-id="16f23-145">應執行 runbook 之混合式輔助角色群組的選用名稱</span><span class="sxs-lookup"><span data-stu-id="16f23-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="16f23-146">-確認</span><span class="sxs-lookup"><span data-stu-id="16f23-146">-Confirm</span></span>
<span data-ttu-id="16f23-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="16f23-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f23-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f23-148">-WhatIf</span></span>
<span data-ttu-id="16f23-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="16f23-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f23-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="16f23-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f23-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f23-151">CommonParameters</span></span>
<span data-ttu-id="16f23-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16f23-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f23-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16f23-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f23-154">輸入</span><span class="sxs-lookup"><span data-stu-id="16f23-154">INPUTS</span></span>

### <span data-ttu-id="16f23-155">System.object</span><span class="sxs-lookup"><span data-stu-id="16f23-155">System.String</span></span>

### <span data-ttu-id="16f23-156">System.object</span><span class="sxs-lookup"><span data-stu-id="16f23-156">System.Boolean</span></span>

### <span data-ttu-id="16f23-157">System.object</span><span class="sxs-lookup"><span data-stu-id="16f23-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="16f23-158">輸出</span><span class="sxs-lookup"><span data-stu-id="16f23-158">OUTPUTS</span></span>

### <span data-ttu-id="16f23-159">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="16f23-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="16f23-160">筆記</span><span class="sxs-lookup"><span data-stu-id="16f23-160">NOTES</span></span>

## <span data-ttu-id="16f23-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="16f23-161">RELATED LINKS</span></span>

[<span data-ttu-id="16f23-162">AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="16f23-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="16f23-163">移除-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="16f23-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="16f23-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="16f23-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


