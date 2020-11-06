---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453259"
---
# <span data-ttu-id="87cd0-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="87cd0-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="87cd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="87cd0-103">取得指定服務匯流排佇列的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="87cd0-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87cd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="87cd0-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87cd0-105">說明</span><span class="sxs-lookup"><span data-stu-id="87cd0-105">DESCRIPTION</span></span>
<span data-ttu-id="87cd0-106">**AzureRmServiceBusQueueKey** Cmdlet 會傳回指定服務匯流排佇列的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="87cd0-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="87cd0-107">示例</span><span class="sxs-lookup"><span data-stu-id="87cd0-107">EXAMPLES</span></span>

### <span data-ttu-id="87cd0-108">範例1</span><span class="sxs-lookup"><span data-stu-id="87cd0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="87cd0-109">傳回指定服務匯流排佇列的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="87cd0-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="87cd0-110">參數</span><span class="sxs-lookup"><span data-stu-id="87cd0-110">PARAMETERS</span></span>

### <span data-ttu-id="87cd0-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87cd0-111">-ResourceGroup</span></span>
<span data-ttu-id="87cd0-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87cd0-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="87cd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cd0-113">-DefaultProfile</span></span>
<span data-ttu-id="87cd0-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87cd0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87cd0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="87cd0-115">-Name</span></span>
<span data-ttu-id="87cd0-116">[AuthorizationRule] 佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="87cd0-116">ServiceBus Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cd0-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="87cd0-117">-Namespace</span></span>
<span data-ttu-id="87cd0-118">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="87cd0-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cd0-119">-佇列</span><span class="sxs-lookup"><span data-stu-id="87cd0-119">-Queue</span></span>
<span data-ttu-id="87cd0-120">[一排佇列名稱]。</span><span class="sxs-lookup"><span data-stu-id="87cd0-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87cd0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cd0-121">CommonParameters</span></span>
<span data-ttu-id="87cd0-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87cd0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cd0-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87cd0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cd0-124">輸入</span><span class="sxs-lookup"><span data-stu-id="87cd0-124">INPUTS</span></span>

### <span data-ttu-id="87cd0-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87cd0-125">-ResourceGroup</span></span>
 <span data-ttu-id="87cd0-126">System.object</span><span class="sxs-lookup"><span data-stu-id="87cd0-126">System.String</span></span>
 

### <span data-ttu-id="87cd0-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="87cd0-127">-NamespaceName</span></span>
 <span data-ttu-id="87cd0-128">System.object</span><span class="sxs-lookup"><span data-stu-id="87cd0-128">System.String</span></span>
 

### <span data-ttu-id="87cd0-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="87cd0-129">-QueueName</span></span>
 <span data-ttu-id="87cd0-130">System.object</span><span class="sxs-lookup"><span data-stu-id="87cd0-130">System.String</span></span>
 

### <span data-ttu-id="87cd0-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="87cd0-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="87cd0-132">System.object</span><span class="sxs-lookup"><span data-stu-id="87cd0-132">System.String</span></span>

## <span data-ttu-id="87cd0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="87cd0-133">OUTPUTS</span></span>

### <span data-ttu-id="87cd0-134">ListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87cd0-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="87cd0-135">PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-Queue_e xampl1 SecondaryConnectionString： Endpoint = SB：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-Queue_e xampl1 PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="87cd0-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="87cd0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="87cd0-136">NOTES</span></span>

## <span data-ttu-id="87cd0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="87cd0-137">RELATED LINKS</span></span>

