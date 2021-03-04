---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917450"
---
# <span data-ttu-id="1a174-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1a174-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="1a174-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a174-102">SYNOPSIS</span></span>
<span data-ttu-id="1a174-103">從自動化中獲得網頁工具。</span><span class="sxs-lookup"><span data-stu-id="1a174-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="1a174-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a174-104">SYNTAX</span></span>

### <span data-ttu-id="1a174-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="1a174-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a174-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1a174-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a174-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="1a174-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a174-108">描述</span><span class="sxs-lookup"><span data-stu-id="1a174-108">DESCRIPTION</span></span>
<span data-ttu-id="1a174-109">**Get-AzAutomationWeb功能 Cmdlet** 會取得 web下拉式。</span><span class="sxs-lookup"><span data-stu-id="1a174-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="1a174-110">若要取得特定的網頁設計，請指定 Web 一個名稱，或指定 Azure 自動化執行手冊的名稱，以將網頁連結至該名稱。</span><span class="sxs-lookup"><span data-stu-id="1a174-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="1a174-111">**注意：** 基於安全性考慮，Weburi 會以空字串形式返回。</span><span class="sxs-lookup"><span data-stu-id="1a174-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="1a174-112">請務必儲存 **New-AzAutomationWebtomation Cmdlet** 所會返回的網頁連結 URL，因為它無法使用 **Get-AzAutomationWeb一併取回**。</span><span class="sxs-lookup"><span data-stu-id="1a174-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="1a174-113">例子</span><span class="sxs-lookup"><span data-stu-id="1a174-113">EXAMPLES</span></span>

### <span data-ttu-id="1a174-114">範例 1：取得 runbook 的所有 web下一個</span><span class="sxs-lookup"><span data-stu-id="1a174-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1a174-115">此命令會針對資源群組中名為 AutomationAccount01 的自動化帳戶名為 Runbook03 的 Runbook，獲得所有網頁工具。</span><span class="sxs-lookup"><span data-stu-id="1a174-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="1a174-116">參數</span><span class="sxs-lookup"><span data-stu-id="1a174-116">PARAMETERS</span></span>

### <span data-ttu-id="1a174-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a174-117">-AutomationAccountName</span></span>
<span data-ttu-id="1a174-118">指定此 Cmdlet 會在此帳戶內獲得 Web一個 Web 一個自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a174-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="1a174-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a174-119">-DefaultProfile</span></span>
<span data-ttu-id="1a174-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1a174-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a174-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a174-121">-Name</span></span>
<span data-ttu-id="1a174-122">指定此 Cmdlet 會獲得的網頁專案名稱。</span><span class="sxs-lookup"><span data-stu-id="1a174-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a174-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a174-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a174-124">指定此 Cmdlet 會獲得 web功能的資源組名。</span><span class="sxs-lookup"><span data-stu-id="1a174-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="1a174-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="1a174-125">-RunbookName</span></span>
<span data-ttu-id="1a174-126">指定此 Cmdlet 會為它獲得網頁集的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="1a174-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a174-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a174-127">CommonParameters</span></span>
<span data-ttu-id="1a174-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a174-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a174-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1a174-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a174-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1a174-130">INPUTS</span></span>

### <span data-ttu-id="1a174-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1a174-131">System.String</span></span>

## <span data-ttu-id="1a174-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1a174-132">OUTPUTS</span></span>

### <span data-ttu-id="1a174-133">Microsoft.Azure.Commands.Automation.Model.Webaz</span><span class="sxs-lookup"><span data-stu-id="1a174-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="1a174-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1a174-134">NOTES</span></span>

## <span data-ttu-id="1a174-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a174-135">RELATED LINKS</span></span>

[<span data-ttu-id="1a174-136">New-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="1a174-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="1a174-137">Remove-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="1a174-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="1a174-138">Set-AzAutomationWeb用</span><span class="sxs-lookup"><span data-stu-id="1a174-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


