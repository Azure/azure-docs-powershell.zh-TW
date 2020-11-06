---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445160"
---
# <span data-ttu-id="2a4a4-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2a4a4-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="2a4a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4a4-103">更新 API 管理服務的部署。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a4a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a4a4-104">SYNTAX</span></span>

### <span data-ttu-id="2a4a4-105">特定 API 管理服務 (預設) </span><span class="sxs-lookup"><span data-stu-id="2a4a4-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4a4-106">從 PsApiManagement 實例更新</span><span class="sxs-lookup"><span data-stu-id="2a4a4-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a4a4-107">說明</span><span class="sxs-lookup"><span data-stu-id="2a4a4-107">DESCRIPTION</span></span>
<span data-ttu-id="2a4a4-108">**AzureRmApiManagementDeployment** Cmdlet 會更新 API 管理服務的目前部署。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="2a4a4-109">示例</span><span class="sxs-lookup"><span data-stu-id="2a4a4-109">EXAMPLES</span></span>

### <span data-ttu-id="2a4a4-110">範例1：更新 ApiManagement 實例的部署</span><span class="sxs-lookup"><span data-stu-id="2a4a4-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="2a4a4-111">這個命令會將 API 管理實例的部署更新為三個單位容量標準。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="2a4a4-112">範例2：取得 ApiManagement 實例並將它重新縮放</span><span class="sxs-lookup"><span data-stu-id="2a4a4-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="2a4a4-113">這個範例會取得 Api 管理實例、將它縮放至5個 premium 單位，然後再將額外的三個單元加到 premium 區域。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="2a4a4-114">範例3：更新部署 (外部 VNET) </span><span class="sxs-lookup"><span data-stu-id="2a4a4-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="2a4a4-115">這個命令會更新現有的 API 管理部署，並加入外部 *VpnType* 。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="2a4a4-116">範例4：更新部署 (內部 VNET) </span><span class="sxs-lookup"><span data-stu-id="2a4a4-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="2a4a4-117">這個命令會更新現有的 API 管理部署，並加入內部 *VpnType* 。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="2a4a4-118">參數</span><span class="sxs-lookup"><span data-stu-id="2a4a4-118">PARAMETERS</span></span>

### <span data-ttu-id="2a4a4-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="2a4a4-119">-AdditionalRegions</span></span>
<span data-ttu-id="2a4a4-120">指定 Azure API 管理的其他部署區域。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a4a4-121">-ApiManagement</span></span>
<span data-ttu-id="2a4a4-122">指定要取得部署配置的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="2a4a4-123">如果實例已有所有必要變更，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-124">-容量</span><span class="sxs-lookup"><span data-stu-id="2a4a4-124">-Capacity</span></span>
<span data-ttu-id="2a4a4-125">指定主 Azure API 管理部署區域的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-126">-位置</span><span class="sxs-lookup"><span data-stu-id="2a4a4-126">-Location</span></span>
<span data-ttu-id="2a4a4-127">指定主 API 管理部署區域的位置。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="2a4a4-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2a4a4-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a4a4-129">美國中北部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-129">North Central US</span></span>
- <span data-ttu-id="2a4a4-130">美國中南部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-130">South Central US</span></span>
- <span data-ttu-id="2a4a4-131">美國中部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-131">Central US</span></span>
- <span data-ttu-id="2a4a4-132">西歐</span><span class="sxs-lookup"><span data-stu-id="2a4a4-132">West Europe</span></span>
- <span data-ttu-id="2a4a4-133">北歐</span><span class="sxs-lookup"><span data-stu-id="2a4a4-133">North Europe</span></span>
- <span data-ttu-id="2a4a4-134">美國西部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-134">West US</span></span>
- <span data-ttu-id="2a4a4-135">東美國</span><span class="sxs-lookup"><span data-stu-id="2a4a4-135">East US</span></span>
- <span data-ttu-id="2a4a4-136">東美國2</span><span class="sxs-lookup"><span data-stu-id="2a4a4-136">East US 2</span></span>
- <span data-ttu-id="2a4a4-137">日本東</span><span class="sxs-lookup"><span data-stu-id="2a4a4-137">Japan East</span></span>
- <span data-ttu-id="2a4a4-138">日本西部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-138">Japan West</span></span>
- <span data-ttu-id="2a4a4-139">巴西南部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-139">Brazil South</span></span>
- <span data-ttu-id="2a4a4-140">東南亞</span><span class="sxs-lookup"><span data-stu-id="2a4a4-140">Southeast Asia</span></span>
- <span data-ttu-id="2a4a4-141">東亞</span><span class="sxs-lookup"><span data-stu-id="2a4a4-141">East Asia</span></span>
- <span data-ttu-id="2a4a4-142">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="2a4a4-142">Australia East</span></span>
- <span data-ttu-id="2a4a4-143">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="2a4a4-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a4a4-144">-Name</span></span>
<span data-ttu-id="2a4a4-145">指定此 Cmdlet 更新之 API 管理的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a4a4-146">-PassThru</span></span>
<span data-ttu-id="2a4a4-147">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2a4a4-148">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2a4a4-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4a4-149">-ResourceGroupName</span></span>
<span data-ttu-id="2a4a4-150">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-151">-Sku</span><span class="sxs-lookup"><span data-stu-id="2a4a4-151">-Sku</span></span>
<span data-ttu-id="2a4a4-152">指定主要 Azure API 管理部署區域的層級。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="2a4a4-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2a4a4-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a4a4-154">人員</span><span class="sxs-lookup"><span data-stu-id="2a4a4-154">Developer</span></span>
- <span data-ttu-id="2a4a4-155">標準</span><span class="sxs-lookup"><span data-stu-id="2a4a4-155">Standard</span></span>
- <span data-ttu-id="2a4a4-156">佳</span><span class="sxs-lookup"><span data-stu-id="2a4a4-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a4a4-157">-VirtualNetwork</span></span>
<span data-ttu-id="2a4a4-158">指定主 Azure API 管理部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2a4a4-159">-VpnType</span></span>
<span data-ttu-id="2a4a4-160">指定 API 管理部署的虛擬網路類型。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="2a4a4-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2a4a4-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a4a4-162">所有.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-162">None.</span></span>
<span data-ttu-id="2a4a4-163">API 管理部署不是任何虛擬網路的一部分。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="2a4a4-164">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-164">This is the default value.</span></span> 
- <span data-ttu-id="2a4a4-165">外來.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-165">External.</span></span>
<span data-ttu-id="2a4a4-166">API 管理部署有一個面向外部的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="2a4a4-167">內部.</span><span class="sxs-lookup"><span data-stu-id="2a4a4-167">Internal.</span></span>
<span data-ttu-id="2a4a4-168">API 管理部署有一個面向內部網路的虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4a4-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4a4-169">-DefaultProfile</span></span>
<span data-ttu-id="2a4a4-170">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a4a4-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4a4-171">CommonParameters</span></span>
<span data-ttu-id="2a4a4-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4a4-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4a4-174">輸入</span><span class="sxs-lookup"><span data-stu-id="2a4a4-174">INPUTS</span></span>

### <span data-ttu-id="2a4a4-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a4a4-175">PsApiManagement</span></span>
<span data-ttu-id="2a4a4-176">形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2a4a4-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="2a4a4-177">輸出</span><span class="sxs-lookup"><span data-stu-id="2a4a4-177">OUTPUTS</span></span>

### <span data-ttu-id="2a4a4-178">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="2a4a4-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2a4a4-179">筆記</span><span class="sxs-lookup"><span data-stu-id="2a4a4-179">NOTES</span></span>

## <span data-ttu-id="2a4a4-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a4a4-180">RELATED LINKS</span></span>

[<span data-ttu-id="2a4a4-181">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2a4a4-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


