---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140724"
---
# <span data-ttu-id="10239-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10239-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="10239-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10239-102">SYNOPSIS</span></span>
<span data-ttu-id="10239-103">停用流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="10239-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="10239-104">句法</span><span class="sxs-lookup"><span data-stu-id="10239-104">SYNTAX</span></span>

### <span data-ttu-id="10239-105">區域</span><span class="sxs-lookup"><span data-stu-id="10239-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10239-106">面向</span><span class="sxs-lookup"><span data-stu-id="10239-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10239-107">說明</span><span class="sxs-lookup"><span data-stu-id="10239-107">DESCRIPTION</span></span>
<span data-ttu-id="10239-108">**Disable AzTrafficManagerEndpoint** Cmdlet 會停用 Azure 流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="10239-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="10239-109">您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數傳遞 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="10239-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="10239-110">或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="10239-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="10239-111">示例</span><span class="sxs-lookup"><span data-stu-id="10239-111">EXAMPLES</span></span>

### <span data-ttu-id="10239-112">範例1：依名稱停用端點</span><span class="sxs-lookup"><span data-stu-id="10239-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="10239-113">這個命令會停用 [資源群組 ResourceGroup11] 中名為 ContosoProfile 的設定檔中名為 [contoso] 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="10239-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="10239-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10239-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="10239-115">範例2：使用管線停用端點</span><span class="sxs-lookup"><span data-stu-id="10239-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="10239-116">這個命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中取得名為 Contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="10239-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="10239-117">然後，命令會使用管線運算子將該端點傳遞到 **Disable AzTrafficManagerEndpoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10239-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="10239-118">該 Cmdlet 會停用該端點。</span><span class="sxs-lookup"><span data-stu-id="10239-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="10239-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="10239-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="10239-120">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10239-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="10239-121">參數</span><span class="sxs-lookup"><span data-stu-id="10239-121">PARAMETERS</span></span>

### <span data-ttu-id="10239-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10239-122">-DefaultProfile</span></span>
<span data-ttu-id="10239-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10239-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10239-124">-Force</span><span class="sxs-lookup"><span data-stu-id="10239-124">-Force</span></span>
<span data-ttu-id="10239-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="10239-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10239-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="10239-126">-Name</span></span>
<span data-ttu-id="10239-127">指定此 Cmdlet 停用之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="10239-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="10239-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="10239-128">-ProfileName</span></span>
<span data-ttu-id="10239-129">指定此 Cmdlet 停用端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="10239-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="10239-130">若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10239-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="10239-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10239-131">-ResourceGroupName</span></span>
<span data-ttu-id="10239-132">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="10239-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="10239-133">這個 Cmdlet 會停用此參數指定之群組中的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="10239-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="10239-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10239-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="10239-135">指定此 Cmdlet 停用的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="10239-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="10239-136">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10239-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="10239-137">-類型</span><span class="sxs-lookup"><span data-stu-id="10239-137">-Type</span></span>
<span data-ttu-id="10239-138">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="10239-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="10239-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="10239-139">Valid values are:</span></span> 

- <span data-ttu-id="10239-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="10239-140">AzureEndpoints</span></span>
- <span data-ttu-id="10239-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="10239-141">ExternalEndpoints</span></span>
- <span data-ttu-id="10239-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="10239-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="10239-143">-確認</span><span class="sxs-lookup"><span data-stu-id="10239-143">-Confirm</span></span>
<span data-ttu-id="10239-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10239-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10239-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10239-145">-WhatIf</span></span>
<span data-ttu-id="10239-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10239-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10239-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10239-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10239-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10239-148">CommonParameters</span></span>
<span data-ttu-id="10239-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10239-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10239-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10239-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10239-151">輸入</span><span class="sxs-lookup"><span data-stu-id="10239-151">INPUTS</span></span>

### <span data-ttu-id="10239-152">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="10239-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="10239-153">輸出</span><span class="sxs-lookup"><span data-stu-id="10239-153">OUTPUTS</span></span>

### <span data-ttu-id="10239-154">System.object</span><span class="sxs-lookup"><span data-stu-id="10239-154">System.Boolean</span></span>

## <span data-ttu-id="10239-155">筆記</span><span class="sxs-lookup"><span data-stu-id="10239-155">NOTES</span></span>

## <span data-ttu-id="10239-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="10239-156">RELATED LINKS</span></span>

[<span data-ttu-id="10239-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10239-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="10239-158">AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10239-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="10239-159">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10239-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="10239-160">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10239-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="10239-161">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10239-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="10239-162">移除-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10239-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="10239-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10239-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

