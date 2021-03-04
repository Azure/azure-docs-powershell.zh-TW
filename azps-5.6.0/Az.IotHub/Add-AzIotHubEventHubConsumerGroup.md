---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 23f6c4b7d40f0ec2e02541f82d5d517019bd15fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913873"
---
# <span data-ttu-id="c18b5-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c18b5-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c18b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c18b5-102">SYNOPSIS</span></span>
<span data-ttu-id="c18b5-103">建立 eventhub 消費者群組。</span><span class="sxs-lookup"><span data-stu-id="c18b5-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="c18b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="c18b5-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c18b5-105">描述</span><span class="sxs-lookup"><span data-stu-id="c18b5-105">DESCRIPTION</span></span>
<span data-ttu-id="c18b5-106">在與指定的 IotHub 相關聯的 Eventhub 中建立消費者群組。</span><span class="sxs-lookup"><span data-stu-id="c18b5-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="c18b5-107">例子</span><span class="sxs-lookup"><span data-stu-id="c18b5-107">EXAMPLES</span></span>

### <span data-ttu-id="c18b5-108">範例 1：新增消費者群組至遙測事件hub</span><span class="sxs-lookup"><span data-stu-id="c18b5-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="c18b5-109">新增名為「myconsumergroup」的新消費者組至 iothub 中名為「myiothub」的遙測事件事件</span><span class="sxs-lookup"><span data-stu-id="c18b5-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="c18b5-110">參數</span><span class="sxs-lookup"><span data-stu-id="c18b5-110">PARAMETERS</span></span>

### <span data-ttu-id="c18b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18b5-111">-DefaultProfile</span></span>
<span data-ttu-id="c18b5-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c18b5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c18b5-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="c18b5-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="c18b5-114">您想要新增的 EventHub ConsumerGroup 名稱。</span><span class="sxs-lookup"><span data-stu-id="c18b5-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

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

### <span data-ttu-id="c18b5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c18b5-115">-Name</span></span>
<span data-ttu-id="c18b5-116">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c18b5-116">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c18b5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c18b5-117">-ResourceGroupName</span></span>
<span data-ttu-id="c18b5-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c18b5-118">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="c18b5-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c18b5-119">-Confirm</span></span>
<span data-ttu-id="c18b5-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c18b5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c18b5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c18b5-121">-WhatIf</span></span>
<span data-ttu-id="c18b5-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c18b5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c18b5-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c18b5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c18b5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18b5-124">CommonParameters</span></span>
<span data-ttu-id="c18b5-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c18b5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18b5-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c18b5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18b5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c18b5-127">INPUTS</span></span>

### <span data-ttu-id="c18b5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c18b5-128">System.String</span></span>

## <span data-ttu-id="c18b5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c18b5-129">OUTPUTS</span></span>

### <span data-ttu-id="c18b5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c18b5-130">System.String</span></span>

## <span data-ttu-id="c18b5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c18b5-131">NOTES</span></span>

## <span data-ttu-id="c18b5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c18b5-132">RELATED LINKS</span></span>
