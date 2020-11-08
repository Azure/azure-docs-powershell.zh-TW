---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140130"
---
# <span data-ttu-id="9e373-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9e373-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="9e373-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e373-102">SYNOPSIS</span></span>
<span data-ttu-id="9e373-103">取得事件中心命名空間的詳細資料，或取得目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="9e373-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="9e373-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e373-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e373-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e373-105">DESCRIPTION</span></span>
<span data-ttu-id="9e373-106">Get-AzEventHubNamespace Cmdlet 會取得指定事件中樞命名空間的詳細資料，或目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="9e373-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="9e373-107">如果提供命名空間名稱，則會傳回單一事件中樞命名空間的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9e373-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="9e373-108">如果未提供命名空間名稱，則會傳回命名空間清單。</span><span class="sxs-lookup"><span data-stu-id="9e373-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="9e373-109">示例</span><span class="sxs-lookup"><span data-stu-id="9e373-109">EXAMPLES</span></span>

### <span data-ttu-id="9e373-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9e373-110">Example 1</span></span>
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

<span data-ttu-id="9e373-111">取得 \` \` 資源群組 MyResourceGroupName 中命名空間 MyNamespaceName 的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="9e373-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9e373-112">參數</span><span class="sxs-lookup"><span data-stu-id="9e373-112">PARAMETERS</span></span>

### <span data-ttu-id="9e373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e373-113">-DefaultProfile</span></span>
<span data-ttu-id="9e373-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e373-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e373-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e373-115">-Name</span></span>
<span data-ttu-id="9e373-116">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="9e373-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="9e373-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e373-117">-ResourceGroupName</span></span>
<span data-ttu-id="9e373-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9e373-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9e373-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e373-119">CommonParameters</span></span>
<span data-ttu-id="9e373-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e373-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e373-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e373-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e373-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9e373-122">INPUTS</span></span>

### <span data-ttu-id="9e373-123">System.object</span><span class="sxs-lookup"><span data-stu-id="9e373-123">System.String</span></span>

## <span data-ttu-id="9e373-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9e373-124">OUTPUTS</span></span>

### <span data-ttu-id="9e373-125">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="9e373-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9e373-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9e373-126">NOTES</span></span>

## <span data-ttu-id="9e373-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e373-127">RELATED LINKS</span></span>
