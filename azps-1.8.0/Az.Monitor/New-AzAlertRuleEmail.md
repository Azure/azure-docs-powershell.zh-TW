---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 063eccb7d42fdee26c642a866c2bce398c87662e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403046"
---
# <span data-ttu-id="89bca-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="89bca-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="89bca-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89bca-102">SYNOPSIS</span></span>
<span data-ttu-id="89bca-103">為警示規則建立電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="89bca-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="89bca-104">語法</span><span class="sxs-lookup"><span data-stu-id="89bca-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89bca-105">描述</span><span class="sxs-lookup"><span data-stu-id="89bca-105">DESCRIPTION</span></span>
<span data-ttu-id="89bca-106">**New-AzAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="89bca-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="89bca-107">例子</span><span class="sxs-lookup"><span data-stu-id="89bca-107">EXAMPLES</span></span>

### <span data-ttu-id="89bca-108">範例 1：為服務擁有者建立提醒規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="89bca-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="89bca-109">此命令會建立警示規則電子郵件動作，以在警示規則發出時傳送給服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="89bca-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="89bca-110">範例 2：為非服務擁有者建立提醒規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="89bca-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="89bca-111">此命令會為指定的電子郵件地址建立通知規則電子郵件動作，但服務擁有者則不在此。</span><span class="sxs-lookup"><span data-stu-id="89bca-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="89bca-112">範例 3：為服務擁有者和非服務擁有者建立提醒規則電子郵件動作</span><span class="sxs-lookup"><span data-stu-id="89bca-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="89bca-113">此命令會針對指定位址及其服務擁有者建立警示規則電子郵件動作。</span><span class="sxs-lookup"><span data-stu-id="89bca-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="89bca-114">參數</span><span class="sxs-lookup"><span data-stu-id="89bca-114">PARAMETERS</span></span>

### <span data-ttu-id="89bca-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="89bca-115">-CustomEmail</span></span>
<span data-ttu-id="89bca-116">指定逗號分隔電子郵件地址的清單。</span><span class="sxs-lookup"><span data-stu-id="89bca-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="89bca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bca-117">-DefaultProfile</span></span>
<span data-ttu-id="89bca-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="89bca-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89bca-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="89bca-119">-SendToServiceOwner</span></span>
<span data-ttu-id="89bca-120">表示此作業在規則啟用時傳送電子郵件給服務擁有者。</span><span class="sxs-lookup"><span data-stu-id="89bca-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="89bca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bca-121">CommonParameters</span></span>
<span data-ttu-id="89bca-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89bca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bca-123">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="89bca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bca-124">輸入</span><span class="sxs-lookup"><span data-stu-id="89bca-124">INPUTS</span></span>

### <span data-ttu-id="89bca-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="89bca-125">System.String[]</span></span>

### <span data-ttu-id="89bca-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89bca-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89bca-127">輸出</span><span class="sxs-lookup"><span data-stu-id="89bca-127">OUTPUTS</span></span>

### <span data-ttu-id="89bca-128">Microsoft.Azure.management.Monitor.management.models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="89bca-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="89bca-129">筆記</span><span class="sxs-lookup"><span data-stu-id="89bca-129">NOTES</span></span>

## <span data-ttu-id="89bca-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="89bca-130">RELATED LINKS</span></span>


[<span data-ttu-id="89bca-131">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="89bca-131">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="89bca-132">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="89bca-132">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="89bca-133">New-AzAlertRuleWeb一體式</span><span class="sxs-lookup"><span data-stu-id="89bca-133">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


