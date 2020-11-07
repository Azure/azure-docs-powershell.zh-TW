---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: a384753d6407eff7864cea6972ac03ab5bd12515
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624631"
---
# <span data-ttu-id="676f5-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="676f5-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="676f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="676f5-102">SYNOPSIS</span></span>
<span data-ttu-id="676f5-103">從自動化取得 webhooks。</span><span class="sxs-lookup"><span data-stu-id="676f5-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="676f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="676f5-104">SYNTAX</span></span>

### <span data-ttu-id="676f5-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="676f5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="676f5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="676f5-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="676f5-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="676f5-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="676f5-108">說明</span><span class="sxs-lookup"><span data-stu-id="676f5-108">DESCRIPTION</span></span>
<span data-ttu-id="676f5-109">**AzureRmAutomationWebhook** Cmdlet 會取得 webhooks。</span><span class="sxs-lookup"><span data-stu-id="676f5-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="676f5-110">若要取得特定 webhooks，請指定 webhook 名稱，或指定 Azure 自動化 runbook 的名稱，以取得與其連線的 webhooks。</span><span class="sxs-lookup"><span data-stu-id="676f5-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="676f5-111">示例</span><span class="sxs-lookup"><span data-stu-id="676f5-111">EXAMPLES</span></span>

### <span data-ttu-id="676f5-112">範例1：取得 runbook 的所有 webhooks</span><span class="sxs-lookup"><span data-stu-id="676f5-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="676f5-113">這個命令會在名為 [ResourceGroup01] 的資源群組中，以名為「AutomationAccount01」的自動化帳戶中取得名為 Runbook03 的所有 webhooks。</span><span class="sxs-lookup"><span data-stu-id="676f5-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="676f5-114">參數</span><span class="sxs-lookup"><span data-stu-id="676f5-114">PARAMETERS</span></span>

### <span data-ttu-id="676f5-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="676f5-115">-AutomationAccountName</span></span>
<span data-ttu-id="676f5-116">指定此 Cmdlet 取得 webhook 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="676f5-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="676f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="676f5-117">-DefaultProfile</span></span>
<span data-ttu-id="676f5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="676f5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="676f5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="676f5-119">-Name</span></span>
<span data-ttu-id="676f5-120">指定此 Cmdlet 取得的 webhook 名稱。</span><span class="sxs-lookup"><span data-stu-id="676f5-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="676f5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="676f5-121">-ResourceGroupName</span></span>
<span data-ttu-id="676f5-122">指定此 Cmdlet 取得 webhooks 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="676f5-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="676f5-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="676f5-123">-RunbookName</span></span>
<span data-ttu-id="676f5-124">指定此 Cmdlet 取得 webhooks 的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="676f5-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="676f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="676f5-125">CommonParameters</span></span>
<span data-ttu-id="676f5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="676f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="676f5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="676f5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="676f5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="676f5-128">INPUTS</span></span>

### <span data-ttu-id="676f5-129">System.object</span><span class="sxs-lookup"><span data-stu-id="676f5-129">System.String</span></span>

## <span data-ttu-id="676f5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="676f5-130">OUTPUTS</span></span>

### <span data-ttu-id="676f5-131">[-Azure. 命令。</span><span class="sxs-lookup"><span data-stu-id="676f5-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="676f5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="676f5-132">NOTES</span></span>

## <span data-ttu-id="676f5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="676f5-133">RELATED LINKS</span></span>

[<span data-ttu-id="676f5-134">新-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="676f5-134">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="676f5-135">移除-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="676f5-135">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="676f5-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="676f5-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


