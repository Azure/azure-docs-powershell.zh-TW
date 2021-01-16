---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281932"
---
# <span data-ttu-id="33785-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="33785-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="33785-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33785-102">SYNOPSIS</span></span>
<span data-ttu-id="33785-103">取得所有 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="33785-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="33785-104">句法</span><span class="sxs-lookup"><span data-stu-id="33785-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33785-105">說明</span><span class="sxs-lookup"><span data-stu-id="33785-105">DESCRIPTION</span></span>
<span data-ttu-id="33785-106">針對 IotHub 使用的不同 EventHubs，取得所有的 eventhub consumergroups。</span><span class="sxs-lookup"><span data-stu-id="33785-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="33785-107">示例</span><span class="sxs-lookup"><span data-stu-id="33785-107">EXAMPLES</span></span>

### <span data-ttu-id="33785-108">範例1取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="33785-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="33785-109">針對名為 myiothub 的 iothub，取得遙測 eventhub 的所有 eventhub consumergroups</span><span class="sxs-lookup"><span data-stu-id="33785-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="33785-110">參數</span><span class="sxs-lookup"><span data-stu-id="33785-110">PARAMETERS</span></span>

### <span data-ttu-id="33785-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33785-111">-DefaultProfile</span></span>
<span data-ttu-id="33785-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="33785-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33785-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="33785-113">-Name</span></span>
<span data-ttu-id="33785-114">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="33785-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="33785-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33785-115">-ResourceGroupName</span></span>
<span data-ttu-id="33785-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="33785-116">Resource Group Name</span></span>

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

### <span data-ttu-id="33785-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33785-117">CommonParameters</span></span>
<span data-ttu-id="33785-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33785-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33785-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33785-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33785-120">輸入</span><span class="sxs-lookup"><span data-stu-id="33785-120">INPUTS</span></span>

### <span data-ttu-id="33785-121">System.object</span><span class="sxs-lookup"><span data-stu-id="33785-121">System.String</span></span>

## <span data-ttu-id="33785-122">輸出</span><span class="sxs-lookup"><span data-stu-id="33785-122">OUTPUTS</span></span>

### <span data-ttu-id="33785-123">PSEventHubConsumerGroupInfo （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="33785-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="33785-124">筆記</span><span class="sxs-lookup"><span data-stu-id="33785-124">NOTES</span></span>

## <span data-ttu-id="33785-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="33785-125">RELATED LINKS</span></span>
