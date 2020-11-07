---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 59a180d422a27ca9d2c3e1e4932d843ba7c70093
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787493"
---
# <span data-ttu-id="60d0f-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="60d0f-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="60d0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="60d0f-103">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="60d0f-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="60d0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="60d0f-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60d0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="60d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="60d0f-106">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="60d0f-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="60d0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="60d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="60d0f-108">範例1從遙測 eventhub 中移除 eventhub consumergroup</span><span class="sxs-lookup"><span data-stu-id="60d0f-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="60d0f-109">從名為 "myiothub" 的 IotHub 中移除名為 myconsumergroup 的 consumergroup</span><span class="sxs-lookup"><span data-stu-id="60d0f-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="60d0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="60d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="60d0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d0f-111">-DefaultProfile</span></span>
<span data-ttu-id="60d0f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="60d0f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60d0f-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="60d0f-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="60d0f-114">EventHub ConsumerGroup Name。</span><span class="sxs-lookup"><span data-stu-id="60d0f-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60d0f-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="60d0f-115">-EventHubEndpointName</span></span>
<span data-ttu-id="60d0f-116">EventHub 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="60d0f-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="60d0f-117">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="60d0f-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="60d0f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="60d0f-118">-Name</span></span>
<span data-ttu-id="60d0f-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="60d0f-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="60d0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="60d0f-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="60d0f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="60d0f-122">-確認</span><span class="sxs-lookup"><span data-stu-id="60d0f-122">-Confirm</span></span>
<span data-ttu-id="60d0f-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60d0f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60d0f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60d0f-124">-WhatIf</span></span>
<span data-ttu-id="60d0f-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60d0f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60d0f-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60d0f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60d0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d0f-127">CommonParameters</span></span>
<span data-ttu-id="60d0f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60d0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d0f-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60d0f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d0f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="60d0f-130">INPUTS</span></span>

### <span data-ttu-id="60d0f-131">System.object</span><span class="sxs-lookup"><span data-stu-id="60d0f-131">System.String</span></span>

## <span data-ttu-id="60d0f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="60d0f-132">OUTPUTS</span></span>

### <span data-ttu-id="60d0f-133">System.object</span><span class="sxs-lookup"><span data-stu-id="60d0f-133">System.String</span></span>

## <span data-ttu-id="60d0f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="60d0f-134">NOTES</span></span>

## <span data-ttu-id="60d0f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="60d0f-135">RELATED LINKS</span></span>
