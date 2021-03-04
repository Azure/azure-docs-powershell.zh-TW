---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 84d994366c81b7adfc5fa0f7fdb34267ae8b6370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901633"
---
# <span data-ttu-id="3a3d7-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3a3d7-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="3a3d7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3d7-103">將位址範圍或子網新增到本地流量管理員端點物件。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="3a3d7-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a3d7-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a3d7-105">描述</span><span class="sxs-lookup"><span data-stu-id="3a3d7-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3d7-106">**Add-AzTrafficManagerIpAddressRange** Cmdlet 會將 IP 位址範圍新增到本地 Azure 流量管理員端點物件。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="3a3d7-107">您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerEndpoint端點Get-AzTrafficManagerEndpoint端點。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="3a3d7-108">此 Cmdlet 在本地端點物件上操作。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="3a3d7-109">使用 Cmdlet 來為流量管理員的端點Set-AzTrafficManagerEndpoint變更。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3a3d7-110">例子</span><span class="sxs-lookup"><span data-stu-id="3a3d7-110">EXAMPLES</span></span>

### <span data-ttu-id="3a3d7-111">範例 1：新增 IP 位址範圍至端點</span><span class="sxs-lookup"><span data-stu-id="3a3d7-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="3a3d7-112">第一個命令會使用 **New-AzTrafficManagerEndpoint** Cmdlet 建立 Azure 流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="3a3d7-113">該命令將本地端點儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="3a3d7-114">第二個命令會將 IP 位址範圍 1.2.3.4 加到 5.6.7.8 到儲存在 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="3a3d7-115">第三個命令會將 IP 位址範圍 9.10.11.0 新增到 9.10.11.255 到儲存在 $TrafficManagerEndpoint 中的端點。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="3a3d7-116">第四個命令會確認範圍符合範圍的大小，然後將 IP 位址範圍 12.13.14.0 新增到 12.13.14.31 到 $TrafficManagerEndpoint 中儲存的端點。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="3a3d7-117">第五個命令會將 IP 位址範圍 15.16.17.18 新增到 15.16.17.18 到 $TrafficManagerEndpoint 中儲存的端點。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="3a3d7-118">最後一個命令會更新 Traffic Manager 中的端點，以符合 $TrafficManagerEndpoint。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="3a3d7-119">參數</span><span class="sxs-lookup"><span data-stu-id="3a3d7-119">PARAMETERS</span></span>

### <span data-ttu-id="3a3d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3d7-120">-DefaultProfile</span></span>
<span data-ttu-id="3a3d7-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a3d7-122">-上次</span><span class="sxs-lookup"><span data-stu-id="3a3d7-122">-Last</span></span>
<span data-ttu-id="3a3d7-123">指定要新增範圍中的最後一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="3a3d7-124">-範圍</span><span class="sxs-lookup"><span data-stu-id="3a3d7-124">-Scope</span></span>
<span data-ttu-id="3a3d7-125">指定要新增的 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3d7-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a3d7-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3a3d7-127">指定一個本地 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="3a3d7-128">此 Cmdlet 會修改此本機物件。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="3a3d7-129">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="3a3d7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3a3d7-130">-Confirm</span></span>
<span data-ttu-id="3a3d7-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3d7-132">-WhatIf</span></span>
<span data-ttu-id="3a3d7-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a3d7-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3d7-135">-第一個</span><span class="sxs-lookup"><span data-stu-id="3a3d7-135">-First</span></span>
<span data-ttu-id="3a3d7-136">指定要新增範圍的第一個 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="3a3d7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3d7-137">CommonParameters</span></span>
<span data-ttu-id="3a3d7-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3d7-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3a3d7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3d7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3a3d7-140">INPUTS</span></span>

### <span data-ttu-id="3a3d7-141">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a3d7-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="3a3d7-142">輸出</span><span class="sxs-lookup"><span data-stu-id="3a3d7-142">OUTPUTS</span></span>

### <span data-ttu-id="3a3d7-143">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a3d7-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="3a3d7-144">筆記</span><span class="sxs-lookup"><span data-stu-id="3a3d7-144">NOTES</span></span>

## <span data-ttu-id="3a3d7-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a3d7-145">RELATED LINKS</span></span>

[<span data-ttu-id="3a3d7-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3a3d7-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="3a3d7-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a3d7-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3a3d7-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3a3d7-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="3a3d7-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a3d7-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
