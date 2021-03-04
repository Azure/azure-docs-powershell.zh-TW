---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 1864cc9d5975c9f959edb6be470e63a10cfa63f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910846"
---
# <span data-ttu-id="66f40-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66f40-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="66f40-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66f40-102">SYNOPSIS</span></span>
<span data-ttu-id="66f40-103">從流量管理員移除端點。</span><span class="sxs-lookup"><span data-stu-id="66f40-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="66f40-104">語法</span><span class="sxs-lookup"><span data-stu-id="66f40-104">SYNTAX</span></span>

### <span data-ttu-id="66f40-105">領域</span><span class="sxs-lookup"><span data-stu-id="66f40-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66f40-106">物件</span><span class="sxs-lookup"><span data-stu-id="66f40-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66f40-107">描述</span><span class="sxs-lookup"><span data-stu-id="66f40-107">DESCRIPTION</span></span>
<span data-ttu-id="66f40-108">**Remove-AzTrafficManagerEndpoint** Cmdlet 會從 Azure 流量管理員移除端點。</span><span class="sxs-lookup"><span data-stu-id="66f40-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="66f40-109">此 Cmdlet 會提交流量管理員服務的每個變更。</span><span class="sxs-lookup"><span data-stu-id="66f40-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="66f40-110">若要從一個本地流量管理員設定檔物件移除多個端點，並承諾在單一作業中變更，請使用 Remove-AzTrafficManagerEndpointConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66f40-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="66f40-111">您可以使用管線運算子將 **TrafficManagerEndpoint** 物件傳遞到此 Cmdlet，或者您可以使用 **TrafficManagerEndpoint 參數指定 TrafficManagerEndpoint** *物件* 。</span><span class="sxs-lookup"><span data-stu-id="66f40-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="66f40-112">或者，您也可以使用名稱和類型參數，以及 *ProfileName* 和 *ResourceGroupName* 參數來指定端點名稱並輸入。 </span><span class="sxs-lookup"><span data-stu-id="66f40-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="66f40-113">例子</span><span class="sxs-lookup"><span data-stu-id="66f40-113">EXAMPLES</span></span>

### <span data-ttu-id="66f40-114">範例 1：從設定檔移除端點</span><span class="sxs-lookup"><span data-stu-id="66f40-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="66f40-115">此命令會從名為 ResourceGroup11 的資源群組中名為 ContosoProfile 的設定檔移除名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="66f40-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="66f40-116">參數</span><span class="sxs-lookup"><span data-stu-id="66f40-116">PARAMETERS</span></span>

### <span data-ttu-id="66f40-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f40-117">-DefaultProfile</span></span>
<span data-ttu-id="66f40-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66f40-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f40-119">-強制</span><span class="sxs-lookup"><span data-stu-id="66f40-119">-Force</span></span>
<span data-ttu-id="66f40-120">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="66f40-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="66f40-121">-Name</span></span>
<span data-ttu-id="66f40-122">指定此 Cmdlet 移除的流量管理員端點名稱。</span><span class="sxs-lookup"><span data-stu-id="66f40-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="66f40-123">-ProfileName</span></span>
<span data-ttu-id="66f40-124">指定流量管理員設定檔的名稱，此 Cmdlet 會從該設定檔移除端點。</span><span class="sxs-lookup"><span data-stu-id="66f40-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="66f40-125">若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66f40-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f40-126">-ResourceGroupName</span></span>
<span data-ttu-id="66f40-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66f40-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="66f40-128">此 Cmdlet 會從此參數指定的群組中，從流量管理員設定檔移除流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="66f40-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66f40-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="66f40-130">指定此 Cmdlet 移除的流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="66f40-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="66f40-131">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66f40-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-132">-類型</span><span class="sxs-lookup"><span data-stu-id="66f40-132">-Type</span></span>
<span data-ttu-id="66f40-133">指定此 Cmdlet 新增到流量管理員設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="66f40-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="66f40-134">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="66f40-134">Valid values are:</span></span> 

- <span data-ttu-id="66f40-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="66f40-135">AzureEndpoints</span></span>
- <span data-ttu-id="66f40-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="66f40-136">ExternalEndpoints</span></span>
- <span data-ttu-id="66f40-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="66f40-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-138">-確認</span><span class="sxs-lookup"><span data-stu-id="66f40-138">-Confirm</span></span>
<span data-ttu-id="66f40-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66f40-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f40-140">-WhatIf</span></span>
<span data-ttu-id="66f40-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66f40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66f40-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66f40-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f40-143">CommonParameters</span></span>
<span data-ttu-id="66f40-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66f40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f40-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="66f40-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f40-146">輸入</span><span class="sxs-lookup"><span data-stu-id="66f40-146">INPUTS</span></span>

### <span data-ttu-id="66f40-147">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66f40-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="66f40-148">輸出</span><span class="sxs-lookup"><span data-stu-id="66f40-148">OUTPUTS</span></span>

### <span data-ttu-id="66f40-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66f40-149">System.Boolean</span></span>

## <span data-ttu-id="66f40-150">筆記</span><span class="sxs-lookup"><span data-stu-id="66f40-150">NOTES</span></span>

## <span data-ttu-id="66f40-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="66f40-151">RELATED LINKS</span></span>

[<span data-ttu-id="66f40-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66f40-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="66f40-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66f40-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="66f40-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="66f40-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="66f40-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="66f40-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="66f40-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66f40-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


