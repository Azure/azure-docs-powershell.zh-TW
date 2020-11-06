---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451991"
---
# <span data-ttu-id="5f431-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="5f431-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f431-102">SYNOPSIS</span></span>
<span data-ttu-id="5f431-103">取得流量管理器設定檔的端點。</span><span class="sxs-lookup"><span data-stu-id="5f431-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f431-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f431-104">SYNTAX</span></span>

### <span data-ttu-id="5f431-105">區域</span><span class="sxs-lookup"><span data-stu-id="5f431-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f431-106">面向</span><span class="sxs-lookup"><span data-stu-id="5f431-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f431-107">說明</span><span class="sxs-lookup"><span data-stu-id="5f431-107">DESCRIPTION</span></span>
<span data-ttu-id="5f431-108">**AzureRmTrafficManagerEndpoint** Cmdlet 會取得 Azure 流量管理器設定檔的端點。</span><span class="sxs-lookup"><span data-stu-id="5f431-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="5f431-109">您可以在本機修改這個物件，然後使用 Set-AzureRmTrafficManagerEndpoint Cmdlet 將變更套用至設定檔。</span><span class="sxs-lookup"><span data-stu-id="5f431-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="5f431-110">使用 *Name* 和 *Type* 參數指定端點。</span><span class="sxs-lookup"><span data-stu-id="5f431-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="5f431-111">您可以使用 *ProfileName* 和 *ResourceGroupName* 參數來指定流量管理器設定檔，或指定 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="5f431-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5f431-112">或者，您也可以使用管線來傳遞這個值。</span><span class="sxs-lookup"><span data-stu-id="5f431-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="5f431-113">示例</span><span class="sxs-lookup"><span data-stu-id="5f431-113">EXAMPLES</span></span>

### <span data-ttu-id="5f431-114">範例1：取得端點</span><span class="sxs-lookup"><span data-stu-id="5f431-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="5f431-115">這個命令會從名為 [ResourceGroup11] 的資源群組中，從名為 [ContosoProfile] 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="5f431-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="5f431-116">參數</span><span class="sxs-lookup"><span data-stu-id="5f431-116">PARAMETERS</span></span>

### <span data-ttu-id="5f431-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f431-117">-DefaultProfile</span></span>
<span data-ttu-id="5f431-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f431-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f431-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f431-119">-Name</span></span>
<span data-ttu-id="5f431-120">指定此 Cmdlet 所取得之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f431-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f431-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5f431-121">-ProfileName</span></span>
<span data-ttu-id="5f431-122">指定此 Cmdlet 所取得之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f431-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f431-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f431-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f431-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f431-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5f431-125">這個 Cmdlet 會在此參數指定的群組中取得流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="5f431-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f431-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5f431-127">指定此 Cmdlet 取得的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="5f431-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f431-128">-類型</span><span class="sxs-lookup"><span data-stu-id="5f431-128">-Type</span></span>
<span data-ttu-id="5f431-129">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="5f431-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="5f431-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="5f431-130">Valid values are:</span></span> 

- <span data-ttu-id="5f431-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="5f431-131">AzureEndpoints</span></span>
- <span data-ttu-id="5f431-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="5f431-132">ExternalEndpoints</span></span>
- <span data-ttu-id="5f431-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="5f431-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="5f431-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f431-134">CommonParameters</span></span>
<span data-ttu-id="5f431-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f431-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f431-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f431-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f431-137">輸入</span><span class="sxs-lookup"><span data-stu-id="5f431-137">INPUTS</span></span>

### <span data-ttu-id="5f431-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="5f431-139">形參 "TrafficManagerEndpoint" 接受管線中 "TrafficManagerEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5f431-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="5f431-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5f431-140">OUTPUTS</span></span>

### <span data-ttu-id="5f431-141">TrafficManagerEndpoint 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="5f431-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5f431-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5f431-142">NOTES</span></span>

## <span data-ttu-id="5f431-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f431-143">RELATED LINKS</span></span>

[<span data-ttu-id="5f431-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5f431-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5f431-146">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5f431-147">移除-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="5f431-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f431-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


