---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450907"
---
# <span data-ttu-id="8c4c7-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8c4c7-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="8c4c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4c7-103">為自動化 runbook 建立 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c4c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c4c7-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="8c4c7-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4c7-106">**新的-AzureRmAutomationWebhook** Cmdlet 會為 Azure 自動化 runbook 建立 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="8c4c7-107">請務必儲存此 Cmdlet 傳回的 webhook URL，因為無法再次檢索它。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="8c4c7-108">示例</span><span class="sxs-lookup"><span data-stu-id="8c4c7-108">EXAMPLES</span></span>

### <span data-ttu-id="8c4c7-109">範例1：建立 webhook</span><span class="sxs-lookup"><span data-stu-id="8c4c7-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="8c4c7-110">這個命令會針對自動化帳戶（名為 AutomationAccount01）中名為 ContosoRunbook 的 runbook，建立一個名為 Webhook06 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="8c4c7-111">該命令會將 webhook 儲存在 $Webhook 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="8c4c7-112">已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-112">The webhook is enabled.</span></span>
<span data-ttu-id="8c4c7-113">Webhook 會在指定的時間到期。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="8c4c7-114">這個命令不會提供 webhook 參數的任何值。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="8c4c7-115">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8c4c7-116">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8c4c7-117">範例2：使用參數建立 webhook</span><span class="sxs-lookup"><span data-stu-id="8c4c7-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="8c4c7-118">第一個命令會建立參數字典，並將它們儲存在 $Params 變數中。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="8c4c7-119">第二個命令會針對自動化帳戶（名為 AutomationAccount01）中名為 ContosoRunbook 的 runbook，建立一個名為 Webhook11 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="8c4c7-120">命令會將 $Params 中的參數指派給 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="8c4c7-121">參數</span><span class="sxs-lookup"><span data-stu-id="8c4c7-121">PARAMETERS</span></span>

### <span data-ttu-id="8c4c7-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8c4c7-122">-AutomationAccountName</span></span>
<span data-ttu-id="8c4c7-123">指定此 Cmdlet 建立 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="8c4c7-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8c4c7-124">-ExpiryTime</span></span>
<span data-ttu-id="8c4c7-125">將 webhook 的到期時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="8c4c7-126">您可以指定可轉換成有效 **DateTimeOffset** 的字串或 **日期時間** 。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="8c4c7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="8c4c7-127">-Force</span></span>
<span data-ttu-id="8c4c7-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="8c4c7-128">ps_force</span></span>

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

### <span data-ttu-id="8c4c7-129">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="8c4c7-129">-IsEnabled</span></span>
<span data-ttu-id="8c4c7-130">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-130">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="8c4c7-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c4c7-131">-Name</span></span>
<span data-ttu-id="8c4c7-132">指定 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="8c4c7-133">-參數</span><span class="sxs-lookup"><span data-stu-id="8c4c7-133">-Parameters</span></span>
<span data-ttu-id="8c4c7-134">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="8c4c7-135">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="8c4c7-136">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="8c4c7-137">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="8c4c7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4c7-138">-ResourceGroupName</span></span>
<span data-ttu-id="8c4c7-139">指定此 Cmdlet 建立 webhook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="8c4c7-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8c4c7-140">-RunbookName</span></span>
<span data-ttu-id="8c4c7-141">指定要與 webhook 相關聯的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-141">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="8c4c7-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="8c4c7-142">-RunOn</span></span>
<span data-ttu-id="8c4c7-143">應執行 runbook 之混合式代理程式的選用名稱</span><span class="sxs-lookup"><span data-stu-id="8c4c7-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="8c4c7-144">-確認</span><span class="sxs-lookup"><span data-stu-id="8c4c7-144">-Confirm</span></span>
<span data-ttu-id="8c4c7-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c4c7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4c7-146">-WhatIf</span></span>
<span data-ttu-id="8c4c7-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4c7-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c4c7-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4c7-149">-DefaultProfile</span></span>
<span data-ttu-id="8c4c7-150">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c4c7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4c7-151">CommonParameters</span></span>
<span data-ttu-id="8c4c7-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4c7-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4c7-154">輸入</span><span class="sxs-lookup"><span data-stu-id="8c4c7-154">INPUTS</span></span>

## <span data-ttu-id="8c4c7-155">輸出</span><span class="sxs-lookup"><span data-stu-id="8c4c7-155">OUTPUTS</span></span>

### <span data-ttu-id="8c4c7-156">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="8c4c7-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="8c4c7-157">筆記</span><span class="sxs-lookup"><span data-stu-id="8c4c7-157">NOTES</span></span>

## <span data-ttu-id="8c4c7-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c4c7-158">RELATED LINKS</span></span>

[<span data-ttu-id="8c4c7-159">AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8c4c7-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="8c4c7-160">移除-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8c4c7-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="8c4c7-161">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="8c4c7-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


