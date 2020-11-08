---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141477"
---
# <span data-ttu-id="0b82b-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="0b82b-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="0b82b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b82b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b82b-103">建立警示規則的電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="0b82b-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="0b82b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b82b-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b82b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b82b-105">DESCRIPTION</span></span>
<span data-ttu-id="0b82b-106">**新的-AzAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="0b82b-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="0b82b-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b82b-107">EXAMPLES</span></span>

### <span data-ttu-id="0b82b-108">範例1：建立服務擁有者的警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="0b82b-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="0b82b-109">當觸發警示規則時，這個命令會建立一個要傳送給其服務擁有者的警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="0b82b-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="0b82b-110">範例2：為非服務擁有者建立警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="0b82b-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="0b82b-111">這個命令會針對指定的電子郵件地址建立一個警示規則電子郵件動作，但不適用於服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="0b82b-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="0b82b-112">範例3：為服務擁有者和非服務擁有者建立警示規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="0b82b-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="0b82b-113">這個命令會針對指定的位址和其服務擁有者建立一個警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="0b82b-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="0b82b-114">參數</span><span class="sxs-lookup"><span data-stu-id="0b82b-114">PARAMETERS</span></span>

### <span data-ttu-id="0b82b-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="0b82b-115">-CustomEmail</span></span>
<span data-ttu-id="0b82b-116">指定逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="0b82b-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="0b82b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b82b-117">-DefaultProfile</span></span>
<span data-ttu-id="0b82b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0b82b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b82b-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="0b82b-119">-SendToServiceOwner</span></span>
<span data-ttu-id="0b82b-120">表示此操作會在規則激發時傳送電子郵件給服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="0b82b-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="0b82b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b82b-121">CommonParameters</span></span>
<span data-ttu-id="0b82b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b82b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b82b-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b82b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b82b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0b82b-124">INPUTS</span></span>

### <span data-ttu-id="0b82b-125">System.object []</span><span class="sxs-lookup"><span data-stu-id="0b82b-125">System.String[]</span></span>

### <span data-ttu-id="0b82b-126">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="0b82b-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b82b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0b82b-127">OUTPUTS</span></span>

### <span data-ttu-id="0b82b-128">RuleEmailAction 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="0b82b-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="0b82b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0b82b-129">NOTES</span></span>

## <span data-ttu-id="0b82b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b82b-130">RELATED LINKS</span></span>

[<span data-ttu-id="0b82b-131">附加 AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="0b82b-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="0b82b-132">附加 AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0b82b-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="0b82b-133">附加 AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0b82b-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="0b82b-134">新-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="0b82b-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

