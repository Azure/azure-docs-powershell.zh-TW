---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: f4899d55919f8b3c08b36babc448f1594f4ac4c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959677"
---
# <span data-ttu-id="59c96-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="59c96-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="59c96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="59c96-102">SYNOPSIS</span></span>
<span data-ttu-id="59c96-103">針對特定主題的訂閱建立新規則。</span><span class="sxs-lookup"><span data-stu-id="59c96-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="59c96-104">句法</span><span class="sxs-lookup"><span data-stu-id="59c96-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59c96-105">說明</span><span class="sxs-lookup"><span data-stu-id="59c96-105">DESCRIPTION</span></span>
<span data-ttu-id="59c96-106">**AzServiceBusRule** Cmdlet 會在指定的主題訂閱中，取得指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="59c96-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="59c96-107">示例</span><span class="sxs-lookup"><span data-stu-id="59c96-107">EXAMPLES</span></span>

### <span data-ttu-id="59c96-108">範例1</span><span class="sxs-lookup"><span data-stu-id="59c96-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="59c96-109">針對指定的訂閱傳回指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="59c96-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="59c96-110">範例2</span><span class="sxs-lookup"><span data-stu-id="59c96-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="59c96-111">傳回指定訂閱的規則描述清單。</span><span class="sxs-lookup"><span data-stu-id="59c96-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="59c96-112">預設會傳回100規則，如果傳回超過100個規則，請使用-MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="59c96-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="59c96-113">範例3</span><span class="sxs-lookup"><span data-stu-id="59c96-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="59c96-114">傳回指定訂閱之前150規則描述的清單。</span><span class="sxs-lookup"><span data-stu-id="59c96-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="59c96-115">參數</span><span class="sxs-lookup"><span data-stu-id="59c96-115">PARAMETERS</span></span>

### <span data-ttu-id="59c96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c96-116">-DefaultProfile</span></span>
<span data-ttu-id="59c96-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="59c96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c96-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="59c96-118">-MaxCount</span></span>
<span data-ttu-id="59c96-119">決定要傳回的規則數目上限。</span><span class="sxs-lookup"><span data-stu-id="59c96-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="59c96-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="59c96-120">-Name</span></span>
<span data-ttu-id="59c96-121">規則名稱</span><span class="sxs-lookup"><span data-stu-id="59c96-121">Rule Name</span></span>

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

### <span data-ttu-id="59c96-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="59c96-122">-Namespace</span></span>
<span data-ttu-id="59c96-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="59c96-123">Namespace Name</span></span>

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

### <span data-ttu-id="59c96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c96-124">-ResourceGroupName</span></span>
<span data-ttu-id="59c96-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="59c96-125">The name of the resource group</span></span>

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

### <span data-ttu-id="59c96-126">-訂閱</span><span class="sxs-lookup"><span data-stu-id="59c96-126">-Subscription</span></span>
<span data-ttu-id="59c96-127">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="59c96-127">Subscription Name</span></span>

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

### <span data-ttu-id="59c96-128">-主題</span><span class="sxs-lookup"><span data-stu-id="59c96-128">-Topic</span></span>
<span data-ttu-id="59c96-129">主題名稱</span><span class="sxs-lookup"><span data-stu-id="59c96-129">Topic Name</span></span>

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

### <span data-ttu-id="59c96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c96-130">CommonParameters</span></span>
<span data-ttu-id="59c96-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="59c96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c96-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="59c96-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c96-133">輸入</span><span class="sxs-lookup"><span data-stu-id="59c96-133">INPUTS</span></span>

### <span data-ttu-id="59c96-134">System.object</span><span class="sxs-lookup"><span data-stu-id="59c96-134">System.String</span></span>

## <span data-ttu-id="59c96-135">輸出</span><span class="sxs-lookup"><span data-stu-id="59c96-135">OUTPUTS</span></span>

### <span data-ttu-id="59c96-136">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="59c96-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="59c96-137">筆記</span><span class="sxs-lookup"><span data-stu-id="59c96-137">NOTES</span></span>

## <span data-ttu-id="59c96-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="59c96-138">RELATED LINKS</span></span>
