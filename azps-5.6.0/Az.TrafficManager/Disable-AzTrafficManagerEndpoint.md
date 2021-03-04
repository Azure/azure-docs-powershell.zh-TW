---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: e14f74af1c8e50ddc5bc3281fca71b1e2d740e3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901622"
---
# <span data-ttu-id="c0046-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c0046-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0046-102">SYNOPSIS</span></span>
<span data-ttu-id="c0046-103">停用流量管理員設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="c0046-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0046-104">SYNTAX</span></span>

### <span data-ttu-id="c0046-105">領域</span><span class="sxs-lookup"><span data-stu-id="c0046-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0046-106">物件</span><span class="sxs-lookup"><span data-stu-id="c0046-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0046-107">描述</span><span class="sxs-lookup"><span data-stu-id="c0046-107">DESCRIPTION</span></span>
<span data-ttu-id="c0046-108">**Disable-AzTrafficManagerEndpoint** Cmdlet 會停用 Azure 流量管理員設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c0046-109">您可以使用管線運算子將 **TrafficManagerEndpoint** 物件傳遞到此 Cmdlet，或者您可以使用 **TrafficManagerEndpoint 參數傳遞 TrafficManagerEndpoint** *物件* 。</span><span class="sxs-lookup"><span data-stu-id="c0046-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="c0046-110">或者，您也可以使用名稱和類型參數，以及 *ProfileName* 和 *ResourceGroupName* 參數來指定端點名稱並輸入。 </span><span class="sxs-lookup"><span data-stu-id="c0046-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="c0046-111">例子</span><span class="sxs-lookup"><span data-stu-id="c0046-111">EXAMPLES</span></span>

### <span data-ttu-id="c0046-112">範例 1：停用端點名稱</span><span class="sxs-lookup"><span data-stu-id="c0046-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="c0046-113">此命令會停用資源群組 ResourceGroup11 中名為 ContosoProfile 之設定檔中名為 contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="c0046-114">命令會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0046-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="c0046-115">範例 2：使用管線停用端點</span><span class="sxs-lookup"><span data-stu-id="c0046-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="c0046-116">此命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中，獲得名為 Contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="c0046-117">命令接著使用管線運算子，將端點傳遞至 **Disable-AzTrafficManagerEndpoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0046-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0046-118">該 Cmdlet 會停用該端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="c0046-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="c0046-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c0046-120">因此，它不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0046-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c0046-121">參數</span><span class="sxs-lookup"><span data-stu-id="c0046-121">PARAMETERS</span></span>

### <span data-ttu-id="c0046-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0046-122">-DefaultProfile</span></span>
<span data-ttu-id="c0046-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0046-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0046-124">-強制</span><span class="sxs-lookup"><span data-stu-id="c0046-124">-Force</span></span>
<span data-ttu-id="c0046-125">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c0046-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0046-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0046-126">-Name</span></span>
<span data-ttu-id="c0046-127">指定此 Cmdlet 停用的流量管理員端點名稱。</span><span class="sxs-lookup"><span data-stu-id="c0046-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="c0046-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c0046-128">-ProfileName</span></span>
<span data-ttu-id="c0046-129">指定此 Cmdlet 停用端點的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="c0046-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="c0046-130">若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0046-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c0046-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0046-131">-ResourceGroupName</span></span>
<span data-ttu-id="c0046-132">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0046-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c0046-133">此 Cmdlet 會停用此參數指定之群組中的流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0046-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c0046-135">指定此 Cmdlet 停用的流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="c0046-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="c0046-136">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0046-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="c0046-137">-類型</span><span class="sxs-lookup"><span data-stu-id="c0046-137">-Type</span></span>
<span data-ttu-id="c0046-138">指定此 Cmdlet 新增到流量管理員設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="c0046-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="c0046-139">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="c0046-139">Valid values are:</span></span> 

- <span data-ttu-id="c0046-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="c0046-140">AzureEndpoints</span></span>
- <span data-ttu-id="c0046-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="c0046-141">ExternalEndpoints</span></span>
- <span data-ttu-id="c0046-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="c0046-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="c0046-143">-確認</span><span class="sxs-lookup"><span data-stu-id="c0046-143">-Confirm</span></span>
<span data-ttu-id="c0046-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0046-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0046-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0046-145">-WhatIf</span></span>
<span data-ttu-id="c0046-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0046-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0046-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0046-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0046-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0046-148">CommonParameters</span></span>
<span data-ttu-id="c0046-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0046-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0046-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c0046-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0046-151">輸入</span><span class="sxs-lookup"><span data-stu-id="c0046-151">INPUTS</span></span>

### <span data-ttu-id="c0046-152">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c0046-153">輸出</span><span class="sxs-lookup"><span data-stu-id="c0046-153">OUTPUTS</span></span>

### <span data-ttu-id="c0046-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0046-154">System.Boolean</span></span>

## <span data-ttu-id="c0046-155">筆記</span><span class="sxs-lookup"><span data-stu-id="c0046-155">NOTES</span></span>

## <span data-ttu-id="c0046-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0046-156">RELATED LINKS</span></span>

[<span data-ttu-id="c0046-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c0046-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c0046-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0046-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="c0046-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c0046-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0046-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c0046-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0046-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c0046-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c0046-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


