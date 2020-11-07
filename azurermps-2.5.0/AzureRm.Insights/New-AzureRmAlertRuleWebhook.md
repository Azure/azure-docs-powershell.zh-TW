---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802474"
---
# <span data-ttu-id="d0227-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d0227-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="d0227-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0227-102">SYNOPSIS</span></span>
<span data-ttu-id="d0227-103">建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="d0227-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0227-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0227-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0227-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0227-105">DESCRIPTION</span></span>
<span data-ttu-id="d0227-106">**新的-AzureRmAlertRuleWebhook** Cmdlet 會建立一個警報規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="d0227-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="d0227-107">示例</span><span class="sxs-lookup"><span data-stu-id="d0227-107">EXAMPLES</span></span>

### <span data-ttu-id="d0227-108">範例1：建立警示規則 webhook</span><span class="sxs-lookup"><span data-stu-id="d0227-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="d0227-109">這個命令會透過只指定服務 URI 來建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="d0227-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="d0227-110">範例2：使用一個屬性建立 webhook</span><span class="sxs-lookup"><span data-stu-id="d0227-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="d0227-111">這個命令會針對具有一個屬性的 Contoso.com 建立一個警示規則 webhook，然後將它儲存在 $Actual 變數中。</span><span class="sxs-lookup"><span data-stu-id="d0227-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="d0227-112">參數</span><span class="sxs-lookup"><span data-stu-id="d0227-112">PARAMETERS</span></span>

### <span data-ttu-id="d0227-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0227-113">-DefaultProfile</span></span>
<span data-ttu-id="d0227-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d0227-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0227-115">-屬性</span><span class="sxs-lookup"><span data-stu-id="d0227-115">-Property</span></span>
<span data-ttu-id="d0227-116">指定 [@ (property1 = ' value1 ",.... ) 格式的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="d0227-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="d0227-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d0227-117">-ServiceUri</span></span>
<span data-ttu-id="d0227-118">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="d0227-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="d0227-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0227-119">CommonParameters</span></span>
<span data-ttu-id="d0227-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0227-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0227-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0227-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0227-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d0227-122">INPUTS</span></span>

### <span data-ttu-id="d0227-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d0227-123">System.String</span></span>

### <span data-ttu-id="d0227-124">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d0227-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d0227-125">輸出</span><span class="sxs-lookup"><span data-stu-id="d0227-125">OUTPUTS</span></span>

### <span data-ttu-id="d0227-126">RuleWebhookAction 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="d0227-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="d0227-127">筆記</span><span class="sxs-lookup"><span data-stu-id="d0227-127">NOTES</span></span>

## <span data-ttu-id="d0227-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0227-128">RELATED LINKS</span></span>



[<span data-ttu-id="d0227-129">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d0227-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="d0227-130">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d0227-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="d0227-131">新-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="d0227-131">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="d0227-132">新-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d0227-132">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


