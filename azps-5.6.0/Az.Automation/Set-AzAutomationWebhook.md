---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 200cc0b6312940606bb4e75f576c60928a84b33f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916651"
---
# <span data-ttu-id="9cd11-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9cd11-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="9cd11-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9cd11-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd11-103">修改自動化 Runbook 的 web一樣。</span><span class="sxs-lookup"><span data-stu-id="9cd11-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="9cd11-104">語法</span><span class="sxs-lookup"><span data-stu-id="9cd11-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cd11-105">描述</span><span class="sxs-lookup"><span data-stu-id="9cd11-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd11-106">**Set-AzAutomationWeb用 Cmdlet** 會修改 Azure 自動化執行手冊的 Web一體。</span><span class="sxs-lookup"><span data-stu-id="9cd11-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="9cd11-107">例子</span><span class="sxs-lookup"><span data-stu-id="9cd11-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd11-108">範例 1：停用網頁設計</span><span class="sxs-lookup"><span data-stu-id="9cd11-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="9cd11-109">此命令會停用名為 AutomationAccount01 的自動化帳戶中名為 Web automation01 的網頁化。</span><span class="sxs-lookup"><span data-stu-id="9cd11-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="9cd11-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="9cd11-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="9cd11-111">此命令會設定 Web 一個值的執行，並強制在稱為 Windows 的混合式員工群組上執行 runbook。</span><span class="sxs-lookup"><span data-stu-id="9cd11-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="9cd11-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="9cd11-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="9cd11-113">此命令會更新 Web 一值的執行，並強制在 Azure runbook 工作程式上執行 runbook。</span><span class="sxs-lookup"><span data-stu-id="9cd11-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="9cd11-114">參數</span><span class="sxs-lookup"><span data-stu-id="9cd11-114">PARAMETERS</span></span>

### <span data-ttu-id="9cd11-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9cd11-115">-AutomationAccountName</span></span>
<span data-ttu-id="9cd11-116">指定此 Cmdlet 可修改 Web一個網頁的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9cd11-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9cd11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd11-117">-DefaultProfile</span></span>
<span data-ttu-id="9cd11-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9cd11-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cd11-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="9cd11-119">-IsEnabled</span></span>
<span data-ttu-id="9cd11-120">指定網頁設計是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="9cd11-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="9cd11-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cd11-121">-Name</span></span>
<span data-ttu-id="9cd11-122">指定此 Cmdlet 修改的網頁網站名稱。</span><span class="sxs-lookup"><span data-stu-id="9cd11-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9cd11-123">-參數</span><span class="sxs-lookup"><span data-stu-id="9cd11-123">-Parameters</span></span>
<span data-ttu-id="9cd11-124">指定金鑰/值組字典。</span><span class="sxs-lookup"><span data-stu-id="9cd11-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="9cd11-125">這些鍵是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="9cd11-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="9cd11-126">值為 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="9cd11-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="9cd11-127">當 runbook 開始回應 web一樣時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="9cd11-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="9cd11-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd11-128">-ResourceGroupName</span></span>
<span data-ttu-id="9cd11-129">指定此 Cmdlet 可修改 Web一項功能的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9cd11-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="9cd11-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="9cd11-130">-RunOn</span></span>
<span data-ttu-id="9cd11-131">混合式代理程式應執行 runbook 的選擇性名稱</span><span class="sxs-lookup"><span data-stu-id="9cd11-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="9cd11-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd11-132">CommonParameters</span></span>
<span data-ttu-id="9cd11-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9cd11-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd11-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cd11-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd11-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9cd11-135">INPUTS</span></span>

### <span data-ttu-id="9cd11-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9cd11-136">System.String</span></span>

### <span data-ttu-id="9cd11-137">System.Nullable'1[[System.Boolean， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9cd11-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9cd11-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="9cd11-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9cd11-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9cd11-139">OUTPUTS</span></span>

### <span data-ttu-id="9cd11-140">Microsoft.Azure.Commands.Automation.Model.Webaz</span><span class="sxs-lookup"><span data-stu-id="9cd11-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="9cd11-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9cd11-141">NOTES</span></span>

## <span data-ttu-id="9cd11-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cd11-142">RELATED LINKS</span></span>

[<span data-ttu-id="9cd11-143">Get-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="9cd11-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="9cd11-144">New-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="9cd11-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="9cd11-145">Remove-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="9cd11-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


