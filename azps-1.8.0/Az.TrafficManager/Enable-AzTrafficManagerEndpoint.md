---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: b36d26fde2922a06f1271268ac588d912d0b72f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614347"
---
# <span data-ttu-id="493ec-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="493ec-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="493ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="493ec-102">SYNOPSIS</span></span>
<span data-ttu-id="493ec-103">啟用流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="493ec-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="493ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="493ec-104">SYNTAX</span></span>

### <span data-ttu-id="493ec-105">區域</span><span class="sxs-lookup"><span data-stu-id="493ec-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="493ec-106">面向</span><span class="sxs-lookup"><span data-stu-id="493ec-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493ec-107">說明</span><span class="sxs-lookup"><span data-stu-id="493ec-107">DESCRIPTION</span></span>
<span data-ttu-id="493ec-108">**Enable-AzTrafficManagerEndpoint** Cmdlet 可在 Azure 流量管理器設定檔中啟用端點。</span><span class="sxs-lookup"><span data-stu-id="493ec-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="493ec-109">您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數來指定 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="493ec-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="493ec-110">或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="493ec-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="493ec-111">示例</span><span class="sxs-lookup"><span data-stu-id="493ec-111">EXAMPLES</span></span>

### <span data-ttu-id="493ec-112">範例1：從設定檔啟用端點</span><span class="sxs-lookup"><span data-stu-id="493ec-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="493ec-113">這個命令會在 [資源群組 ResouceGroup11] 中，將名為 ContosoProfile 的設定檔中的外部端點啟用為 contoso。</span><span class="sxs-lookup"><span data-stu-id="493ec-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="493ec-114">範例2：使用管線啟用端點</span><span class="sxs-lookup"><span data-stu-id="493ec-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="493ec-115">這個命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中取得名為 Contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="493ec-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="493ec-116">然後，命令會使用管線運算子將該端點傳遞到 **Enable AzTrafficManagerEndpoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="493ec-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="493ec-117">該 Cmdlet 可啟用該端點。</span><span class="sxs-lookup"><span data-stu-id="493ec-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="493ec-118">參數</span><span class="sxs-lookup"><span data-stu-id="493ec-118">PARAMETERS</span></span>

### <span data-ttu-id="493ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493ec-119">-DefaultProfile</span></span>
<span data-ttu-id="493ec-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="493ec-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="493ec-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="493ec-121">-Name</span></span>
<span data-ttu-id="493ec-122">指定此 Cmdlet 啟用之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="493ec-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="493ec-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="493ec-123">-ProfileName</span></span>
<span data-ttu-id="493ec-124">指定此 Cmdlet 啟用端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="493ec-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="493ec-125">若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="493ec-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="493ec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493ec-126">-ResourceGroupName</span></span>
<span data-ttu-id="493ec-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="493ec-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="493ec-128">這個 Cmdlet 可在此參數指定的群組中啟用流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="493ec-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="493ec-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="493ec-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="493ec-130">指定此 Cmdlet 啟用的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="493ec-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="493ec-131">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="493ec-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="493ec-132">-類型</span><span class="sxs-lookup"><span data-stu-id="493ec-132">-Type</span></span>
<span data-ttu-id="493ec-133">指定此 Cmdlet 在流量管理器設定檔中停用的端點類型。</span><span class="sxs-lookup"><span data-stu-id="493ec-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="493ec-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="493ec-134">Valid values are:</span></span> 

- <span data-ttu-id="493ec-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="493ec-135">AzureEndpoints</span></span>
- <span data-ttu-id="493ec-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="493ec-136">ExternalEndpoints</span></span>
- <span data-ttu-id="493ec-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="493ec-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="493ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493ec-138">CommonParameters</span></span>
<span data-ttu-id="493ec-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="493ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493ec-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="493ec-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493ec-141">輸入</span><span class="sxs-lookup"><span data-stu-id="493ec-141">INPUTS</span></span>

### <span data-ttu-id="493ec-142">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="493ec-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="493ec-143">輸出</span><span class="sxs-lookup"><span data-stu-id="493ec-143">OUTPUTS</span></span>

### <span data-ttu-id="493ec-144">System.object</span><span class="sxs-lookup"><span data-stu-id="493ec-144">System.Boolean</span></span>

## <span data-ttu-id="493ec-145">筆記</span><span class="sxs-lookup"><span data-stu-id="493ec-145">NOTES</span></span>

## <span data-ttu-id="493ec-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="493ec-146">RELATED LINKS</span></span>

[<span data-ttu-id="493ec-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="493ec-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="493ec-148">AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="493ec-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="493ec-149">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="493ec-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="493ec-150">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="493ec-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="493ec-151">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="493ec-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="493ec-152">移除-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="493ec-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="493ec-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="493ec-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


