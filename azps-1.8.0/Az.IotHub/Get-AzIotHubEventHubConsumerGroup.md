---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 065c2e185be1a9cdc0f495b61104f659076b54b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787549"
---
# <span data-ttu-id="ceb63-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ceb63-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="ceb63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ceb63-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb63-103">取得所有 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="ceb63-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="ceb63-104">句法</span><span class="sxs-lookup"><span data-stu-id="ceb63-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb63-105">說明</span><span class="sxs-lookup"><span data-stu-id="ceb63-105">DESCRIPTION</span></span>
<span data-ttu-id="ceb63-106">針對 IotHub 使用的不同 EventHubs，取得所有的 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="ceb63-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="ceb63-107">示例</span><span class="sxs-lookup"><span data-stu-id="ceb63-107">EXAMPLES</span></span>

### <span data-ttu-id="ceb63-108">範例1取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="ceb63-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="ceb63-109">針對名為 myiothub 的 iothub，取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="ceb63-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="ceb63-110">範例2取得 operationsmonitoring eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="ceb63-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="ceb63-111">針對名稱為 myiothub 的 iothub，取得 operationsMonitoringEvents eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="ceb63-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="ceb63-112">參數</span><span class="sxs-lookup"><span data-stu-id="ceb63-112">PARAMETERS</span></span>

### <span data-ttu-id="ceb63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb63-113">-DefaultProfile</span></span>
<span data-ttu-id="ceb63-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ceb63-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ceb63-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="ceb63-115">-EventHubEndpointName</span></span>
<span data-ttu-id="ceb63-116">事件中心端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ceb63-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="ceb63-117">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="ceb63-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="ceb63-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ceb63-118">-Name</span></span>
<span data-ttu-id="ceb63-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="ceb63-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="ceb63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceb63-120">-ResourceGroupName</span></span>
<span data-ttu-id="ceb63-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ceb63-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ceb63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb63-122">CommonParameters</span></span>
<span data-ttu-id="ceb63-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ceb63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb63-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ceb63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb63-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ceb63-125">INPUTS</span></span>

### <span data-ttu-id="ceb63-126">System.object</span><span class="sxs-lookup"><span data-stu-id="ceb63-126">System.String</span></span>

## <span data-ttu-id="ceb63-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ceb63-127">OUTPUTS</span></span>

### <span data-ttu-id="ceb63-128">PSEventHubConsumerGroupInfo （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="ceb63-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="ceb63-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ceb63-129">NOTES</span></span>

## <span data-ttu-id="ceb63-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ceb63-130">RELATED LINKS</span></span>
