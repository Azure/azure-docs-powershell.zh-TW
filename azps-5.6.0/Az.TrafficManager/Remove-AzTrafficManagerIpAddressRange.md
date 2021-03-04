---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: f427407ad966fd9680646e1d8b7551624231229d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910837"
---
# <span data-ttu-id="3f178-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3f178-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="3f178-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f178-102">SYNOPSIS</span></span>
<span data-ttu-id="3f178-103">從本地流量管理員端點物件移除位址範圍或子網。</span><span class="sxs-lookup"><span data-stu-id="3f178-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="3f178-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f178-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f178-105">描述</span><span class="sxs-lookup"><span data-stu-id="3f178-105">DESCRIPTION</span></span>
<span data-ttu-id="3f178-106">**Remove-AzTrafficManagerIpAddressRange** Cmdlet 會從本地 Azure Traffic Manager 端點物件移除 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="3f178-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="3f178-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerEndpoint端點Get-AzTrafficManagerEndpoint端點。</span><span class="sxs-lookup"><span data-stu-id="3f178-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="3f178-108">此 Cmdlet 在本地端點物件上操作。</span><span class="sxs-lookup"><span data-stu-id="3f178-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="3f178-109">使用 Cmdlet 來為流量管理員的端點Set-AzTrafficManagerEndpoint變更。</span><span class="sxs-lookup"><span data-stu-id="3f178-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3f178-110">例子</span><span class="sxs-lookup"><span data-stu-id="3f178-110">EXAMPLES</span></span>

### <span data-ttu-id="3f178-111">範例 1：移除端點的 IP 位址範圍</span><span class="sxs-lookup"><span data-stu-id="3f178-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="3f178-112">第一個命令會從名為 ResourceGroup11 的資源群組中名為 ContosoProfile 的設定檔中，獲得名為 contosoProfile 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="3f178-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="3f178-113">第二個命令會從儲存在 $TrafficManagerEndpoint 的端點移除 IP 位址$TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="3f178-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="3f178-114">最後一個命令會更新 Traffic Manager 中的端點，以符合 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="3f178-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="3f178-115">參數</span><span class="sxs-lookup"><span data-stu-id="3f178-115">PARAMETERS</span></span>

### <span data-ttu-id="3f178-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f178-116">-DefaultProfile</span></span>
<span data-ttu-id="3f178-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f178-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f178-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f178-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3f178-119">指定一個本地 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="3f178-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="3f178-120">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="3f178-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3f178-121">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f178-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f178-122">-確認</span><span class="sxs-lookup"><span data-stu-id="3f178-122">-Confirm</span></span>
<span data-ttu-id="3f178-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3f178-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f178-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f178-124">-WhatIf</span></span>
<span data-ttu-id="3f178-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f178-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f178-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f178-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f178-127">-第一個</span><span class="sxs-lookup"><span data-stu-id="3f178-127">-First</span></span>
<span data-ttu-id="3f178-128">指定要移除範圍中的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3f178-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="3f178-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f178-129">CommonParameters</span></span>
<span data-ttu-id="3f178-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f178-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f178-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3f178-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f178-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3f178-132">INPUTS</span></span>

### <span data-ttu-id="3f178-133">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f178-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="3f178-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3f178-134">OUTPUTS</span></span>

### <span data-ttu-id="3f178-135">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f178-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="3f178-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3f178-136">NOTES</span></span>

## <span data-ttu-id="3f178-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f178-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f178-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3f178-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="3f178-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f178-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3f178-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f178-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3f178-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f178-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
