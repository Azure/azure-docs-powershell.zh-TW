---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447284"
---
# <span data-ttu-id="45bdc-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="45bdc-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="45bdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="45bdc-103">從自動化取得 webhooks。</span><span class="sxs-lookup"><span data-stu-id="45bdc-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="45bdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="45bdc-104">SYNTAX</span></span>

### <span data-ttu-id="45bdc-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="45bdc-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45bdc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="45bdc-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45bdc-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="45bdc-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45bdc-108">說明</span><span class="sxs-lookup"><span data-stu-id="45bdc-108">DESCRIPTION</span></span>
<span data-ttu-id="45bdc-109">**AzAutomationWebhook** Cmdlet 會取得 webhooks。</span><span class="sxs-lookup"><span data-stu-id="45bdc-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="45bdc-110">若要取得特定 webhooks，請指定 webhook 名稱，或指定 Azure 自動化 runbook 的名稱，以取得與其連線的 webhooks。</span><span class="sxs-lookup"><span data-stu-id="45bdc-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="45bdc-111">示例</span><span class="sxs-lookup"><span data-stu-id="45bdc-111">EXAMPLES</span></span>

### <span data-ttu-id="45bdc-112">範例1：取得 runbook 的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="45bdc-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="45bdc-113">這個命令會在名為 [ResourceGroup01] 的資源群組中，以名為「AutomationAccount01」的自動化帳戶中取得名為 Runbook03 的所有 webhooks。</span><span class="sxs-lookup"><span data-stu-id="45bdc-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="45bdc-114">參數</span><span class="sxs-lookup"><span data-stu-id="45bdc-114">PARAMETERS</span></span>

### <span data-ttu-id="45bdc-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="45bdc-115">-AutomationAccountName</span></span>
<span data-ttu-id="45bdc-116">指定此 Cmdlet 取得 webhook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="45bdc-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="45bdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bdc-117">-DefaultProfile</span></span>
<span data-ttu-id="45bdc-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="45bdc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45bdc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="45bdc-119">-Name</span></span>
<span data-ttu-id="45bdc-120">指定此 Cmdlet 取得的 webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="45bdc-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="45bdc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bdc-121">-ResourceGroupName</span></span>
<span data-ttu-id="45bdc-122">指定此 Cmdlet 取得 webhooks 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45bdc-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="45bdc-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="45bdc-123">-RunbookName</span></span>
<span data-ttu-id="45bdc-124">指定此 Cmdlet 取得 webhooks 的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="45bdc-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="45bdc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bdc-125">CommonParameters</span></span>
<span data-ttu-id="45bdc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45bdc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bdc-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45bdc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bdc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="45bdc-128">INPUTS</span></span>

### <span data-ttu-id="45bdc-129">System.object</span><span class="sxs-lookup"><span data-stu-id="45bdc-129">System.String</span></span>

## <span data-ttu-id="45bdc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="45bdc-130">OUTPUTS</span></span>

### <span data-ttu-id="45bdc-131">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="45bdc-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="45bdc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="45bdc-132">NOTES</span></span>

## <span data-ttu-id="45bdc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="45bdc-133">RELATED LINKS</span></span>

[<span data-ttu-id="45bdc-134">新-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="45bdc-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="45bdc-135">移除-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="45bdc-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="45bdc-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="45bdc-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


