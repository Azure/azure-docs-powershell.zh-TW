---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 04764a27a6940c0bc2b5d0e6df0baad350606972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901617"
---
# <span data-ttu-id="06a83-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="06a83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06a83-102">SYNOPSIS</span></span>
<span data-ttu-id="06a83-103">獲得流量管理員設定檔的端點。</span><span class="sxs-lookup"><span data-stu-id="06a83-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="06a83-104">語法</span><span class="sxs-lookup"><span data-stu-id="06a83-104">SYNTAX</span></span>

### <span data-ttu-id="06a83-105">領域</span><span class="sxs-lookup"><span data-stu-id="06a83-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06a83-106">物件</span><span class="sxs-lookup"><span data-stu-id="06a83-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06a83-107">描述</span><span class="sxs-lookup"><span data-stu-id="06a83-107">DESCRIPTION</span></span>
<span data-ttu-id="06a83-108">**Get-AzTrafficManagerEndpoint** Cmdlet 會取得 Azure 流量管理員設定檔的端點。</span><span class="sxs-lookup"><span data-stu-id="06a83-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="06a83-109">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzTrafficManagerEndpoint設定檔。</span><span class="sxs-lookup"><span data-stu-id="06a83-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="06a83-110">使用名稱和類型參數 *指定* 端點。</span><span class="sxs-lookup"><span data-stu-id="06a83-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="06a83-111">您可以使用 *ProfileName* 和 *ResourceGroupName* 參數指定流量管理員設定檔，或指定 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="06a83-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="06a83-112">或者，您可以使用管線傳遞該值。</span><span class="sxs-lookup"><span data-stu-id="06a83-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="06a83-113">例子</span><span class="sxs-lookup"><span data-stu-id="06a83-113">EXAMPLES</span></span>

### <span data-ttu-id="06a83-114">範例 1：取得端點</span><span class="sxs-lookup"><span data-stu-id="06a83-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="06a83-115">此命令會從名為 ResourceGroup11 的資源群組中名為 ContosoProfile 的設定檔中，將 Azure 端點命名為 contoso，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="06a83-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="06a83-116">參數</span><span class="sxs-lookup"><span data-stu-id="06a83-116">PARAMETERS</span></span>

### <span data-ttu-id="06a83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a83-117">-DefaultProfile</span></span>
<span data-ttu-id="06a83-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="06a83-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a83-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="06a83-119">-Name</span></span>
<span data-ttu-id="06a83-120">指定此 Cmdlet 所獲得流量管理員端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="06a83-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06a83-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="06a83-121">-ProfileName</span></span>
<span data-ttu-id="06a83-122">指定此 Cmdlet 所獲得流量管理員端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="06a83-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06a83-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a83-123">-ResourceGroupName</span></span>
<span data-ttu-id="06a83-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06a83-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="06a83-125">此 Cmdlet 會在此參數指定的群組中，獲得流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="06a83-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="06a83-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="06a83-127">指定此 Cmdlet 獲得的流量管理員端點。</span><span class="sxs-lookup"><span data-stu-id="06a83-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06a83-128">-類型</span><span class="sxs-lookup"><span data-stu-id="06a83-128">-Type</span></span>
<span data-ttu-id="06a83-129">指定此 Cmdlet 新增到流量管理員設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="06a83-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="06a83-130">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="06a83-130">Valid values are:</span></span> 

- <span data-ttu-id="06a83-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="06a83-131">AzureEndpoints</span></span>
- <span data-ttu-id="06a83-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="06a83-132">ExternalEndpoints</span></span>
- <span data-ttu-id="06a83-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="06a83-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="06a83-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a83-134">CommonParameters</span></span>
<span data-ttu-id="06a83-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06a83-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a83-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="06a83-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a83-137">輸入</span><span class="sxs-lookup"><span data-stu-id="06a83-137">INPUTS</span></span>

### <span data-ttu-id="06a83-138">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="06a83-139">輸出</span><span class="sxs-lookup"><span data-stu-id="06a83-139">OUTPUTS</span></span>

### <span data-ttu-id="06a83-140">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="06a83-141">筆記</span><span class="sxs-lookup"><span data-stu-id="06a83-141">NOTES</span></span>

## <span data-ttu-id="06a83-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="06a83-142">RELATED LINKS</span></span>

[<span data-ttu-id="06a83-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06a83-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06a83-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06a83-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="06a83-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06a83-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


