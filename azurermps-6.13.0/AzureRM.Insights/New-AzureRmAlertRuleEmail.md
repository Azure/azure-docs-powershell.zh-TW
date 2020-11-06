---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: f5936bcbbf12308830fd158baa2c2d20f295694b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448412"
---
# <span data-ttu-id="7d730-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7d730-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="7d730-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d730-102">SYNOPSIS</span></span>
<span data-ttu-id="7d730-103">建立警示規則的電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="7d730-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d730-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d730-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d730-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d730-105">DESCRIPTION</span></span>
<span data-ttu-id="7d730-106">**新的-AzureRmAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="7d730-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="7d730-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d730-107">EXAMPLES</span></span>

### <span data-ttu-id="7d730-108">範例1：建立服務擁有者的警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="7d730-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="7d730-109">當觸發警示規則時，這個命令會建立一個要傳送給其服務擁有者的警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="7d730-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="7d730-110">範例2：為非服務擁有者建立警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="7d730-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="7d730-111">這個命令會針對指定的電子郵件地址建立一個警示規則電子郵件動作，但不適用於服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="7d730-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="7d730-112">範例3：為服務擁有者和非服務擁有者建立警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="7d730-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="7d730-113">這個命令會針對指定的位址和其服務擁有者建立一個警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="7d730-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="7d730-114">參數</span><span class="sxs-lookup"><span data-stu-id="7d730-114">PARAMETERS</span></span>

### <span data-ttu-id="7d730-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="7d730-115">-CustomEmail</span></span>
<span data-ttu-id="7d730-116">指定逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="7d730-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d730-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d730-117">-DefaultProfile</span></span>
<span data-ttu-id="7d730-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7d730-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d730-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="7d730-119">-SendToServiceOwner</span></span>
<span data-ttu-id="7d730-120">表示此操作會在規則激發時傳送電子郵件給服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="7d730-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d730-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d730-121">CommonParameters</span></span>
<span data-ttu-id="7d730-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d730-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d730-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d730-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d730-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7d730-124">INPUTS</span></span>

### <span data-ttu-id="7d730-125">System.object []</span><span class="sxs-lookup"><span data-stu-id="7d730-125">System.String[]</span></span>

### <span data-ttu-id="7d730-126">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7d730-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d730-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7d730-127">OUTPUTS</span></span>

### <span data-ttu-id="7d730-128">RuleEmailAction 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="7d730-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="7d730-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7d730-129">NOTES</span></span>

## <span data-ttu-id="7d730-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d730-130">RELATED LINKS</span></span>

[<span data-ttu-id="7d730-131">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d730-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="7d730-132">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d730-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7d730-133">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7d730-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7d730-134">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7d730-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


