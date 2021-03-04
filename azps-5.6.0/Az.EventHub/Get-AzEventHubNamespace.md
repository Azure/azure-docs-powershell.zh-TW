---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: e550afd0b7f580c46b15bd8b6ac68b3b0ad1bc89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903229"
---
# <span data-ttu-id="c5e08-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c5e08-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="c5e08-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c5e08-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e08-103">獲得事件中樞命名空間的詳細資訊，或獲得目前 Azure 訂閱中所有事件中樞命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="c5e08-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="c5e08-104">語法</span><span class="sxs-lookup"><span data-stu-id="c5e08-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5e08-105">描述</span><span class="sxs-lookup"><span data-stu-id="c5e08-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e08-106">此Get-AzEventHubNamespace Cmdlet 會獲得指定事件中樞命名空間的詳細資訊，或目前 Azure 訂閱中所有事件中樞命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="c5e08-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="c5e08-107">如果提供命名空間名稱，則會返回單一事件中樞命名空間的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c5e08-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="c5e08-108">如果未提供命名空間名稱，會返回命名空間清單。</span><span class="sxs-lookup"><span data-stu-id="c5e08-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="c5e08-109">例子</span><span class="sxs-lookup"><span data-stu-id="c5e08-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e08-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c5e08-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="c5e08-111">在資源群組 \` \` MyResourceGroupName 中，獲得 \` 命名空間 MyNamespaceName 的詳細資訊 \` 。</span><span class="sxs-lookup"><span data-stu-id="c5e08-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c5e08-112">參數</span><span class="sxs-lookup"><span data-stu-id="c5e08-112">PARAMETERS</span></span>

### <span data-ttu-id="c5e08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e08-113">-DefaultProfile</span></span>
<span data-ttu-id="c5e08-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5e08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5e08-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5e08-115">-Name</span></span>
<span data-ttu-id="c5e08-116">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c5e08-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e08-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5e08-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="c5e08-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e08-119">CommonParameters</span></span>
<span data-ttu-id="c5e08-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c5e08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e08-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c5e08-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e08-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c5e08-122">INPUTS</span></span>

### <span data-ttu-id="c5e08-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c5e08-123">System.String</span></span>

## <span data-ttu-id="c5e08-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c5e08-124">OUTPUTS</span></span>

### <span data-ttu-id="c5e08-125">Microsoft.Azure.Commands.EventHub.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c5e08-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c5e08-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c5e08-126">NOTES</span></span>

## <span data-ttu-id="c5e08-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5e08-127">RELATED LINKS</span></span>
