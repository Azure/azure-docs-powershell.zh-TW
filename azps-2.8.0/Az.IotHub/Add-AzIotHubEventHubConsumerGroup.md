---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 938949ae1eada6d85bb6e01728f5be09655c3e06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612243"
---
# <span data-ttu-id="27581-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="27581-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="27581-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27581-102">SYNOPSIS</span></span>
<span data-ttu-id="27581-103">建立 eventhub 消費者群組。</span><span class="sxs-lookup"><span data-stu-id="27581-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="27581-104">句法</span><span class="sxs-lookup"><span data-stu-id="27581-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27581-105">說明</span><span class="sxs-lookup"><span data-stu-id="27581-105">DESCRIPTION</span></span>
<span data-ttu-id="27581-106">在與指定 IotHub 相關聯的 Eventhub 中建立消費者群組。</span><span class="sxs-lookup"><span data-stu-id="27581-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="27581-107">示例</span><span class="sxs-lookup"><span data-stu-id="27581-107">EXAMPLES</span></span>

### <span data-ttu-id="27581-108">範例1：將消費者群組新增至遙測 eventhub</span><span class="sxs-lookup"><span data-stu-id="27581-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="27581-109">將名為 "myconsumergroup" 的新 consumergroup，新增到名為 "myiothub" 的 iothub 中的 [] 的 eventhub 事件</span><span class="sxs-lookup"><span data-stu-id="27581-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="27581-110">參數</span><span class="sxs-lookup"><span data-stu-id="27581-110">PARAMETERS</span></span>

### <span data-ttu-id="27581-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27581-111">-DefaultProfile</span></span>
<span data-ttu-id="27581-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="27581-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27581-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="27581-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="27581-114">您想要新增的 EventHub ConsumerGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="27581-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="27581-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="27581-115">-EventHubEndpointName</span></span>
<span data-ttu-id="27581-116">EventHub 端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="27581-116">Name of the EventHub Endpoint.</span></span>
<span data-ttu-id="27581-117">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="27581-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27581-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="27581-118">-Name</span></span>
<span data-ttu-id="27581-119">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="27581-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27581-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27581-120">-ResourceGroupName</span></span>
<span data-ttu-id="27581-121">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27581-121">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="27581-122">-確認</span><span class="sxs-lookup"><span data-stu-id="27581-122">-Confirm</span></span>
<span data-ttu-id="27581-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27581-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27581-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27581-124">-WhatIf</span></span>
<span data-ttu-id="27581-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27581-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27581-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27581-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27581-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27581-127">CommonParameters</span></span>
<span data-ttu-id="27581-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27581-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27581-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27581-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27581-130">輸入</span><span class="sxs-lookup"><span data-stu-id="27581-130">INPUTS</span></span>

### <span data-ttu-id="27581-131">System.object</span><span class="sxs-lookup"><span data-stu-id="27581-131">System.String</span></span>

## <span data-ttu-id="27581-132">輸出</span><span class="sxs-lookup"><span data-stu-id="27581-132">OUTPUTS</span></span>

### <span data-ttu-id="27581-133">System.object</span><span class="sxs-lookup"><span data-stu-id="27581-133">System.String</span></span>

## <span data-ttu-id="27581-134">筆記</span><span class="sxs-lookup"><span data-stu-id="27581-134">NOTES</span></span>

## <span data-ttu-id="27581-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="27581-135">RELATED LINKS</span></span>
