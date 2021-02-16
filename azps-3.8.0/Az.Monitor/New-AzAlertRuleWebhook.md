---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 8410ca475ed17376e01a526512d758c4712f2726
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411274"
---
# <span data-ttu-id="de00a-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="de00a-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="de00a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de00a-102">SYNOPSIS</span></span>
<span data-ttu-id="de00a-103">建立警示規則 web一樣。</span><span class="sxs-lookup"><span data-stu-id="de00a-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="de00a-104">語法</span><span class="sxs-lookup"><span data-stu-id="de00a-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de00a-105">描述</span><span class="sxs-lookup"><span data-stu-id="de00a-105">DESCRIPTION</span></span>
<span data-ttu-id="de00a-106">**New-AzAlertRuleWeb有 Cmdlet** 會建立警示規則 webrule。</span><span class="sxs-lookup"><span data-stu-id="de00a-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="de00a-107">例子</span><span class="sxs-lookup"><span data-stu-id="de00a-107">EXAMPLES</span></span>

### <span data-ttu-id="de00a-108">範例 1：建立通知規則 Web更</span><span class="sxs-lookup"><span data-stu-id="de00a-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="de00a-109">此命令僅指定服務 URI，以建立警示規則 web建立。</span><span class="sxs-lookup"><span data-stu-id="de00a-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="de00a-110">範例 2：使用一個屬性建立 Web一個</span><span class="sxs-lookup"><span data-stu-id="de00a-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="de00a-111">此命令會針對具有一個屬性Contoso.com建立提醒規則 web出，然後將它儲存在$Actual變數中。</span><span class="sxs-lookup"><span data-stu-id="de00a-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="de00a-112">參數</span><span class="sxs-lookup"><span data-stu-id="de00a-112">PARAMETERS</span></span>

### <span data-ttu-id="de00a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de00a-113">-DefaultProfile</span></span>
<span data-ttu-id="de00a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="de00a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de00a-115">-屬性</span><span class="sxs-lookup"><span data-stu-id="de00a-115">-Property</span></span>
<span data-ttu-id="de00a-116">指定格式為 @ (屬性1 = 'value1',....) 。</span><span class="sxs-lookup"><span data-stu-id="de00a-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="de00a-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="de00a-117">-ServiceUri</span></span>
<span data-ttu-id="de00a-118">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="de00a-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="de00a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de00a-119">CommonParameters</span></span>
<span data-ttu-id="de00a-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de00a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de00a-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de00a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de00a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="de00a-122">INPUTS</span></span>

### <span data-ttu-id="de00a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="de00a-123">System.String</span></span>

### <span data-ttu-id="de00a-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="de00a-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de00a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="de00a-125">OUTPUTS</span></span>

### <span data-ttu-id="de00a-126">Microsoft.Azure.management.monitor.management.models.RuleWebaction</span><span class="sxs-lookup"><span data-stu-id="de00a-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="de00a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="de00a-127">NOTES</span></span>

## <span data-ttu-id="de00a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="de00a-128">RELATED LINKS</span></span>


[<span data-ttu-id="de00a-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="de00a-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="de00a-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="de00a-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="de00a-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="de00a-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="de00a-132">New-AzAutoscaleWeb用</span><span class="sxs-lookup"><span data-stu-id="de00a-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


