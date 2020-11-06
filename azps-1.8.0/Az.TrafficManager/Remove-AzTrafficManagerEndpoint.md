---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 60ce16c9c9933d326013ce03b74637b0fce4a3b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614331"
---
# <span data-ttu-id="d2feb-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2feb-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d2feb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2feb-102">SYNOPSIS</span></span>
<span data-ttu-id="d2feb-103">從流量管理器移除端點。</span><span class="sxs-lookup"><span data-stu-id="d2feb-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="d2feb-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2feb-104">SYNTAX</span></span>

### <span data-ttu-id="d2feb-105">區域</span><span class="sxs-lookup"><span data-stu-id="d2feb-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2feb-106">面向</span><span class="sxs-lookup"><span data-stu-id="d2feb-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2feb-107">說明</span><span class="sxs-lookup"><span data-stu-id="d2feb-107">DESCRIPTION</span></span>
<span data-ttu-id="d2feb-108">**AzTrafficManagerEndpoint** Cmdlet 會從 Azure 流量管理器中移除端點。</span><span class="sxs-lookup"><span data-stu-id="d2feb-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="d2feb-109">這個 Cmdlet 會將每個變更提交到流量管理器服務。</span><span class="sxs-lookup"><span data-stu-id="d2feb-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="d2feb-110">若要從本機流量管理器設定檔物件移除多個端點，並在單一作業中提交變更，請使用 Remove-AzTrafficManagerEndpointConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2feb-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="d2feb-111">您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數來指定 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="d2feb-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="d2feb-112">或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="d2feb-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d2feb-113">示例</span><span class="sxs-lookup"><span data-stu-id="d2feb-113">EXAMPLES</span></span>

### <span data-ttu-id="d2feb-114">範例1：從設定檔移除端點</span><span class="sxs-lookup"><span data-stu-id="d2feb-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="d2feb-115">這個命令會從名為 ResourceGroup11 的資源群組中，從名為 ContosoProfile 的設定檔中移除名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="d2feb-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d2feb-116">參數</span><span class="sxs-lookup"><span data-stu-id="d2feb-116">PARAMETERS</span></span>

### <span data-ttu-id="d2feb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2feb-117">-DefaultProfile</span></span>
<span data-ttu-id="d2feb-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2feb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2feb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d2feb-119">-Force</span></span>
<span data-ttu-id="d2feb-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d2feb-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2feb-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2feb-121">-Name</span></span>
<span data-ttu-id="d2feb-122">指定此 Cmdlet 移除之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2feb-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d2feb-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d2feb-123">-ProfileName</span></span>
<span data-ttu-id="d2feb-124">指定此 Cmdlet 從中移除端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d2feb-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="d2feb-125">若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2feb-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d2feb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2feb-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2feb-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2feb-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d2feb-128">這個 Cmdlet 會從此參數指定之群組中的流量管理器設定檔，移除流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="d2feb-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d2feb-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2feb-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d2feb-130">指定此 Cmdlet 移除的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="d2feb-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="d2feb-131">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2feb-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d2feb-132">-類型</span><span class="sxs-lookup"><span data-stu-id="d2feb-132">-Type</span></span>
<span data-ttu-id="d2feb-133">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="d2feb-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d2feb-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d2feb-134">Valid values are:</span></span> 

- <span data-ttu-id="d2feb-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d2feb-135">AzureEndpoints</span></span>
- <span data-ttu-id="d2feb-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d2feb-136">ExternalEndpoints</span></span>
- <span data-ttu-id="d2feb-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d2feb-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="d2feb-138">-確認</span><span class="sxs-lookup"><span data-stu-id="d2feb-138">-Confirm</span></span>
<span data-ttu-id="d2feb-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2feb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2feb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2feb-140">-WhatIf</span></span>
<span data-ttu-id="d2feb-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2feb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2feb-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2feb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2feb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2feb-143">CommonParameters</span></span>
<span data-ttu-id="d2feb-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2feb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2feb-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2feb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2feb-146">輸入</span><span class="sxs-lookup"><span data-stu-id="d2feb-146">INPUTS</span></span>

### <span data-ttu-id="d2feb-147">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="d2feb-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d2feb-148">輸出</span><span class="sxs-lookup"><span data-stu-id="d2feb-148">OUTPUTS</span></span>

### <span data-ttu-id="d2feb-149">System.object</span><span class="sxs-lookup"><span data-stu-id="d2feb-149">System.Boolean</span></span>

## <span data-ttu-id="d2feb-150">筆記</span><span class="sxs-lookup"><span data-stu-id="d2feb-150">NOTES</span></span>

## <span data-ttu-id="d2feb-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2feb-151">RELATED LINKS</span></span>

[<span data-ttu-id="d2feb-152">AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2feb-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d2feb-153">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2feb-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d2feb-154">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2feb-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d2feb-155">移除-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d2feb-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="d2feb-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d2feb-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

