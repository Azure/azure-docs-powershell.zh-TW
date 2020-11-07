---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 6dd40ff6bdf94d95b9fe31ead7ce6bde53c7042b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787837"
---
# <span data-ttu-id="af406-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="af406-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="af406-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af406-102">SYNOPSIS</span></span>
<span data-ttu-id="af406-103">取得前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="af406-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="af406-104">句法</span><span class="sxs-lookup"><span data-stu-id="af406-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af406-105">說明</span><span class="sxs-lookup"><span data-stu-id="af406-105">DESCRIPTION</span></span>
<span data-ttu-id="af406-106">**AzFrontDoor** CmdletGet 會取得目前訂閱中符合所提供資訊的所有現有前門。</span><span class="sxs-lookup"><span data-stu-id="af406-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="af406-107">示例</span><span class="sxs-lookup"><span data-stu-id="af406-107">EXAMPLES</span></span>

### <span data-ttu-id="af406-108">範例1：取得目前訂閱中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="af406-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="af406-109">取得目前訂閱中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="af406-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="af406-110">範例2：在目前的訂閱中取得資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="af406-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="af406-111">取得目前訂閱中資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="af406-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="af406-112">範例3：在目前訂閱中取得名為 "frontDoor1" 的資源群組 "rg1" 中的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="af406-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="af406-113">在目前訂閱中取得名為 "frontDoor1" 的資源群組 "rg1" 中的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="af406-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="af406-114">參數</span><span class="sxs-lookup"><span data-stu-id="af406-114">PARAMETERS</span></span>

### <span data-ttu-id="af406-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af406-115">-DefaultProfile</span></span>
<span data-ttu-id="af406-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af406-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af406-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="af406-117">-Name</span></span>
<span data-ttu-id="af406-118">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="af406-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af406-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af406-119">-ResourceGroupName</span></span>
<span data-ttu-id="af406-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af406-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af406-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af406-121">CommonParameters</span></span>
<span data-ttu-id="af406-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af406-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af406-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af406-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af406-124">輸入</span><span class="sxs-lookup"><span data-stu-id="af406-124">INPUTS</span></span>

### <span data-ttu-id="af406-125">所有</span><span class="sxs-lookup"><span data-stu-id="af406-125">None</span></span>

## <span data-ttu-id="af406-126">輸出</span><span class="sxs-lookup"><span data-stu-id="af406-126">OUTPUTS</span></span>

### <span data-ttu-id="af406-127">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="af406-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="af406-128">筆記</span><span class="sxs-lookup"><span data-stu-id="af406-128">NOTES</span></span>

## <span data-ttu-id="af406-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="af406-129">RELATED LINKS</span></span>

<span data-ttu-id="af406-130">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md) 
[移除-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="af406-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
