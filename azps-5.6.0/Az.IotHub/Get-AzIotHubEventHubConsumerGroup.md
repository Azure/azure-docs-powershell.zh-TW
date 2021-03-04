---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911053"
---
# <span data-ttu-id="b39ad-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b39ad-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b39ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b39ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b39ad-103">獲得所有 eventhub 消費者群。</span><span class="sxs-lookup"><span data-stu-id="b39ad-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="b39ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="b39ad-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b39ad-105">描述</span><span class="sxs-lookup"><span data-stu-id="b39ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b39ad-106">針對 IotHub 使用的不同 EventHub，獲得所有 eventhub 消費者組。</span><span class="sxs-lookup"><span data-stu-id="b39ad-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="b39ad-107">例子</span><span class="sxs-lookup"><span data-stu-id="b39ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b39ad-108">範例 1 為遙測事件hub 獲取所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="b39ad-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b39ad-109">為名為 myiothub 的 iothub 遙測事件hub，獲得所有 eventhub 消費者組</span><span class="sxs-lookup"><span data-stu-id="b39ad-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="b39ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="b39ad-110">PARAMETERS</span></span>

### <span data-ttu-id="b39ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39ad-111">-DefaultProfile</span></span>
<span data-ttu-id="b39ad-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b39ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b39ad-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b39ad-113">-Name</span></span>
<span data-ttu-id="b39ad-114">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b39ad-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="b39ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b39ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="b39ad-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="b39ad-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b39ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39ad-117">CommonParameters</span></span>
<span data-ttu-id="b39ad-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b39ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39ad-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b39ad-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39ad-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b39ad-120">INPUTS</span></span>

### <span data-ttu-id="b39ad-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b39ad-121">System.String</span></span>

## <span data-ttu-id="b39ad-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b39ad-122">OUTPUTS</span></span>

### <span data-ttu-id="b39ad-123">Microsoft.Azure.Commands.management.IotHub.models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="b39ad-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="b39ad-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b39ad-124">NOTES</span></span>

## <span data-ttu-id="b39ad-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b39ad-125">RELATED LINKS</span></span>
