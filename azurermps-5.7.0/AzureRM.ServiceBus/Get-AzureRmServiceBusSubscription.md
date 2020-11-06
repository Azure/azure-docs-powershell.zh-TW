---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 3d99b261dc65af5d19a93acb575116a91c8a97fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454083"
---
# <span data-ttu-id="07c6e-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="07c6e-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="07c6e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="07c6e-103">傳回指定主題的訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="07c6e-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c6e-104">句法</span><span class="sxs-lookup"><span data-stu-id="07c6e-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c6e-105">說明</span><span class="sxs-lookup"><span data-stu-id="07c6e-105">DESCRIPTION</span></span>
<span data-ttu-id="07c6e-106">**AzureRmServiceBusSubscription** Cmdlet 會針對指定的服務匯流排主題傳回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="07c6e-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="07c6e-107">示例</span><span class="sxs-lookup"><span data-stu-id="07c6e-107">EXAMPLES</span></span>

### <span data-ttu-id="07c6e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="07c6e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="07c6e-109">針對指定的服務匯流排主題，返回訂閱描述。</span><span class="sxs-lookup"><span data-stu-id="07c6e-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="07c6e-110">參數</span><span class="sxs-lookup"><span data-stu-id="07c6e-110">PARAMETERS</span></span>

### <span data-ttu-id="07c6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c6e-111">-DefaultProfile</span></span>
<span data-ttu-id="07c6e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07c6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c6e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="07c6e-113">-Name</span></span>
<span data-ttu-id="07c6e-114">訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="07c6e-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07c6e-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="07c6e-115">-Namespace</span></span>
<span data-ttu-id="07c6e-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="07c6e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="07c6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07c6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="07c6e-118">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="07c6e-118">The name of the resource group</span></span>

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

### <span data-ttu-id="07c6e-119">-主題</span><span class="sxs-lookup"><span data-stu-id="07c6e-119">-Topic</span></span>
<span data-ttu-id="07c6e-120">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="07c6e-120">Topic Name.</span></span>

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

### <span data-ttu-id="07c6e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c6e-121">CommonParameters</span></span>
<span data-ttu-id="07c6e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07c6e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c6e-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07c6e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c6e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="07c6e-124">INPUTS</span></span>

### <span data-ttu-id="07c6e-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="07c6e-125">-ResourceGroup</span></span>
 <span data-ttu-id="07c6e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="07c6e-126">System.String</span></span>
 

### <span data-ttu-id="07c6e-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="07c6e-127">-NamespaceName</span></span>
 <span data-ttu-id="07c6e-128">System.object</span><span class="sxs-lookup"><span data-stu-id="07c6e-128">System.String</span></span>
 

### <span data-ttu-id="07c6e-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="07c6e-129">-TopicName</span></span>
 <span data-ttu-id="07c6e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="07c6e-130">System.String</span></span>
 

### <span data-ttu-id="07c6e-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="07c6e-131">-SubscriptionName</span></span>
 <span data-ttu-id="07c6e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="07c6e-132">System.String</span></span>
 

## <span data-ttu-id="07c6e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="07c6e-133">OUTPUTS</span></span>

### <span data-ttu-id="07c6e-134">PSSubscriptionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07c6e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="07c6e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="07c6e-135">NOTES</span></span>

## <span data-ttu-id="07c6e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="07c6e-136">RELATED LINKS</span></span>

