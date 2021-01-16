---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279139"
---
# <span data-ttu-id="90484-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="90484-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="90484-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90484-102">SYNOPSIS</span></span>
<span data-ttu-id="90484-103">在指定的主題訂閱中，檢索現有規則的定義。</span><span class="sxs-lookup"><span data-stu-id="90484-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="90484-104">句法</span><span class="sxs-lookup"><span data-stu-id="90484-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90484-105">說明</span><span class="sxs-lookup"><span data-stu-id="90484-105">DESCRIPTION</span></span>
<span data-ttu-id="90484-106">**AzServiceBusRule** Cmdlet 會在指定的主題訂閱中，取得指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="90484-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="90484-107">示例</span><span class="sxs-lookup"><span data-stu-id="90484-107">EXAMPLES</span></span>

### <span data-ttu-id="90484-108">範例1</span><span class="sxs-lookup"><span data-stu-id="90484-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="90484-109">針對指定的訂閱傳回指定的規則描述。</span><span class="sxs-lookup"><span data-stu-id="90484-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="90484-110">範例2</span><span class="sxs-lookup"><span data-stu-id="90484-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="90484-111">傳回指定訂閱的規則描述清單。</span><span class="sxs-lookup"><span data-stu-id="90484-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="90484-112">預設會傳回100規則，如果傳回超過100個規則，請使用-MaxCount 參數。</span><span class="sxs-lookup"><span data-stu-id="90484-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="90484-113">範例3</span><span class="sxs-lookup"><span data-stu-id="90484-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="90484-114">傳回指定訂閱之前150規則描述的清單。</span><span class="sxs-lookup"><span data-stu-id="90484-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="90484-115">參數</span><span class="sxs-lookup"><span data-stu-id="90484-115">PARAMETERS</span></span>

### <span data-ttu-id="90484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90484-116">-DefaultProfile</span></span>
<span data-ttu-id="90484-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90484-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="90484-118">-MaxCount</span></span>
<span data-ttu-id="90484-119">決定要傳回的規則數目上限。</span><span class="sxs-lookup"><span data-stu-id="90484-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="90484-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="90484-120">-Name</span></span>
<span data-ttu-id="90484-121">規則名稱</span><span class="sxs-lookup"><span data-stu-id="90484-121">Rule Name</span></span>

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

### <span data-ttu-id="90484-122">-命名空間</span><span class="sxs-lookup"><span data-stu-id="90484-122">-Namespace</span></span>
<span data-ttu-id="90484-123">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="90484-123">Namespace Name</span></span>

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

### <span data-ttu-id="90484-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90484-124">-ResourceGroupName</span></span>
<span data-ttu-id="90484-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="90484-125">The name of the resource group</span></span>

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

### <span data-ttu-id="90484-126">-訂閱</span><span class="sxs-lookup"><span data-stu-id="90484-126">-Subscription</span></span>
<span data-ttu-id="90484-127">訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="90484-127">Subscription Name</span></span>

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

### <span data-ttu-id="90484-128">-主題</span><span class="sxs-lookup"><span data-stu-id="90484-128">-Topic</span></span>
<span data-ttu-id="90484-129">主題名稱</span><span class="sxs-lookup"><span data-stu-id="90484-129">Topic Name</span></span>

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

### <span data-ttu-id="90484-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90484-130">CommonParameters</span></span>
<span data-ttu-id="90484-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90484-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90484-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90484-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90484-133">輸入</span><span class="sxs-lookup"><span data-stu-id="90484-133">INPUTS</span></span>

### <span data-ttu-id="90484-134">System.object</span><span class="sxs-lookup"><span data-stu-id="90484-134">System.String</span></span>

## <span data-ttu-id="90484-135">輸出</span><span class="sxs-lookup"><span data-stu-id="90484-135">OUTPUTS</span></span>

### <span data-ttu-id="90484-136">PSRulesAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="90484-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="90484-137">筆記</span><span class="sxs-lookup"><span data-stu-id="90484-137">NOTES</span></span>

## <span data-ttu-id="90484-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="90484-138">RELATED LINKS</span></span>
