---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 13b798da7b35a4721b35d2375cf4e25bb47fbb98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624650"
---
# <span data-ttu-id="ece7c-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ece7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ece7c-102">SYNOPSIS</span></span>
<span data-ttu-id="ece7c-103">停用流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ece7c-104">SYNTAX</span></span>

### <span data-ttu-id="ece7c-105">區域</span><span class="sxs-lookup"><span data-stu-id="ece7c-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ece7c-106">面向</span><span class="sxs-lookup"><span data-stu-id="ece7c-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece7c-107">說明</span><span class="sxs-lookup"><span data-stu-id="ece7c-107">DESCRIPTION</span></span>
<span data-ttu-id="ece7c-108">**Disable AzureRmTrafficManagerEndpoint** Cmdlet 會停用 Azure 流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="ece7c-109">您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數傳遞 **TrafficManagerEndpoint** 物件。</span><span class="sxs-lookup"><span data-stu-id="ece7c-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="ece7c-110">或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。</span><span class="sxs-lookup"><span data-stu-id="ece7c-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="ece7c-111">示例</span><span class="sxs-lookup"><span data-stu-id="ece7c-111">EXAMPLES</span></span>

### <span data-ttu-id="ece7c-112">範例1：依名稱停用端點</span><span class="sxs-lookup"><span data-stu-id="ece7c-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="ece7c-113">這個命令會停用 [資源群組 ResouceGroup11] 中名為 ContosoProfile 的設定檔中名為 [contoso] 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="ece7c-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ece7c-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="ece7c-115">範例2：使用管線停用端點</span><span class="sxs-lookup"><span data-stu-id="ece7c-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="ece7c-116">這個命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中取得名為 Contoso 的外部端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="ece7c-117">然後，命令會使用管線運算子將該端點傳遞到 **Disable AzureRmTrafficManagerEndpoint** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece7c-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ece7c-118">該 Cmdlet 會停用該端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="ece7c-119">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="ece7c-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ece7c-120">因此，它不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ece7c-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ece7c-121">參數</span><span class="sxs-lookup"><span data-stu-id="ece7c-121">PARAMETERS</span></span>

### <span data-ttu-id="ece7c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece7c-122">-DefaultProfile</span></span>
<span data-ttu-id="ece7c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ece7c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece7c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ece7c-124">-Force</span></span>
<span data-ttu-id="ece7c-125">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ece7c-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ece7c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="ece7c-126">-Name</span></span>
<span data-ttu-id="ece7c-127">指定此 Cmdlet 停用之流量管理器端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ece7c-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="ece7c-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ece7c-128">-ProfileName</span></span>
<span data-ttu-id="ece7c-129">指定此 Cmdlet 停用端點的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ece7c-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="ece7c-130">若要取得設定檔，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece7c-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ece7c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece7c-131">-ResourceGroupName</span></span>
<span data-ttu-id="ece7c-132">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ece7c-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ece7c-133">這個 Cmdlet 會停用此參數指定之群組中的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ece7c-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ece7c-135">指定此 Cmdlet 停用的流量管理器端點。</span><span class="sxs-lookup"><span data-stu-id="ece7c-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="ece7c-136">若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzureRmTrafficManagerEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece7c-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="ece7c-137">-類型</span><span class="sxs-lookup"><span data-stu-id="ece7c-137">-Type</span></span>
<span data-ttu-id="ece7c-138">指定此 Cmdlet 新增至流量管理器設定檔的端點類型。</span><span class="sxs-lookup"><span data-stu-id="ece7c-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="ece7c-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ece7c-139">Valid values are:</span></span> 

- <span data-ttu-id="ece7c-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ece7c-140">AzureEndpoints</span></span>
- <span data-ttu-id="ece7c-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ece7c-141">ExternalEndpoints</span></span>
- <span data-ttu-id="ece7c-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ece7c-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="ece7c-143">-確認</span><span class="sxs-lookup"><span data-stu-id="ece7c-143">-Confirm</span></span>
<span data-ttu-id="ece7c-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ece7c-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece7c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece7c-145">-WhatIf</span></span>
<span data-ttu-id="ece7c-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ece7c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece7c-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ece7c-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece7c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece7c-148">CommonParameters</span></span>
<span data-ttu-id="ece7c-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ece7c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece7c-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ece7c-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece7c-151">輸入</span><span class="sxs-lookup"><span data-stu-id="ece7c-151">INPUTS</span></span>

### <span data-ttu-id="ece7c-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="ece7c-153">形參 "TrafficManagerEndpoint" 接受管線中 "TrafficManagerEndpoint" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ece7c-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ece7c-154">輸出</span><span class="sxs-lookup"><span data-stu-id="ece7c-154">OUTPUTS</span></span>

### <span data-ttu-id="ece7c-155">System.object</span><span class="sxs-lookup"><span data-stu-id="ece7c-155">System.Boolean</span></span>

## <span data-ttu-id="ece7c-156">筆記</span><span class="sxs-lookup"><span data-stu-id="ece7c-156">NOTES</span></span>

## <span data-ttu-id="ece7c-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ece7c-157">RELATED LINKS</span></span>

[<span data-ttu-id="ece7c-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ece7c-159">AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ece7c-160">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ece7c-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ece7c-161">新-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ece7c-162">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ece7c-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ece7c-163">移除-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ece7c-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ece7c-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ece7c-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


