---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: b3484b410ef885567010c05660590808f3995308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449356"
---
# <span data-ttu-id="e793c-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e793c-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="e793c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e793c-102">SYNOPSIS</span></span>
<span data-ttu-id="e793c-103">建立警示規則的電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="e793c-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e793c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e793c-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e793c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e793c-105">DESCRIPTION</span></span>
<span data-ttu-id="e793c-106">**新的-AzureRmAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="e793c-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="e793c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e793c-107">EXAMPLES</span></span>

### <span data-ttu-id="e793c-108">範例1：建立服務擁有者的警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="e793c-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="e793c-109">當觸發警示規則時，這個命令會建立一個要傳送給其服務擁有者的警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="e793c-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="e793c-110">範例2：為非服務擁有者建立警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="e793c-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="e793c-111">這個命令會針對指定的電子郵件地址建立一個警示規則電子郵件動作，但不適用於服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="e793c-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="e793c-112">範例3：為服務擁有者和非服務擁有者建立警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="e793c-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="e793c-113">這個命令會針對指定的位址和其服務擁有者建立一個警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="e793c-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="e793c-114">參數</span><span class="sxs-lookup"><span data-stu-id="e793c-114">PARAMETERS</span></span>

### <span data-ttu-id="e793c-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="e793c-115">-CustomEmail</span></span>
<span data-ttu-id="e793c-116">指定逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="e793c-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e793c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e793c-117">-DefaultProfile</span></span>
<span data-ttu-id="e793c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e793c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e793c-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="e793c-119">-SendToServiceOwner</span></span>
<span data-ttu-id="e793c-120">表示此操作會在規則激發時傳送電子郵件給服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="e793c-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendToServiceOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e793c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e793c-121">CommonParameters</span></span>
<span data-ttu-id="e793c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e793c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e793c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e793c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e793c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e793c-124">INPUTS</span></span>

### <span data-ttu-id="e793c-125">所有</span><span class="sxs-lookup"><span data-stu-id="e793c-125">None</span></span>
<span data-ttu-id="e793c-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e793c-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e793c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e793c-127">OUTPUTS</span></span>

### <span data-ttu-id="e793c-128">RuleEmailAction 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="e793c-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="e793c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e793c-129">NOTES</span></span>

## <span data-ttu-id="e793c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e793c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e793c-131">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e793c-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e793c-132">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e793c-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e793c-133">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e793c-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e793c-134">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e793c-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


