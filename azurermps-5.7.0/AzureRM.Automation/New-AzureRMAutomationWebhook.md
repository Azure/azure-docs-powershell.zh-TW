---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456256"
---
# <span data-ttu-id="ce80d-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ce80d-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="ce80d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce80d-102">SYNOPSIS</span></span>
<span data-ttu-id="ce80d-103">為自動化 runbook 建立 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce80d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce80d-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce80d-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce80d-105">DESCRIPTION</span></span>
<span data-ttu-id="ce80d-106">**新的-AzureRmAutomationWebhook** Cmdlet 會為 Azure 自動化 runbook 建立 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="ce80d-107">請務必儲存此 Cmdlet 傳回的 webhook URL，因為無法再次檢索它。</span><span class="sxs-lookup"><span data-stu-id="ce80d-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="ce80d-108">示例</span><span class="sxs-lookup"><span data-stu-id="ce80d-108">EXAMPLES</span></span>

### <span data-ttu-id="ce80d-109">範例1：建立 webhook</span><span class="sxs-lookup"><span data-stu-id="ce80d-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="ce80d-110">這個命令會針對自動化帳戶（名為 AutomationAccount01）中名為 ContosoRunbook 的 runbook，建立一個名為 Webhook06 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="ce80d-111">該命令會將 webhook 儲存在 $Webhook 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce80d-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="ce80d-112">已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-112">The webhook is enabled.</span></span>
<span data-ttu-id="ce80d-113">Webhook 會在指定的時間到期。</span><span class="sxs-lookup"><span data-stu-id="ce80d-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="ce80d-114">這個命令不會提供 webhook 參數的任何值。</span><span class="sxs-lookup"><span data-stu-id="ce80d-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="ce80d-115">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="ce80d-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ce80d-116">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce80d-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ce80d-117">範例2：使用參數建立 webhook</span><span class="sxs-lookup"><span data-stu-id="ce80d-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="ce80d-118">第一個命令會建立參數字典，並將它們儲存在 $Params 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce80d-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="ce80d-119">第二個命令會針對自動化帳戶（名為 AutomationAccount01）中名為 ContosoRunbook 的 runbook，建立一個名為 Webhook11 的 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="ce80d-120">命令會將 $Params 中的參數指派給 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="ce80d-121">參數</span><span class="sxs-lookup"><span data-stu-id="ce80d-121">PARAMETERS</span></span>

### <span data-ttu-id="ce80d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce80d-122">-AutomationAccountName</span></span>
<span data-ttu-id="ce80d-123">指定此 Cmdlet 建立 webhook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80d-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="ce80d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce80d-124">-DefaultProfile</span></span>
<span data-ttu-id="ce80d-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce80d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce80d-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ce80d-126">-ExpiryTime</span></span>
<span data-ttu-id="ce80d-127">將 webhook 的到期時間指定為 **DateTimeOffset** 物件。</span><span class="sxs-lookup"><span data-stu-id="ce80d-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ce80d-128">您可以指定可轉換成有效 **DateTimeOffset** 的字串或 **日期時間** 。</span><span class="sxs-lookup"><span data-stu-id="ce80d-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce80d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ce80d-129">-Force</span></span>
<span data-ttu-id="ce80d-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="ce80d-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce80d-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="ce80d-131">-IsEnabled</span></span>
<span data-ttu-id="ce80d-132">指定是否已啟用 webhook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce80d-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce80d-133">-Name</span></span>
<span data-ttu-id="ce80d-134">指定 webhook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80d-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="ce80d-135">-參數</span><span class="sxs-lookup"><span data-stu-id="ce80d-135">-Parameters</span></span>
<span data-ttu-id="ce80d-136">指定鍵/值對的字典。</span><span class="sxs-lookup"><span data-stu-id="ce80d-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="ce80d-137">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80d-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="ce80d-138">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="ce80d-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="ce80d-139">當 runbook 開始回應 webhook 時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="ce80d-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce80d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce80d-140">-ResourceGroupName</span></span>
<span data-ttu-id="ce80d-141">指定此 Cmdlet 建立 webhook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80d-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="ce80d-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ce80d-142">-RunbookName</span></span>
<span data-ttu-id="ce80d-143">指定要與 webhook 相關聯的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="ce80d-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce80d-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="ce80d-144">-RunOn</span></span>
<span data-ttu-id="ce80d-145">應執行 runbook 之混合式輔助角色群組的選用名稱</span><span class="sxs-lookup"><span data-stu-id="ce80d-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce80d-146">-確認</span><span class="sxs-lookup"><span data-stu-id="ce80d-146">-Confirm</span></span>
<span data-ttu-id="ce80d-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce80d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce80d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce80d-148">-WhatIf</span></span>
<span data-ttu-id="ce80d-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce80d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce80d-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce80d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce80d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce80d-151">CommonParameters</span></span>
<span data-ttu-id="ce80d-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce80d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce80d-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce80d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce80d-154">輸入</span><span class="sxs-lookup"><span data-stu-id="ce80d-154">INPUTS</span></span>

### <span data-ttu-id="ce80d-155">所有</span><span class="sxs-lookup"><span data-stu-id="ce80d-155">None</span></span>
<span data-ttu-id="ce80d-156">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ce80d-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce80d-157">輸出</span><span class="sxs-lookup"><span data-stu-id="ce80d-157">OUTPUTS</span></span>

### <span data-ttu-id="ce80d-158">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="ce80d-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="ce80d-159">筆記</span><span class="sxs-lookup"><span data-stu-id="ce80d-159">NOTES</span></span>

## <span data-ttu-id="ce80d-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce80d-160">RELATED LINKS</span></span>

[<span data-ttu-id="ce80d-161">AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ce80d-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ce80d-162">移除-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ce80d-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="ce80d-163">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="ce80d-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


