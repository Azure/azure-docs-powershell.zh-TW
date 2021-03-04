---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 520efcb6cccc3c3d4c0afc3b532d528c11c305c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913262"
---
# <span data-ttu-id="461a4-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="461a4-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="461a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="461a4-102">SYNOPSIS</span></span>
<span data-ttu-id="461a4-103">為自動化 runbook 建立 Web一個 Web一樣。</span><span class="sxs-lookup"><span data-stu-id="461a4-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="461a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="461a4-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="461a4-105">描述</span><span class="sxs-lookup"><span data-stu-id="461a4-105">DESCRIPTION</span></span>
<span data-ttu-id="461a4-106">**New-AzAutomationWebtomation Cmdlet** 會為 Azure 自動化執行手冊建立 Webaz。</span><span class="sxs-lookup"><span data-stu-id="461a4-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="461a4-107">請務必儲存此 Cmdlet 會返回的網頁連結 URL，因為它無法再次取回。</span><span class="sxs-lookup"><span data-stu-id="461a4-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="461a4-108">例子</span><span class="sxs-lookup"><span data-stu-id="461a4-108">EXAMPLES</span></span>

### <span data-ttu-id="461a4-109">範例 1：建立網頁</span><span class="sxs-lookup"><span data-stu-id="461a4-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="461a4-110">此命令會為自動化帳戶中名為 ContosoRunbook 的 Runbook 建立一個名為 Web automation06 的 Web一個 Web一般，名稱為 AutomationAccount01。</span><span class="sxs-lookup"><span data-stu-id="461a4-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="461a4-111">命令會儲存網頁$Webhook變數。</span><span class="sxs-lookup"><span data-stu-id="461a4-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="461a4-112">網頁設計已啟用。</span><span class="sxs-lookup"><span data-stu-id="461a4-112">The webhook is enabled.</span></span>
<span data-ttu-id="461a4-113">Web一開始會在指定的時間到期。</span><span class="sxs-lookup"><span data-stu-id="461a4-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="461a4-114">此命令不會提供 Web 一些參數的任何值。</span><span class="sxs-lookup"><span data-stu-id="461a4-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="461a4-115">此命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="461a4-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="461a4-116">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="461a4-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="461a4-117">範例 2：使用參數建立 Web一</span><span class="sxs-lookup"><span data-stu-id="461a4-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="461a4-118">第一個命令會建立參數字典，並儲存在$Params變數中。</span><span class="sxs-lookup"><span data-stu-id="461a4-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="461a4-119">第二個命令會為自動化帳戶中名為 ContosoRunbook 的 Runbook 建立一個名為 Web automation11 的 Web一個 Web automation，名稱為 AutomationAccount01。</span><span class="sxs-lookup"><span data-stu-id="461a4-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="461a4-120">該命令會指派$Params至 web一樣。</span><span class="sxs-lookup"><span data-stu-id="461a4-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="461a4-121">參數</span><span class="sxs-lookup"><span data-stu-id="461a4-121">PARAMETERS</span></span>

### <span data-ttu-id="461a4-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="461a4-122">-AutomationAccountName</span></span>
<span data-ttu-id="461a4-123">指定此 Cmdlet 在其中建立 Web一個 Web一樣之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="461a4-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="461a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461a4-124">-DefaultProfile</span></span>
<span data-ttu-id="461a4-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="461a4-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="461a4-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="461a4-126">-ExpiryTime</span></span>
<span data-ttu-id="461a4-127">指定 Web 一個 **DateTimeOffset** 物件的到期時間。</span><span class="sxs-lookup"><span data-stu-id="461a4-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="461a4-128">您可以指定可轉換成有效 **DateTimeOffset** 的字串或 DateTime。 </span><span class="sxs-lookup"><span data-stu-id="461a4-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="461a4-129">-強制</span><span class="sxs-lookup"><span data-stu-id="461a4-129">-Force</span></span>
<span data-ttu-id="461a4-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="461a4-130">ps_force</span></span>

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

### <span data-ttu-id="461a4-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="461a4-131">-IsEnabled</span></span>
<span data-ttu-id="461a4-132">指定網頁設計是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="461a4-132">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="461a4-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="461a4-133">-Name</span></span>
<span data-ttu-id="461a4-134">指定網頁設計的名稱。</span><span class="sxs-lookup"><span data-stu-id="461a4-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="461a4-135">-參數</span><span class="sxs-lookup"><span data-stu-id="461a4-135">-Parameters</span></span>
<span data-ttu-id="461a4-136">指定金鑰/值組字典。</span><span class="sxs-lookup"><span data-stu-id="461a4-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="461a4-137">這些鍵是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="461a4-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="461a4-138">值為 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="461a4-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="461a4-139">當 runbook 開始回應 web一樣時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="461a4-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="461a4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461a4-140">-ResourceGroupName</span></span>
<span data-ttu-id="461a4-141">指定此 Cmdlet 建立 Web 一個網頁組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="461a4-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="461a4-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="461a4-142">-RunbookName</span></span>
<span data-ttu-id="461a4-143">指定要與 web一起關聯的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="461a4-143">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="461a4-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="461a4-144">-RunOn</span></span>
<span data-ttu-id="461a4-145">應該執行 runbook 的混合式員工群組的選擇性名稱</span><span class="sxs-lookup"><span data-stu-id="461a4-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="461a4-146">-確認</span><span class="sxs-lookup"><span data-stu-id="461a4-146">-Confirm</span></span>
<span data-ttu-id="461a4-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="461a4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="461a4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="461a4-148">-WhatIf</span></span>
<span data-ttu-id="461a4-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="461a4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="461a4-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="461a4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="461a4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461a4-151">CommonParameters</span></span>
<span data-ttu-id="461a4-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="461a4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461a4-153">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="461a4-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461a4-154">輸入</span><span class="sxs-lookup"><span data-stu-id="461a4-154">INPUTS</span></span>

### <span data-ttu-id="461a4-155">System.String</span><span class="sxs-lookup"><span data-stu-id="461a4-155">System.String</span></span>

### <span data-ttu-id="461a4-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="461a4-156">System.Boolean</span></span>

### <span data-ttu-id="461a4-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="461a4-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="461a4-158">輸出</span><span class="sxs-lookup"><span data-stu-id="461a4-158">OUTPUTS</span></span>

### <span data-ttu-id="461a4-159">Microsoft.Azure.Commands.Automation.Model.Webaz</span><span class="sxs-lookup"><span data-stu-id="461a4-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="461a4-160">筆記</span><span class="sxs-lookup"><span data-stu-id="461a4-160">NOTES</span></span>

## <span data-ttu-id="461a4-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="461a4-161">RELATED LINKS</span></span>

[<span data-ttu-id="461a4-162">Get-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="461a4-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="461a4-163">Remove-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="461a4-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="461a4-164">Set-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="461a4-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


