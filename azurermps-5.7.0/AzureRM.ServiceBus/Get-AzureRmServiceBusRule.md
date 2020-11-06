---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454084"
---
# <span data-ttu-id="97311-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="97311-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="97311-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97311-102">SYNOPSIS</span></span>
<span data-ttu-id="97311-103">針對特定主題的相關訂閱取得指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="97311-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97311-104">句法</span><span class="sxs-lookup"><span data-stu-id="97311-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97311-105">說明</span><span class="sxs-lookup"><span data-stu-id="97311-105">DESCRIPTION</span></span>
<span data-ttu-id="97311-106">**AzureRmServiceBusRule** Cmdlet 會在指定的主題訂閱中，取得指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="97311-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="97311-107">示例</span><span class="sxs-lookup"><span data-stu-id="97311-107">EXAMPLES</span></span>

### <span data-ttu-id="97311-108">範例1</span><span class="sxs-lookup"><span data-stu-id="97311-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="97311-109">針對指定的訂閱傳回指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="97311-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="97311-110">參數</span><span class="sxs-lookup"><span data-stu-id="97311-110">PARAMETERS</span></span>

### <span data-ttu-id="97311-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97311-111">-DefaultProfile</span></span>
<span data-ttu-id="97311-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97311-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97311-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="97311-113">-Name</span></span>
<span data-ttu-id="97311-114">規則名稱。</span><span class="sxs-lookup"><span data-stu-id="97311-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97311-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="97311-115">-Namespace</span></span>
<span data-ttu-id="97311-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="97311-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97311-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97311-117">-ResourceGroupName</span></span>
<span data-ttu-id="97311-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="97311-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97311-119">-訂閱</span><span class="sxs-lookup"><span data-stu-id="97311-119">-Subscription</span></span>
<span data-ttu-id="97311-120">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="97311-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97311-121">-主題</span><span class="sxs-lookup"><span data-stu-id="97311-121">-Topic</span></span>
<span data-ttu-id="97311-122">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="97311-122">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97311-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97311-123">CommonParameters</span></span>
<span data-ttu-id="97311-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97311-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97311-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97311-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97311-126">輸入</span><span class="sxs-lookup"><span data-stu-id="97311-126">INPUTS</span></span>

### <span data-ttu-id="97311-127">System.object</span><span class="sxs-lookup"><span data-stu-id="97311-127">System.String</span></span>

## <span data-ttu-id="97311-128">輸出</span><span class="sxs-lookup"><span data-stu-id="97311-128">OUTPUTS</span></span>

### <span data-ttu-id="97311-129">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97311-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="97311-130">筆記</span><span class="sxs-lookup"><span data-stu-id="97311-130">NOTES</span></span>

## <span data-ttu-id="97311-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="97311-131">RELATED LINKS</span></span>

