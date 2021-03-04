---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905398"
---
# <span data-ttu-id="e648b-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e648b-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="e648b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e648b-102">SYNOPSIS</span></span>
<span data-ttu-id="e648b-103">建立 PSBackendPool 物件以建立前端門</span><span class="sxs-lookup"><span data-stu-id="e648b-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e648b-104">語法</span><span class="sxs-lookup"><span data-stu-id="e648b-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e648b-105">描述</span><span class="sxs-lookup"><span data-stu-id="e648b-105">DESCRIPTION</span></span>
<span data-ttu-id="e648b-106">建立 PSBackendPool 物件以建立前端門</span><span class="sxs-lookup"><span data-stu-id="e648b-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e648b-107">例子</span><span class="sxs-lookup"><span data-stu-id="e648b-107">EXAMPLES</span></span>

### <span data-ttu-id="e648b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e648b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="e648b-109">建立 PSBackendPool 物件以建立前端門</span><span class="sxs-lookup"><span data-stu-id="e648b-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e648b-110">參數</span><span class="sxs-lookup"><span data-stu-id="e648b-110">PARAMETERS</span></span>

### <span data-ttu-id="e648b-111">-後端</span><span class="sxs-lookup"><span data-stu-id="e648b-111">-Backend</span></span>
<span data-ttu-id="e648b-112">此集區後端集。</span><span class="sxs-lookup"><span data-stu-id="e648b-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e648b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e648b-113">-DefaultProfile</span></span>
<span data-ttu-id="e648b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e648b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e648b-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e648b-115">-FrontDoorName</span></span>
<span data-ttu-id="e648b-116">此路由規則所屬的前門名稱。</span><span class="sxs-lookup"><span data-stu-id="e648b-116">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e648b-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="e648b-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="e648b-118">此後端資料庫的健康狀態查詢設定名稱</span><span class="sxs-lookup"><span data-stu-id="e648b-118">The name of the health probe settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e648b-119">-LoadBalsettingSettingsName</span><span class="sxs-lookup"><span data-stu-id="e648b-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="e648b-120">此後端資料庫的負載平衡設定名稱</span><span class="sxs-lookup"><span data-stu-id="e648b-120">The name of the load balancing settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e648b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e648b-121">-Name</span></span>
<span data-ttu-id="e648b-122">後端多工緩衝處理程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e648b-122">BackendPool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e648b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e648b-123">-ResourceGroupName</span></span>
<span data-ttu-id="e648b-124">要建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e648b-124">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e648b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e648b-125">CommonParameters</span></span>
<span data-ttu-id="e648b-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e648b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e648b-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e648b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e648b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e648b-128">INPUTS</span></span>

### <span data-ttu-id="e648b-129">沒有</span><span class="sxs-lookup"><span data-stu-id="e648b-129">None</span></span>

## <span data-ttu-id="e648b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e648b-130">OUTPUTS</span></span>

### <span data-ttu-id="e648b-131">Microsoft.Azure.Commands.FrontDoor.models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="e648b-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="e648b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e648b-132">NOTES</span></span>

## <span data-ttu-id="e648b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e648b-133">RELATED LINKS</span></span>

<span data-ttu-id="e648b-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md) 
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="e648b-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
