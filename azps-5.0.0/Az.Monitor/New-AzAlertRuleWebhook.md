---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284676"
---
# <span data-ttu-id="9ffa4-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="9ffa4-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="9ffa4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ffa4-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffa4-103">建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="9ffa4-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ffa4-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ffa4-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ffa4-105">DESCRIPTION</span></span>
<span data-ttu-id="9ffa4-106">**新的-AzAlertRuleWebhook** Cmdlet 會建立一個警報規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="9ffa4-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ffa4-107">EXAMPLES</span></span>

### <span data-ttu-id="9ffa4-108">範例1：建立警示規則 webhook</span><span class="sxs-lookup"><span data-stu-id="9ffa4-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="9ffa4-109">這個命令會透過只指定服務 URI 來建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="9ffa4-110">範例2：使用一個屬性建立 webhook</span><span class="sxs-lookup"><span data-stu-id="9ffa4-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="9ffa4-111">這個命令會針對具有一個屬性的 Contoso.com 建立一個警示規則 webhook，然後將它儲存在 $Actual 變數中。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="9ffa4-112">參數</span><span class="sxs-lookup"><span data-stu-id="9ffa4-112">PARAMETERS</span></span>

### <span data-ttu-id="9ffa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffa4-113">-DefaultProfile</span></span>
<span data-ttu-id="9ffa4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9ffa4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ffa4-115">-屬性</span><span class="sxs-lookup"><span data-stu-id="9ffa4-115">-Property</span></span>
<span data-ttu-id="9ffa4-116">指定 [@ (property1 = ' value1 ",.... ) 格式的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="9ffa4-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="9ffa4-117">-ServiceUri</span></span>
<span data-ttu-id="9ffa4-118">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="9ffa4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffa4-119">CommonParameters</span></span>
<span data-ttu-id="9ffa4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffa4-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffa4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9ffa4-122">INPUTS</span></span>

### <span data-ttu-id="9ffa4-123">System.object</span><span class="sxs-lookup"><span data-stu-id="9ffa4-123">System.String</span></span>

### <span data-ttu-id="9ffa4-124">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ffa4-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9ffa4-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9ffa4-125">OUTPUTS</span></span>

### <span data-ttu-id="9ffa4-126">RuleWebhookAction 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="9ffa4-127">筆記</span><span class="sxs-lookup"><span data-stu-id="9ffa4-127">NOTES</span></span>

## <span data-ttu-id="9ffa4-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ffa4-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ffa4-129">附加 AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ffa4-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="9ffa4-130">附加 AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ffa4-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="9ffa4-131">附加 AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ffa4-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="9ffa4-132">新-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="9ffa4-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="9ffa4-133">新-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="9ffa4-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


