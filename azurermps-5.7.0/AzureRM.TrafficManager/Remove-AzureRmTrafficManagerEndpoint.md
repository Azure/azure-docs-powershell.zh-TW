---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 3b3eb2fb0539be4750f4cce7dedb7cd2f26931a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448522"
---
# <span data-ttu-id="2247a-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2247a-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2247a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2247a-102">SYNOPSIS</span></span>
<span data-ttu-id="2247a-103">從流量管理器移除端點。</span><span class="sxs-lookup"><span data-stu-id="2247a-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2247a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2247a-104">SYNTAX</span></span>

### <span data-ttu-id="2247a-105">區域</span><span class="sxs-lookup"><span data-stu-id="2247a-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2247a-106">面向</span><span class="sxs-lookup"><span data-stu-id="2247a-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2247a-107">說明</span><span class="sxs-lookup"><span data-stu-id="2247a-107">DESCRIPTION</span></span>
<span data-ttu-id="2247a-108">**AzureRmTrafficManagerEndpoint** Cmdlet 會從 Azure 流量管理器中移除端點。</span><span class="sxs-lookup"><span data-stu-id="2247a-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="2247a-109">這個 Cmdlet 會將每個變更提交到流量管理器服務。</span><span class="sxs-lookup"><span data-stu-id="2247a-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="2247a-110">若要從本機流量管理器設定檔物件移除多個端點，並在單一作業中提交變更，請使用 Remove-AzureRmTrafficManagerEndpointConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2247a-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="2247a-111">您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數來指定 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="2247a-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="2247a-112">或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="2247a-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="2247a-113">示例</span><span class="sxs-lookup"><span data-stu-id="2247a-113">EXAMPLES</span></span>

### <span data-ttu-id="2247a-114">範例1：從設定檔移除端點</span><span class="sxs-lookup"><span data-stu-id="2247a-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="2247a-115">這個命令會從名為 ResourceGroup11 的資源群組中，從名為 ContosoProfile 的設定檔中移除名為 contoso 的 Azure 端點。</span><span class="sxs-lookup"><span data-stu-id="2247a-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2247a-116">參數</span><span class="sxs-lookup"><span data-stu-id="2247a-116">PARAMETERS</span></span>

### <span data-ttu-id="2247a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2247a-117">-DefaultProfile</span></span>
<span data-ttu-id="2247a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2247a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2247a-119">-Force</span></span>
<span data-ttu-id="2247a-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2247a-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2247a-121">-Name</span></span>
<span data-ttu-id="2247a-122">指定此 Cmdlet 移除之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="2247a-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2247a-123">-ProfileName</span></span>
<span data-ttu-id="2247a-124">指定此 Cmdlet 從中移除端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="2247a-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="2247a-125">若要取得設定檔，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2247a-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2247a-126">-ResourceGroupName</span></span>
<span data-ttu-id="2247a-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2247a-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2247a-128">這個 Cmdlet 會從此參數指定之群組中的流量管理器設定檔，移除流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="2247a-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2247a-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2247a-130">指定此 Cmdlet 移除的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="2247a-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="2247a-131">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2247a-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-132">-類型</span><span class="sxs-lookup"><span data-stu-id="2247a-132">-Type</span></span>
<span data-ttu-id="2247a-133">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="2247a-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="2247a-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2247a-134">Valid values are:</span></span> 

- <span data-ttu-id="2247a-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2247a-135">AzureEndpoints</span></span>
- <span data-ttu-id="2247a-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2247a-136">ExternalEndpoints</span></span>
- <span data-ttu-id="2247a-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2247a-137">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="2247a-138">-Confirm</span></span>
<span data-ttu-id="2247a-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2247a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2247a-140">-WhatIf</span></span>
<span data-ttu-id="2247a-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2247a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2247a-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2247a-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2247a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2247a-143">CommonParameters</span></span>
<span data-ttu-id="2247a-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2247a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2247a-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2247a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2247a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="2247a-146">INPUTS</span></span>

### <span data-ttu-id="2247a-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2247a-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="2247a-148">形參 "TrafficManagerEndpoint" 接受管線中 "TrafficManagerEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2247a-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="2247a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="2247a-149">OUTPUTS</span></span>

### <span data-ttu-id="2247a-150">System.object</span><span class="sxs-lookup"><span data-stu-id="2247a-150">System.Boolean</span></span>

## <span data-ttu-id="2247a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="2247a-151">NOTES</span></span>

## <span data-ttu-id="2247a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="2247a-152">RELATED LINKS</span></span>

[<span data-ttu-id="2247a-153">AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2247a-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2247a-154">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2247a-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="2247a-155">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2247a-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="2247a-156">移除-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2247a-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2247a-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2247a-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


