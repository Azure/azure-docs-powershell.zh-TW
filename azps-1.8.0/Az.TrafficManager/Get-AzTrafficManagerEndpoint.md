---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614346"
---
# <span data-ttu-id="1c098-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c098-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c098-102">SYNOPSIS</span></span>
<span data-ttu-id="1c098-103">取得流量管理器設定檔的端點。</span><span class="sxs-lookup"><span data-stu-id="1c098-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="1c098-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c098-104">SYNTAX</span></span>

### <span data-ttu-id="1c098-105">區域</span><span class="sxs-lookup"><span data-stu-id="1c098-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c098-106">面向</span><span class="sxs-lookup"><span data-stu-id="1c098-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c098-107">說明</span><span class="sxs-lookup"><span data-stu-id="1c098-107">DESCRIPTION</span></span>
<span data-ttu-id="1c098-108">**AzTrafficManagerEndpoint** Cmdlet 會取得 Azure 流量管理器設定檔的端點。</span><span class="sxs-lookup"><span data-stu-id="1c098-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="1c098-109">您可以在本機修改這個物件，然後使用 Set-AzTrafficManagerEndpoint Cmdlet 將變更套用至設定檔。</span><span class="sxs-lookup"><span data-stu-id="1c098-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="1c098-110">使用 *Name* 和 *Type* 參數指定端點。</span><span class="sxs-lookup"><span data-stu-id="1c098-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="1c098-111">您可以使用 *ProfileName* 和 *ResourceGroupName* 參數來指定流量管理器設定檔，或指定 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="1c098-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1c098-112">或者，您也可以使用管線來傳遞這個值。</span><span class="sxs-lookup"><span data-stu-id="1c098-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="1c098-113">示例</span><span class="sxs-lookup"><span data-stu-id="1c098-113">EXAMPLES</span></span>

### <span data-ttu-id="1c098-114">範例1：取得端點</span><span class="sxs-lookup"><span data-stu-id="1c098-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="1c098-115">這個命令會從名為 [ResourceGroup11] 的資源群組中，從名為 [ContosoProfile] 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="1c098-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="1c098-116">參數</span><span class="sxs-lookup"><span data-stu-id="1c098-116">PARAMETERS</span></span>

### <span data-ttu-id="1c098-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c098-117">-DefaultProfile</span></span>
<span data-ttu-id="1c098-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c098-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c098-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c098-119">-Name</span></span>
<span data-ttu-id="1c098-120">指定此 Cmdlet 所取得之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c098-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c098-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1c098-121">-ProfileName</span></span>
<span data-ttu-id="1c098-122">指定此 Cmdlet 所取得之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c098-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c098-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c098-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c098-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c098-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1c098-125">這個 Cmdlet 會在此參數指定的群組中取得流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="1c098-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c098-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="1c098-127">指定此 Cmdlet 取得的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="1c098-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1c098-128">-類型</span><span class="sxs-lookup"><span data-stu-id="1c098-128">-Type</span></span>
<span data-ttu-id="1c098-129">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="1c098-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="1c098-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="1c098-130">Valid values are:</span></span> 

- <span data-ttu-id="1c098-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c098-131">AzureEndpoints</span></span>
- <span data-ttu-id="1c098-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c098-132">ExternalEndpoints</span></span>
- <span data-ttu-id="1c098-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="1c098-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="1c098-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c098-134">CommonParameters</span></span>
<span data-ttu-id="1c098-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c098-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c098-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c098-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c098-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1c098-137">INPUTS</span></span>

### <span data-ttu-id="1c098-138">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="1c098-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c098-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1c098-139">OUTPUTS</span></span>

### <span data-ttu-id="1c098-140">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="1c098-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="1c098-141">筆記</span><span class="sxs-lookup"><span data-stu-id="1c098-141">NOTES</span></span>

## <span data-ttu-id="1c098-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c098-142">RELATED LINKS</span></span>

[<span data-ttu-id="1c098-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c098-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c098-145">新-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c098-146">移除-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="1c098-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c098-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)

