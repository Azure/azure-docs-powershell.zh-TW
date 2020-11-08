---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969680"
---
# <span data-ttu-id="a0e74-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0e74-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="a0e74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0e74-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e74-103">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="a0e74-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="a0e74-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0e74-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0e74-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0e74-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e74-106">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="a0e74-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="a0e74-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0e74-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e74-108">範例1從遙測 eventhub 中移除 eventhub consumergroup</span><span class="sxs-lookup"><span data-stu-id="a0e74-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="a0e74-109">從名為 "myiothub" 的 IotHub 中移除名為 myconsumergroup 的 consumergroup</span><span class="sxs-lookup"><span data-stu-id="a0e74-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a0e74-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0e74-110">PARAMETERS</span></span>

### <span data-ttu-id="a0e74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e74-111">-DefaultProfile</span></span>
<span data-ttu-id="a0e74-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a0e74-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0e74-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e74-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="a0e74-114">EventHub ConsumerGroup Name。</span><span class="sxs-lookup"><span data-stu-id="a0e74-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0e74-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0e74-115">-Name</span></span>
<span data-ttu-id="a0e74-116">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="a0e74-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="a0e74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e74-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0e74-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a0e74-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a0e74-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a0e74-119">-Confirm</span></span>
<span data-ttu-id="a0e74-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0e74-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0e74-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0e74-121">-WhatIf</span></span>
<span data-ttu-id="a0e74-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0e74-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0e74-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0e74-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0e74-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e74-124">CommonParameters</span></span>
<span data-ttu-id="a0e74-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0e74-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e74-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0e74-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e74-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a0e74-127">INPUTS</span></span>

### <span data-ttu-id="a0e74-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a0e74-128">System.String</span></span>

## <span data-ttu-id="a0e74-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a0e74-129">OUTPUTS</span></span>

### <span data-ttu-id="a0e74-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a0e74-130">System.String</span></span>

## <span data-ttu-id="a0e74-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a0e74-131">NOTES</span></span>

## <span data-ttu-id="a0e74-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0e74-132">RELATED LINKS</span></span>
