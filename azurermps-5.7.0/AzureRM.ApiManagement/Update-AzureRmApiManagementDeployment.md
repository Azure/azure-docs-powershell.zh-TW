---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: 62400acbb9fb70f05772bd9749e39e3d7d62cc62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449419"
---
# <span data-ttu-id="eb7e1-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="eb7e1-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="eb7e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7e1-103">更新 API 管理服務的部署。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb7e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb7e1-104">SYNTAX</span></span>

### <span data-ttu-id="eb7e1-105">UpdateSpecificService (預設) </span><span class="sxs-lookup"><span data-stu-id="eb7e1-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb7e1-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="eb7e1-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb7e1-107">說明</span><span class="sxs-lookup"><span data-stu-id="eb7e1-107">DESCRIPTION</span></span>
<span data-ttu-id="eb7e1-108">**AzureRmApiManagementDeployment** Cmdlet 會更新 API 管理服務的目前部署。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="eb7e1-109">示例</span><span class="sxs-lookup"><span data-stu-id="eb7e1-109">EXAMPLES</span></span>

### <span data-ttu-id="eb7e1-110">範例1：更新 ApiManagement 實例的部署</span><span class="sxs-lookup"><span data-stu-id="eb7e1-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="eb7e1-111">這個命令會將 API 管理實例的部署更新為三個單位容量標準。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="eb7e1-112">範例2：取得 ApiManagement 實例並將它重新縮放</span><span class="sxs-lookup"><span data-stu-id="eb7e1-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="eb7e1-113">這個範例會取得 Api 管理實例、將它縮放至5個 premium 單位，然後再將額外的三個單元加到 premium 區域。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="eb7e1-114">範例3：更新部署 (外部 VNET) </span><span class="sxs-lookup"><span data-stu-id="eb7e1-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="eb7e1-115">這個命令會更新現有的 API 管理部署，並加入外部 *VpnType* 。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="eb7e1-116">範例4：更新部署 (內部 VNET) </span><span class="sxs-lookup"><span data-stu-id="eb7e1-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="eb7e1-117">這個命令會更新現有的 API 管理部署，並加入內部 *VpnType* 。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="eb7e1-118">參數</span><span class="sxs-lookup"><span data-stu-id="eb7e1-118">PARAMETERS</span></span>

### <span data-ttu-id="eb7e1-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="eb7e1-119">-AdditionalRegions</span></span>
<span data-ttu-id="eb7e1-120">指定 Azure API 管理的其他部署區域。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb7e1-121">-ApiManagement</span></span>
<span data-ttu-id="eb7e1-122">指定要取得部署配置的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="eb7e1-123">如果實例已有所有必要變更，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-124">-容量</span><span class="sxs-lookup"><span data-stu-id="eb7e1-124">-Capacity</span></span>
<span data-ttu-id="eb7e1-125">指定主 Azure API 管理部署區域的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7e1-126">-DefaultProfile</span></span>
<span data-ttu-id="eb7e1-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="eb7e1-128">-位置</span><span class="sxs-lookup"><span data-stu-id="eb7e1-128">-Location</span></span>
<span data-ttu-id="eb7e1-129">指定主 API 管理部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-129">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="eb7e1-130">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="eb7e1-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb7e1-131">-Name</span></span>
<span data-ttu-id="eb7e1-132">指定此 Cmdlet 更新之 API 管理的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb7e1-133">-PassThru</span></span>
<span data-ttu-id="eb7e1-134">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb7e1-135">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb7e1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7e1-136">-ResourceGroupName</span></span>
<span data-ttu-id="eb7e1-137">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: UpdateSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="eb7e1-138">-Sku</span></span>
<span data-ttu-id="eb7e1-139">指定主要 Azure API 管理部署區域的層級。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-139">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="eb7e1-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="eb7e1-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb7e1-141">人員</span><span class="sxs-lookup"><span data-stu-id="eb7e1-141">Developer</span></span>
- <span data-ttu-id="eb7e1-142">標準</span><span class="sxs-lookup"><span data-stu-id="eb7e1-142">Standard</span></span>
- <span data-ttu-id="eb7e1-143">佳</span><span class="sxs-lookup"><span data-stu-id="eb7e1-143">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb7e1-144">-VirtualNetwork</span></span>
<span data-ttu-id="eb7e1-145">指定主 Azure API 管理部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="eb7e1-146">-VpnType</span></span>
<span data-ttu-id="eb7e1-147">指定 API 管理部署的虛擬網路類型。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="eb7e1-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="eb7e1-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb7e1-149">所有.</span><span class="sxs-lookup"><span data-stu-id="eb7e1-149">None.</span></span>
<span data-ttu-id="eb7e1-150">API 管理部署不是任何虛擬網路的一部分。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="eb7e1-151">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-151">This is the default value.</span></span> 
- <span data-ttu-id="eb7e1-152">外來.</span><span class="sxs-lookup"><span data-stu-id="eb7e1-152">External.</span></span>
<span data-ttu-id="eb7e1-153">API 管理部署有一個面向外部的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="eb7e1-154">內部.</span><span class="sxs-lookup"><span data-stu-id="eb7e1-154">Internal.</span></span>
<span data-ttu-id="eb7e1-155">API 管理部署有一個面向內部網路的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb7e1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7e1-156">CommonParameters</span></span>
<span data-ttu-id="eb7e1-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7e1-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7e1-159">輸入</span><span class="sxs-lookup"><span data-stu-id="eb7e1-159">INPUTS</span></span>

### <span data-ttu-id="eb7e1-160">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb7e1-160">PsApiManagement</span></span>
<span data-ttu-id="eb7e1-161">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="eb7e1-161">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="eb7e1-162">輸出</span><span class="sxs-lookup"><span data-stu-id="eb7e1-162">OUTPUTS</span></span>

### <span data-ttu-id="eb7e1-163">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="eb7e1-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="eb7e1-164">筆記</span><span class="sxs-lookup"><span data-stu-id="eb7e1-164">NOTES</span></span>

## <span data-ttu-id="eb7e1-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb7e1-165">RELATED LINKS</span></span>

[<span data-ttu-id="eb7e1-166">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb7e1-166">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


