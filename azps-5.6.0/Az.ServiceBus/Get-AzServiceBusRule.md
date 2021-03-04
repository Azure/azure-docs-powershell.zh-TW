---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0dc9c54b3d2a080d7bb40c8560371b31f4ad3acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912590"
---
# <span data-ttu-id="88b71-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="88b71-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="88b71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88b71-102">SYNOPSIS</span></span>
<span data-ttu-id="88b71-103">在給定的主題訂閱中，取回現有規則的定義。</span><span class="sxs-lookup"><span data-stu-id="88b71-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="88b71-104">語法</span><span class="sxs-lookup"><span data-stu-id="88b71-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88b71-105">描述</span><span class="sxs-lookup"><span data-stu-id="88b71-105">DESCRIPTION</span></span>
<span data-ttu-id="88b71-106">**Get-AzServiceBusRule** Cmdlet 會取得指定主題訂閱中指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="88b71-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="88b71-107">例子</span><span class="sxs-lookup"><span data-stu-id="88b71-107">EXAMPLES</span></span>

### <span data-ttu-id="88b71-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="88b71-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="88b71-109">會針對指定的訂閱，返回指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="88b71-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="88b71-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="88b71-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="88b71-111">會針對指定的訂閱，返回規則描述清單。</span><span class="sxs-lookup"><span data-stu-id="88b71-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="88b71-112">根據預設，會返回 100 個規則，如果要退回的規則超過 100 個，請使用 -MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="88b71-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="88b71-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="88b71-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="88b71-114">會針對指定的訂閱，返回前 150 個規則描述的清單。</span><span class="sxs-lookup"><span data-stu-id="88b71-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="88b71-115">參數</span><span class="sxs-lookup"><span data-stu-id="88b71-115">PARAMETERS</span></span>

### <span data-ttu-id="88b71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b71-116">-DefaultProfile</span></span>
<span data-ttu-id="88b71-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88b71-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b71-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="88b71-118">-MaxCount</span></span>
<span data-ttu-id="88b71-119">決定要退回的規則數上限。</span><span class="sxs-lookup"><span data-stu-id="88b71-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="88b71-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="88b71-120">-Name</span></span>
<span data-ttu-id="88b71-121">規則名稱</span><span class="sxs-lookup"><span data-stu-id="88b71-121">Rule Name</span></span>

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

### <span data-ttu-id="88b71-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="88b71-122">-Namespace</span></span>
<span data-ttu-id="88b71-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="88b71-123">Namespace Name</span></span>

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

### <span data-ttu-id="88b71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b71-124">-ResourceGroupName</span></span>
<span data-ttu-id="88b71-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="88b71-125">The name of the resource group</span></span>

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

### <span data-ttu-id="88b71-126">-訂閱</span><span class="sxs-lookup"><span data-stu-id="88b71-126">-Subscription</span></span>
<span data-ttu-id="88b71-127">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="88b71-127">Subscription Name</span></span>

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

### <span data-ttu-id="88b71-128">-主題</span><span class="sxs-lookup"><span data-stu-id="88b71-128">-Topic</span></span>
<span data-ttu-id="88b71-129">主題名稱</span><span class="sxs-lookup"><span data-stu-id="88b71-129">Topic Name</span></span>

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

### <span data-ttu-id="88b71-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b71-130">CommonParameters</span></span>
<span data-ttu-id="88b71-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88b71-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b71-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="88b71-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b71-133">輸入</span><span class="sxs-lookup"><span data-stu-id="88b71-133">INPUTS</span></span>

### <span data-ttu-id="88b71-134">System.String</span><span class="sxs-lookup"><span data-stu-id="88b71-134">System.String</span></span>

## <span data-ttu-id="88b71-135">輸出</span><span class="sxs-lookup"><span data-stu-id="88b71-135">OUTPUTS</span></span>

### <span data-ttu-id="88b71-136">Microsoft.Azure.Commands.ServiceBus.models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="88b71-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="88b71-137">筆記</span><span class="sxs-lookup"><span data-stu-id="88b71-137">NOTES</span></span>

## <span data-ttu-id="88b71-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="88b71-138">RELATED LINKS</span></span>
