---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624345"
---
# <span data-ttu-id="0db1b-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0db1b-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="0db1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0db1b-102">SYNOPSIS</span></span>
<span data-ttu-id="0db1b-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="0db1b-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0db1b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0db1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0db1b-105">DESCRIPTION</span></span>
<span data-ttu-id="0db1b-106">**AzureRmServiceBusRule** Cmdlet 會在指定的主題訂閱中，取得指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="0db1b-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="0db1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="0db1b-107">EXAMPLES</span></span>

### <span data-ttu-id="0db1b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0db1b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="0db1b-109">針對指定的訂閱傳回指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="0db1b-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="0db1b-110">範例2</span><span class="sxs-lookup"><span data-stu-id="0db1b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="0db1b-111">傳回指定訂閱的規則描述清單。</span><span class="sxs-lookup"><span data-stu-id="0db1b-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="0db1b-112">預設會傳回100規則，如果傳回超過100個規則，請使用-MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="0db1b-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="0db1b-113">範例3</span><span class="sxs-lookup"><span data-stu-id="0db1b-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="0db1b-114">傳回指定訂閱之前150規則描述的清單。</span><span class="sxs-lookup"><span data-stu-id="0db1b-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="0db1b-115">參數</span><span class="sxs-lookup"><span data-stu-id="0db1b-115">PARAMETERS</span></span>

### <span data-ttu-id="0db1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db1b-116">-DefaultProfile</span></span>
<span data-ttu-id="0db1b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0db1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db1b-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0db1b-118">-MaxCount</span></span>
<span data-ttu-id="0db1b-119">決定要傳回的規則數目上限。</span><span class="sxs-lookup"><span data-stu-id="0db1b-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db1b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0db1b-120">-Name</span></span>
<span data-ttu-id="0db1b-121">規則名稱</span><span class="sxs-lookup"><span data-stu-id="0db1b-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db1b-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0db1b-122">-Namespace</span></span>
<span data-ttu-id="0db1b-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="0db1b-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0db1b-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="0db1b-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db1b-126">-訂閱</span><span class="sxs-lookup"><span data-stu-id="0db1b-126">-Subscription</span></span>
<span data-ttu-id="0db1b-127">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="0db1b-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db1b-128">-主題</span><span class="sxs-lookup"><span data-stu-id="0db1b-128">-Topic</span></span>
<span data-ttu-id="0db1b-129">主題名稱</span><span class="sxs-lookup"><span data-stu-id="0db1b-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db1b-130">CommonParameters</span></span>
<span data-ttu-id="0db1b-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0db1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db1b-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0db1b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db1b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0db1b-133">INPUTS</span></span>

### <span data-ttu-id="0db1b-134">System.object</span><span class="sxs-lookup"><span data-stu-id="0db1b-134">System.String</span></span>

## <span data-ttu-id="0db1b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0db1b-135">OUTPUTS</span></span>

### <span data-ttu-id="0db1b-136">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0db1b-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0db1b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0db1b-137">NOTES</span></span>

## <span data-ttu-id="0db1b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0db1b-138">RELATED LINKS</span></span>
