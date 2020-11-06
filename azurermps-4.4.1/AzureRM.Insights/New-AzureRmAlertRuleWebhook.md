---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455811"
---
# <span data-ttu-id="81583-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="81583-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="81583-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81583-102">SYNOPSIS</span></span>
<span data-ttu-id="81583-103">建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="81583-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81583-104">句法</span><span class="sxs-lookup"><span data-stu-id="81583-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81583-105">說明</span><span class="sxs-lookup"><span data-stu-id="81583-105">DESCRIPTION</span></span>
<span data-ttu-id="81583-106">**新的-AzureRmAlertRuleWebhook** Cmdlet 會建立一個警報規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="81583-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="81583-107">示例</span><span class="sxs-lookup"><span data-stu-id="81583-107">EXAMPLES</span></span>

### <span data-ttu-id="81583-108">範例1：建立警示規則 webhook</span><span class="sxs-lookup"><span data-stu-id="81583-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="81583-109">這個命令會透過只指定服務 URI 來建立警示規則 webhook。</span><span class="sxs-lookup"><span data-stu-id="81583-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="81583-110">範例2：使用一個屬性建立 webhook</span><span class="sxs-lookup"><span data-stu-id="81583-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="81583-111">這個命令會針對具有一個屬性的 Contoso.com 建立一個警示規則 webhook，然後將它儲存在 $Actual 變數中。</span><span class="sxs-lookup"><span data-stu-id="81583-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="81583-112">參數</span><span class="sxs-lookup"><span data-stu-id="81583-112">PARAMETERS</span></span>

### <span data-ttu-id="81583-113">-屬性</span><span class="sxs-lookup"><span data-stu-id="81583-113">-Properties</span></span>
<span data-ttu-id="81583-114">指定 [@ (property1 = ' value1 ",.... ) 格式的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="81583-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="81583-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="81583-115">-ServiceUri</span></span>
<span data-ttu-id="81583-116">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="81583-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="81583-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81583-117">-DefaultProfile</span></span>
<span data-ttu-id="81583-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81583-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81583-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81583-119">CommonParameters</span></span>
<span data-ttu-id="81583-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81583-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81583-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81583-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81583-122">輸入</span><span class="sxs-lookup"><span data-stu-id="81583-122">INPUTS</span></span>

## <span data-ttu-id="81583-123">輸出</span><span class="sxs-lookup"><span data-stu-id="81583-123">OUTPUTS</span></span>

### <span data-ttu-id="81583-124">RuleWebhookAction 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="81583-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="81583-125">筆記</span><span class="sxs-lookup"><span data-stu-id="81583-125">NOTES</span></span>

## <span data-ttu-id="81583-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="81583-126">RELATED LINKS</span></span>

[<span data-ttu-id="81583-127">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="81583-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="81583-128">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="81583-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="81583-129">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="81583-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="81583-130">新-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="81583-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="81583-131">新-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="81583-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


