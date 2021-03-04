---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5ab6ba03b9803cc8726eff458776f8ee40d48793
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901621"
---
# <span data-ttu-id="427cd-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="427cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="427cd-102">SYNOPSIS</span></span>
<span data-ttu-id="427cd-103">啟用流量管理員設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="427cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="427cd-104">SYNTAX</span></span>

### <span data-ttu-id="427cd-105">領域</span><span class="sxs-lookup"><span data-stu-id="427cd-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="427cd-106">物件</span><span class="sxs-lookup"><span data-stu-id="427cd-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="427cd-107">描述</span><span class="sxs-lookup"><span data-stu-id="427cd-107">DESCRIPTION</span></span>
<span data-ttu-id="427cd-108">**Enable-AzTrafficManagerEndpoint** Cmdlet 可啟用 Azure 流量管理員設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="427cd-109">您可以使用管線運算子將 **TrafficManagerEndpoint** 物件傳遞到此 Cmdlet，或者您可以使用 **TrafficManagerEndpoint 參數指定 TrafficManagerEndpoint** *物件* 。</span><span class="sxs-lookup"><span data-stu-id="427cd-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="427cd-110">或者，您也可以使用名稱和類型參數，以及 *ProfileName* 和 *ResourceGroupName* 參數來指定端點名稱並輸入。 </span><span class="sxs-lookup"><span data-stu-id="427cd-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="427cd-111">例子</span><span class="sxs-lookup"><span data-stu-id="427cd-111">EXAMPLES</span></span>

### <span data-ttu-id="427cd-112">範例 1：從設定檔啟用端點</span><span class="sxs-lookup"><span data-stu-id="427cd-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="427cd-113">此命令會啟用資源群組 ResourceGroup11 中名為 ContosoProfile 之設定檔中名為 contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="427cd-114">範例 2：使用管線啟用端點</span><span class="sxs-lookup"><span data-stu-id="427cd-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="427cd-115">此命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中，獲得名為 Contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="427cd-116">命令接著使用管線運算子，將端點傳遞至 **Enable-AzTrafficManagerEndpoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="427cd-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="427cd-117">該 Cmdlet 會啟用該端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="427cd-118">參數</span><span class="sxs-lookup"><span data-stu-id="427cd-118">PARAMETERS</span></span>

### <span data-ttu-id="427cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427cd-119">-DefaultProfile</span></span>
<span data-ttu-id="427cd-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="427cd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="427cd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="427cd-121">-Name</span></span>
<span data-ttu-id="427cd-122">指定此 Cmdlet 啟用的流量管理員端點名稱。</span><span class="sxs-lookup"><span data-stu-id="427cd-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="427cd-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="427cd-123">-ProfileName</span></span>
<span data-ttu-id="427cd-124">指定此 Cmdlet 啟用端點的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="427cd-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="427cd-125">若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="427cd-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="427cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="427cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="427cd-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="427cd-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="427cd-128">此 Cmdlet 會啟用此參數指定之群組中的流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="427cd-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="427cd-130">指定此 Cmdlet 啟用的流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="427cd-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="427cd-131">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="427cd-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="427cd-132">-類型</span><span class="sxs-lookup"><span data-stu-id="427cd-132">-Type</span></span>
<span data-ttu-id="427cd-133">指定此 Cmdlet 在流量管理員設定檔中停用的端點類型。</span><span class="sxs-lookup"><span data-stu-id="427cd-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="427cd-134">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="427cd-134">Valid values are:</span></span> 

- <span data-ttu-id="427cd-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="427cd-135">AzureEndpoints</span></span>
- <span data-ttu-id="427cd-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="427cd-136">ExternalEndpoints</span></span>
- <span data-ttu-id="427cd-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="427cd-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="427cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427cd-138">CommonParameters</span></span>
<span data-ttu-id="427cd-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="427cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427cd-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="427cd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427cd-141">輸入</span><span class="sxs-lookup"><span data-stu-id="427cd-141">INPUTS</span></span>

### <span data-ttu-id="427cd-142">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="427cd-143">輸出</span><span class="sxs-lookup"><span data-stu-id="427cd-143">OUTPUTS</span></span>

### <span data-ttu-id="427cd-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="427cd-144">System.Boolean</span></span>

## <span data-ttu-id="427cd-145">筆記</span><span class="sxs-lookup"><span data-stu-id="427cd-145">NOTES</span></span>

## <span data-ttu-id="427cd-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="427cd-146">RELATED LINKS</span></span>

[<span data-ttu-id="427cd-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="427cd-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="427cd-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="427cd-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="427cd-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="427cd-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="427cd-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="427cd-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="427cd-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="427cd-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="427cd-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


