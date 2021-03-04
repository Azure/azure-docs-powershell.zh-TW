---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 1e563126bb57986bed752184340808991f7e2a00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907634"
---
# <span data-ttu-id="2caef-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2caef-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="2caef-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2caef-102">SYNOPSIS</span></span>
<span data-ttu-id="2caef-103">刪除 eventhub 消費者組。</span><span class="sxs-lookup"><span data-stu-id="2caef-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="2caef-104">語法</span><span class="sxs-lookup"><span data-stu-id="2caef-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2caef-105">描述</span><span class="sxs-lookup"><span data-stu-id="2caef-105">DESCRIPTION</span></span>
<span data-ttu-id="2caef-106">刪除 eventhub 消費者組。</span><span class="sxs-lookup"><span data-stu-id="2caef-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="2caef-107">例子</span><span class="sxs-lookup"><span data-stu-id="2caef-107">EXAMPLES</span></span>

### <span data-ttu-id="2caef-108">範例 1 從遙測事件hub 移除 eventhub Consumergroup</span><span class="sxs-lookup"><span data-stu-id="2caef-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="2caef-109">從名為"myiothub" 的 IotHub 移除名為 myconsumergroup 的消費者組</span><span class="sxs-lookup"><span data-stu-id="2caef-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2caef-110">參數</span><span class="sxs-lookup"><span data-stu-id="2caef-110">PARAMETERS</span></span>

### <span data-ttu-id="2caef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2caef-111">-DefaultProfile</span></span>
<span data-ttu-id="2caef-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2caef-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2caef-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="2caef-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="2caef-114">EventHub ConsumerGroup 名稱。</span><span class="sxs-lookup"><span data-stu-id="2caef-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="2caef-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2caef-115">-Name</span></span>
<span data-ttu-id="2caef-116">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="2caef-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="2caef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2caef-117">-ResourceGroupName</span></span>
<span data-ttu-id="2caef-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="2caef-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2caef-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2caef-119">-Confirm</span></span>
<span data-ttu-id="2caef-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2caef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2caef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2caef-121">-WhatIf</span></span>
<span data-ttu-id="2caef-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2caef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2caef-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2caef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2caef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2caef-124">CommonParameters</span></span>
<span data-ttu-id="2caef-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2caef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2caef-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2caef-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2caef-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2caef-127">INPUTS</span></span>

### <span data-ttu-id="2caef-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2caef-128">System.String</span></span>

## <span data-ttu-id="2caef-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2caef-129">OUTPUTS</span></span>

### <span data-ttu-id="2caef-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2caef-130">System.String</span></span>

## <span data-ttu-id="2caef-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2caef-131">NOTES</span></span>

## <span data-ttu-id="2caef-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2caef-132">RELATED LINKS</span></span>
