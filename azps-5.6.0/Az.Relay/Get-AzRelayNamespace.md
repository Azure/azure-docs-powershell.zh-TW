---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: 153d6622b00df1e45ab674b7d4832f0eb2d609f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914609"
---
# <span data-ttu-id="6212d-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="6212d-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="6212d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6212d-102">SYNOPSIS</span></span>
<span data-ttu-id="6212d-103">在資源群組中，獲得指定之 Relay 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="6212d-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="6212d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6212d-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6212d-105">描述</span><span class="sxs-lookup"><span data-stu-id="6212d-105">DESCRIPTION</span></span>
<span data-ttu-id="6212d-106">**Get-AzRelayNamespace** Cmdlet 會取得資源群組中指定之 Relay 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="6212d-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="6212d-107">例子</span><span class="sxs-lookup"><span data-stu-id="6212d-107">EXAMPLES</span></span>

### <span data-ttu-id="6212d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6212d-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="6212d-109">傳回指定 Relay 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="6212d-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="6212d-110">參數</span><span class="sxs-lookup"><span data-stu-id="6212d-110">PARAMETERS</span></span>

### <span data-ttu-id="6212d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6212d-111">-DefaultProfile</span></span>
<span data-ttu-id="6212d-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6212d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6212d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6212d-113">-Name</span></span>
<span data-ttu-id="6212d-114">轉場命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="6212d-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6212d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6212d-115">-ResourceGroupName</span></span>
<span data-ttu-id="6212d-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6212d-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="6212d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6212d-117">CommonParameters</span></span>
<span data-ttu-id="6212d-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6212d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6212d-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6212d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6212d-120">輸入</span><span class="sxs-lookup"><span data-stu-id="6212d-120">INPUTS</span></span>

### <span data-ttu-id="6212d-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6212d-121">System.String</span></span>

## <span data-ttu-id="6212d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="6212d-122">OUTPUTS</span></span>

### <span data-ttu-id="6212d-123">Microsoft.Azure.Commands.Relay.models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="6212d-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="6212d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="6212d-124">NOTES</span></span>

## <span data-ttu-id="6212d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="6212d-125">RELATED LINKS</span></span>
