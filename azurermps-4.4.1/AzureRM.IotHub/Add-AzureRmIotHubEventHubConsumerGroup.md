---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 19a3098eff598c223014b65381e524d063f7d425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624812"
---
# <span data-ttu-id="8a646-101">Add-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8a646-101">Add-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="8a646-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a646-102">SYNOPSIS</span></span>
<span data-ttu-id="8a646-103">建立 eventhub 消費者群組。</span><span class="sxs-lookup"><span data-stu-id="8a646-103">Creates an eventhub consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a646-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a646-104">SYNTAX</span></span>

```
Add-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a646-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a646-105">DESCRIPTION</span></span>
<span data-ttu-id="8a646-106">在與指定 IotHub 相關聯的 Eventhub 中建立消費者群組。</span><span class="sxs-lookup"><span data-stu-id="8a646-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="8a646-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a646-107">EXAMPLES</span></span>

### <span data-ttu-id="8a646-108">範例1：將消費者群組新增至遙測 eventhub</span><span class="sxs-lookup"><span data-stu-id="8a646-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="8a646-109">將名為 "myconsumergroup" 的新 consumergroup，新增到名為 "myiothub" 的 iothub 中的 [] 的 eventhub 事件</span><span class="sxs-lookup"><span data-stu-id="8a646-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

### <span data-ttu-id="8a646-110">範例2：將消費者群組新增至作業監視 eventhub</span><span class="sxs-lookup"><span data-stu-id="8a646-110">Example 2: Add a consumer group to the operations monitoring eventhub</span></span>
```
PS C:\> Add-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="8a646-111">在名為 "myiothub" 的 iothub 中，將名為 "myconsumergroup" 的新 consumergroup 新增至 eventhub，以取得操作監視事件</span><span class="sxs-lookup"><span data-stu-id="8a646-111">Adds a new consumergroup named "myconsumergroup" to the eventhub for operations monitoring events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="8a646-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a646-112">PARAMETERS</span></span>

### <span data-ttu-id="8a646-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="8a646-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="8a646-114">您想要新增的 EventHub ConsumerGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a646-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a646-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="8a646-115">-EventHubEndpointName</span></span>
<span data-ttu-id="8a646-116">EventHub 端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a646-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="8a646-117">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="8a646-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a646-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a646-118">-Name</span></span>
<span data-ttu-id="8a646-119">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="8a646-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a646-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a646-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a646-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a646-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="8a646-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8a646-122">-Confirm</span></span>
<span data-ttu-id="8a646-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a646-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a646-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a646-124">-WhatIf</span></span>
<span data-ttu-id="8a646-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a646-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a646-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a646-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a646-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a646-127">-DefaultProfile</span></span>
<span data-ttu-id="8a646-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a646-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a646-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a646-129">CommonParameters</span></span>
<span data-ttu-id="8a646-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a646-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a646-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a646-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a646-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8a646-132">INPUTS</span></span>

### <span data-ttu-id="8a646-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8a646-133">System.String</span></span>

## <span data-ttu-id="8a646-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8a646-134">OUTPUTS</span></span>

### <span data-ttu-id="8a646-135">System.object. IEnumerable "1 [[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8a646-135">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="8a646-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8a646-136">NOTES</span></span>

## <span data-ttu-id="8a646-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a646-137">RELATED LINKS</span></span>

