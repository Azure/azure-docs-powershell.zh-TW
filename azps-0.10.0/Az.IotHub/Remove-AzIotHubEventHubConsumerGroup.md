---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: e2b6bb4c58be90b205fc4a50ddab9c84c0d1ee20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794705"
---
# <span data-ttu-id="b0106-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b0106-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b0106-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0106-102">SYNOPSIS</span></span>
<span data-ttu-id="b0106-103">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="b0106-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b0106-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0106-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0106-105">說明</span><span class="sxs-lookup"><span data-stu-id="b0106-105">DESCRIPTION</span></span>
<span data-ttu-id="b0106-106">刪除 eventhub consumergroup。</span><span class="sxs-lookup"><span data-stu-id="b0106-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b0106-107">示例</span><span class="sxs-lookup"><span data-stu-id="b0106-107">EXAMPLES</span></span>

### <span data-ttu-id="b0106-108">範例1從遙測 eventhub 中移除 eventhub consumergroup</span><span class="sxs-lookup"><span data-stu-id="b0106-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="b0106-109">從名為 "myiothub" 的 IotHub 中移除名為 myconsumergroup 的 consumergroup</span><span class="sxs-lookup"><span data-stu-id="b0106-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b0106-110">參數</span><span class="sxs-lookup"><span data-stu-id="b0106-110">PARAMETERS</span></span>

### <span data-ttu-id="b0106-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0106-111">-DefaultProfile</span></span>
<span data-ttu-id="b0106-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b0106-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0106-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b0106-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b0106-114">EventHub ConsumerGroup Name。</span><span class="sxs-lookup"><span data-stu-id="b0106-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="b0106-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0106-115">-Name</span></span>
<span data-ttu-id="b0106-116">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b0106-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="b0106-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0106-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0106-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b0106-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b0106-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b0106-119">-Confirm</span></span>
<span data-ttu-id="b0106-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b0106-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0106-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0106-121">-WhatIf</span></span>
<span data-ttu-id="b0106-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b0106-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0106-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0106-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0106-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0106-124">CommonParameters</span></span>
<span data-ttu-id="b0106-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0106-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0106-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0106-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0106-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b0106-127">INPUTS</span></span>

### <span data-ttu-id="b0106-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b0106-128">System.String</span></span>

## <span data-ttu-id="b0106-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b0106-129">OUTPUTS</span></span>

### <span data-ttu-id="b0106-130">System.object</span><span class="sxs-lookup"><span data-stu-id="b0106-130">System.String</span></span>

## <span data-ttu-id="b0106-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b0106-131">NOTES</span></span>

## <span data-ttu-id="b0106-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0106-132">RELATED LINKS</span></span>
