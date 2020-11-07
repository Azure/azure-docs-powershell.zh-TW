---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 32af04aec91302304be3ed11c17d81d2e71cc772
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787825"
---
# <span data-ttu-id="e7a2c-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e7a2c-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="e7a2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a2c-103">建立用來建立前門的 PSBackendPool 物件</span><span class="sxs-lookup"><span data-stu-id="e7a2c-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e7a2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7a2c-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a2c-106">建立用來建立前門的 PSBackendPool 物件</span><span class="sxs-lookup"><span data-stu-id="e7a2c-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e7a2c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e7a2c-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a2c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e7a2c-108">Example 1</span></span>
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

<span data-ttu-id="e7a2c-109">建立用來建立前門的 PSBackendPool 物件</span><span class="sxs-lookup"><span data-stu-id="e7a2c-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e7a2c-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7a2c-110">PARAMETERS</span></span>

### <span data-ttu-id="e7a2c-111">-後端</span><span class="sxs-lookup"><span data-stu-id="e7a2c-111">-Backend</span></span>
<span data-ttu-id="e7a2c-112">此池子的 backends 集合。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="e7a2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a2c-113">-DefaultProfile</span></span>
<span data-ttu-id="e7a2c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a2c-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e7a2c-115">-FrontDoorName</span></span>
<span data-ttu-id="e7a2c-116">此傳送規則所屬之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="e7a2c-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="e7a2c-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="e7a2c-118">此後端池的健康情況探測設定的名稱</span><span class="sxs-lookup"><span data-stu-id="e7a2c-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="e7a2c-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="e7a2c-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="e7a2c-120">此後端池負載平衡設定的名稱</span><span class="sxs-lookup"><span data-stu-id="e7a2c-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="e7a2c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7a2c-121">-Name</span></span>
<span data-ttu-id="e7a2c-122">BackendPool [名稱]。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-122">BackendPool name.</span></span>

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

### <span data-ttu-id="e7a2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="e7a2c-124">將在其中建立 RoutingRule 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="e7a2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a2c-125">CommonParameters</span></span>
<span data-ttu-id="e7a2c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a2c-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a2c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e7a2c-128">INPUTS</span></span>

### <span data-ttu-id="e7a2c-129">所有</span><span class="sxs-lookup"><span data-stu-id="e7a2c-129">None</span></span>

## <span data-ttu-id="e7a2c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e7a2c-130">OUTPUTS</span></span>

### <span data-ttu-id="e7a2c-131">PSBackendPool 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="e7a2c-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="e7a2c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e7a2c-132">NOTES</span></span>

## <span data-ttu-id="e7a2c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7a2c-133">RELATED LINKS</span></span>

<span data-ttu-id="e7a2c-134">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md) 
[新-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="e7a2c-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
