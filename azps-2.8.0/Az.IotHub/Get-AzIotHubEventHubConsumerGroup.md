---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 3905111a0855eef6421a587bc7151b411106d13a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612224"
---
# <span data-ttu-id="c0bd7-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c0bd7-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="c0bd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0bd7-103">取得所有 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="c0bd7-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="c0bd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0bd7-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0bd7-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0bd7-105">DESCRIPTION</span></span>
<span data-ttu-id="c0bd7-106">針對 IotHub 使用的不同 EventHubs，取得所有的 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="c0bd7-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="c0bd7-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0bd7-107">EXAMPLES</span></span>

### <span data-ttu-id="c0bd7-108">範例1取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="c0bd7-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="c0bd7-109">針對名為 myiothub 的 iothub，取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="c0bd7-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="c0bd7-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0bd7-110">PARAMETERS</span></span>

### <span data-ttu-id="c0bd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0bd7-111">-DefaultProfile</span></span>
<span data-ttu-id="c0bd7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c0bd7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0bd7-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="c0bd7-113">-EventHubEndpointName</span></span>
<span data-ttu-id="c0bd7-114">事件中心端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0bd7-114">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="c0bd7-115">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="c0bd7-115">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0bd7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0bd7-116">-Name</span></span>
<span data-ttu-id="c0bd7-117">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c0bd7-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="c0bd7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0bd7-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0bd7-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c0bd7-119">Resource Group Name</span></span>

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

### <span data-ttu-id="c0bd7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0bd7-120">CommonParameters</span></span>
<span data-ttu-id="c0bd7-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0bd7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0bd7-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0bd7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0bd7-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c0bd7-123">INPUTS</span></span>

### <span data-ttu-id="c0bd7-124">System.object</span><span class="sxs-lookup"><span data-stu-id="c0bd7-124">System.String</span></span>

## <span data-ttu-id="c0bd7-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c0bd7-125">OUTPUTS</span></span>

### <span data-ttu-id="c0bd7-126">PSEventHubConsumerGroupInfo （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c0bd7-126">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="c0bd7-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c0bd7-127">NOTES</span></span>

## <span data-ttu-id="c0bd7-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0bd7-128">RELATED LINKS</span></span>
