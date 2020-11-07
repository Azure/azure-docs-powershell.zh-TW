---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 507787df7215efcd1b275f481b638aa80f979498
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625844"
---
# <span data-ttu-id="eb8de-101">Get-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="eb8de-101">Get-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="eb8de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb8de-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8de-103">取得所有 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="eb8de-103">Gets all the eventhub consumergroups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb8de-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb8de-104">SYNTAX</span></span>

```
Get-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb8de-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb8de-105">DESCRIPTION</span></span>
<span data-ttu-id="eb8de-106">針對 IotHub 使用的不同 EventHubs，取得所有的 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="eb8de-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="eb8de-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb8de-107">EXAMPLES</span></span>

### <span data-ttu-id="eb8de-108">範例1取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="eb8de-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "events"
```

<span data-ttu-id="eb8de-109">針對名為 myiothub 的 iothub，取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="eb8de-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

### <span data-ttu-id="eb8de-110">範例2取得 operationsmonitoring eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="eb8de-110">Example 2 Gets all the eventhub consumergroups for the operationsmonitoring eventhub</span></span>
```
PS C:\> Get-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "operationsMonitoringEvents"
```

<span data-ttu-id="eb8de-111">針對名稱為 myiothub 的 iothub，取得 operationsMonitoringEvents eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="eb8de-111">Gets all the eventhub consumergroups for the operationsMonitoringEvents eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="eb8de-112">參數</span><span class="sxs-lookup"><span data-stu-id="eb8de-112">PARAMETERS</span></span>

### <span data-ttu-id="eb8de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8de-113">-DefaultProfile</span></span>
<span data-ttu-id="eb8de-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eb8de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb8de-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="eb8de-115">-EventHubEndpointName</span></span>
<span data-ttu-id="eb8de-116">事件中心端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb8de-116">Name of the Event Hub endpoint.</span></span>
<span data-ttu-id="eb8de-117">可能的值事件、operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="eb8de-117">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="eb8de-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb8de-118">-Name</span></span>
<span data-ttu-id="eb8de-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="eb8de-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="eb8de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8de-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb8de-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="eb8de-121">Resource Group Name</span></span>

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

### <span data-ttu-id="eb8de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8de-122">CommonParameters</span></span>
<span data-ttu-id="eb8de-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb8de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8de-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb8de-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8de-125">輸入</span><span class="sxs-lookup"><span data-stu-id="eb8de-125">INPUTS</span></span>

### <span data-ttu-id="eb8de-126">System.object</span><span class="sxs-lookup"><span data-stu-id="eb8de-126">System.String</span></span>

## <span data-ttu-id="eb8de-127">輸出</span><span class="sxs-lookup"><span data-stu-id="eb8de-127">OUTPUTS</span></span>

### <span data-ttu-id="eb8de-128">PSEventHubConsumerGroupInfo （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="eb8de-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="eb8de-129">筆記</span><span class="sxs-lookup"><span data-stu-id="eb8de-129">NOTES</span></span>

## <span data-ttu-id="eb8de-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb8de-130">RELATED LINKS</span></span>
