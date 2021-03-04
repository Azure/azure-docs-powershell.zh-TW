---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 22afc323e827c543150bffb317f1b5db5275d82c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908893"
---
# <span data-ttu-id="791cc-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="791cc-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="791cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="791cc-102">SYNOPSIS</span></span>
<span data-ttu-id="791cc-103">建立警示規則 web一樣。</span><span class="sxs-lookup"><span data-stu-id="791cc-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="791cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="791cc-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="791cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="791cc-105">DESCRIPTION</span></span>
<span data-ttu-id="791cc-106">**New-AzAlertRuleWeb有 Cmdlet** 會建立提醒規則 webrule。</span><span class="sxs-lookup"><span data-stu-id="791cc-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="791cc-107">例子</span><span class="sxs-lookup"><span data-stu-id="791cc-107">EXAMPLES</span></span>

### <span data-ttu-id="791cc-108">範例 1：建立提醒規則 web更</span><span class="sxs-lookup"><span data-stu-id="791cc-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="791cc-109">此命令僅指定服務 URI，以建立警示規則 web建立。</span><span class="sxs-lookup"><span data-stu-id="791cc-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="791cc-110">範例 2：使用一個屬性建立 Web一個</span><span class="sxs-lookup"><span data-stu-id="791cc-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="791cc-111">此命令會針對具有一個屬性Contoso.com建立提醒規則 web下一個屬性，然後將它儲存在$Actual變數中。</span><span class="sxs-lookup"><span data-stu-id="791cc-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="791cc-112">參數</span><span class="sxs-lookup"><span data-stu-id="791cc-112">PARAMETERS</span></span>

### <span data-ttu-id="791cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791cc-113">-DefaultProfile</span></span>
<span data-ttu-id="791cc-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="791cc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="791cc-115">-屬性</span><span class="sxs-lookup"><span data-stu-id="791cc-115">-Property</span></span>
<span data-ttu-id="791cc-116">指定格式為 @ (屬性1 = 'value1',....) 。</span><span class="sxs-lookup"><span data-stu-id="791cc-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="791cc-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="791cc-117">-ServiceUri</span></span>
<span data-ttu-id="791cc-118">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="791cc-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="791cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791cc-119">CommonParameters</span></span>
<span data-ttu-id="791cc-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="791cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791cc-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="791cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791cc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="791cc-122">INPUTS</span></span>

### <span data-ttu-id="791cc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="791cc-123">System.String</span></span>

### <span data-ttu-id="791cc-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="791cc-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="791cc-125">輸出</span><span class="sxs-lookup"><span data-stu-id="791cc-125">OUTPUTS</span></span>

### <span data-ttu-id="791cc-126">Microsoft.Azure.management.Monitor.management.models.RuleWebaction</span><span class="sxs-lookup"><span data-stu-id="791cc-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="791cc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="791cc-127">NOTES</span></span>

## <span data-ttu-id="791cc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="791cc-128">RELATED LINKS</span></span>

[<span data-ttu-id="791cc-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="791cc-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="791cc-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="791cc-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="791cc-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="791cc-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="791cc-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="791cc-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="791cc-133">New-AzAutoscaleWeb用</span><span class="sxs-lookup"><span data-stu-id="791cc-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


