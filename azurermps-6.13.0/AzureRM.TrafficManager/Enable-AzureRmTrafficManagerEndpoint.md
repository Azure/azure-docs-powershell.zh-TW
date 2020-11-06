---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 2556715c321ddcc3f8acbc518ddbe6a3048353af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448868"
---
# <span data-ttu-id="a47a5-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a47a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a47a5-102">SYNOPSIS</span></span>
<span data-ttu-id="a47a5-103">啟用流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="a47a5-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a47a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a47a5-104">SYNTAX</span></span>

### <span data-ttu-id="a47a5-105">區域</span><span class="sxs-lookup"><span data-stu-id="a47a5-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a47a5-106">面向</span><span class="sxs-lookup"><span data-stu-id="a47a5-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a47a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="a47a5-107">DESCRIPTION</span></span>
<span data-ttu-id="a47a5-108">**Enable-AzureRmTrafficManagerEndpoint** Cmdlet 可在 Azure 流量管理器設定檔中啟用端點。</span><span class="sxs-lookup"><span data-stu-id="a47a5-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a47a5-109">您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數來指定 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="a47a5-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="a47a5-110">或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="a47a5-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="a47a5-111">示例</span><span class="sxs-lookup"><span data-stu-id="a47a5-111">EXAMPLES</span></span>

### <span data-ttu-id="a47a5-112">範例1：從設定檔啟用端點</span><span class="sxs-lookup"><span data-stu-id="a47a5-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="a47a5-113">這個命令會在 [資源群組 ResouceGroup11] 中，將名為 ContosoProfile 的設定檔中的外部端點啟用為 contoso。</span><span class="sxs-lookup"><span data-stu-id="a47a5-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="a47a5-114">範例2：使用管線啟用端點</span><span class="sxs-lookup"><span data-stu-id="a47a5-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="a47a5-115">這個命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中取得名為 Contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="a47a5-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a47a5-116">然後，命令會使用管線運算子將該端點傳遞到 **Enable AzureRmTrafficManagerEndpoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a47a5-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a47a5-117">該 Cmdlet 可啟用該端點。</span><span class="sxs-lookup"><span data-stu-id="a47a5-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="a47a5-118">參數</span><span class="sxs-lookup"><span data-stu-id="a47a5-118">PARAMETERS</span></span>

### <span data-ttu-id="a47a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47a5-119">-DefaultProfile</span></span>
<span data-ttu-id="a47a5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a47a5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47a5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a47a5-121">-Name</span></span>
<span data-ttu-id="a47a5-122">指定此 Cmdlet 啟用之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a47a5-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="a47a5-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a47a5-123">-ProfileName</span></span>
<span data-ttu-id="a47a5-124">指定此 Cmdlet 啟用端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="a47a5-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="a47a5-125">若要取得設定檔，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a47a5-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a47a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="a47a5-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a47a5-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a47a5-128">這個 Cmdlet 可在此參數指定的群組中啟用流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="a47a5-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a47a5-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a47a5-130">指定此 Cmdlet 啟用的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="a47a5-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="a47a5-131">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a47a5-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="a47a5-132">-類型</span><span class="sxs-lookup"><span data-stu-id="a47a5-132">-Type</span></span>
<span data-ttu-id="a47a5-133">指定此 Cmdlet 在流量管理器設定檔中停用的端點類型。</span><span class="sxs-lookup"><span data-stu-id="a47a5-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="a47a5-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a47a5-134">Valid values are:</span></span> 

- <span data-ttu-id="a47a5-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a47a5-135">AzureEndpoints</span></span>
- <span data-ttu-id="a47a5-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a47a5-136">ExternalEndpoints</span></span>
- <span data-ttu-id="a47a5-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="a47a5-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="a47a5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47a5-138">CommonParameters</span></span>
<span data-ttu-id="a47a5-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a47a5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47a5-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a47a5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47a5-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a47a5-141">INPUTS</span></span>

### <span data-ttu-id="a47a5-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="a47a5-143">形參 "TrafficManagerEndpoint" 接受管線中 "TrafficManagerEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a47a5-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a47a5-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a47a5-144">OUTPUTS</span></span>

### <span data-ttu-id="a47a5-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a47a5-145">System.Boolean</span></span>

## <span data-ttu-id="a47a5-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a47a5-146">NOTES</span></span>

## <span data-ttu-id="a47a5-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a47a5-147">RELATED LINKS</span></span>

[<span data-ttu-id="a47a5-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a47a5-149">AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a47a5-150">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a47a5-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a47a5-151">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a47a5-152">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a47a5-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a47a5-153">移除-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a47a5-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a47a5-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a47a5-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


