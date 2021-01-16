---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283751"
---
# <span data-ttu-id="c7ad9-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="c7ad9-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="c7ad9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ad9-103">取得資源群組中指定的中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="c7ad9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7ad9-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7ad9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ad9-106">**AzRelayNamespace** Cmdlet 會取得資源群組中指定的中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="c7ad9-107">示例</span><span class="sxs-lookup"><span data-stu-id="c7ad9-107">EXAMPLES</span></span>

### <span data-ttu-id="c7ad9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c7ad9-108">Example 1</span></span>
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

<span data-ttu-id="c7ad9-109">傳回指定的中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="c7ad9-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7ad9-110">PARAMETERS</span></span>

### <span data-ttu-id="c7ad9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ad9-111">-DefaultProfile</span></span>
<span data-ttu-id="c7ad9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7ad9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7ad9-113">-Name</span></span>
<span data-ttu-id="c7ad9-114">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c7ad9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ad9-115">-ResourceGroupName</span></span>
<span data-ttu-id="c7ad9-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7ad9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ad9-117">CommonParameters</span></span>
<span data-ttu-id="c7ad9-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ad9-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7ad9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ad9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c7ad9-120">INPUTS</span></span>

### <span data-ttu-id="c7ad9-121">System.object</span><span class="sxs-lookup"><span data-stu-id="c7ad9-121">System.String</span></span>

## <span data-ttu-id="c7ad9-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c7ad9-122">OUTPUTS</span></span>

### <span data-ttu-id="c7ad9-123">PSRelayNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c7ad9-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="c7ad9-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c7ad9-124">NOTES</span></span>

## <span data-ttu-id="c7ad9-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7ad9-125">RELATED LINKS</span></span>
