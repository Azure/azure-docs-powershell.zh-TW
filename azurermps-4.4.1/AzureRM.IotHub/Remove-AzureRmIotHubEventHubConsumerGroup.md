---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455783"
---
# <span data-ttu-id="b1789-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b1789-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b1789-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1789-102">SYNOPSIS</span></span>
<span data-ttu-id="b1789-103">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="b1789-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1789-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1789-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1789-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1789-105">DESCRIPTION</span></span>
<span data-ttu-id="b1789-106">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="b1789-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b1789-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1789-107">EXAMPLES</span></span>

### <span data-ttu-id="b1789-108">範例1從遙測 eventhub 中移除 eventhub consumergroup</span><span class="sxs-lookup"><span data-stu-id="b1789-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="b1789-109">從名為 "myiothub" 的 IotHub 中移除名為 myconsumergroup 的 consumergroup</span><span class="sxs-lookup"><span data-stu-id="b1789-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b1789-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1789-110">PARAMETERS</span></span>

### <span data-ttu-id="b1789-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b1789-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b1789-112">EventHub ConsumerGroup Name。</span><span class="sxs-lookup"><span data-stu-id="b1789-112">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="b1789-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b1789-113">-EventHubEndpointName</span></span>
<span data-ttu-id="b1789-114">EventHub 端點名稱。</span><span class="sxs-lookup"><span data-stu-id="b1789-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="b1789-115">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="b1789-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="b1789-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1789-116">-Name</span></span>
<span data-ttu-id="b1789-117">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b1789-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b1789-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1789-118">-ResourceGroupName</span></span>
<span data-ttu-id="b1789-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b1789-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b1789-120">-確認</span><span class="sxs-lookup"><span data-stu-id="b1789-120">-Confirm</span></span>
<span data-ttu-id="b1789-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1789-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1789-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1789-122">-WhatIf</span></span>
<span data-ttu-id="b1789-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1789-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1789-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1789-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1789-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1789-125">-DefaultProfile</span></span>
<span data-ttu-id="b1789-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1789-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1789-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1789-127">CommonParameters</span></span>
<span data-ttu-id="b1789-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1789-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1789-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1789-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1789-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b1789-130">INPUTS</span></span>

### <span data-ttu-id="b1789-131">System.object</span><span class="sxs-lookup"><span data-stu-id="b1789-131">System.String</span></span>

## <span data-ttu-id="b1789-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b1789-132">OUTPUTS</span></span>

### <span data-ttu-id="b1789-133">System.object. IEnumerable "1 [[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b1789-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b1789-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b1789-134">NOTES</span></span>

## <span data-ttu-id="b1789-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1789-135">RELATED LINKS</span></span>

