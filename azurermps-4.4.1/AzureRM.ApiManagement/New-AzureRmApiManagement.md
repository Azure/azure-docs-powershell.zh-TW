---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450123"
---
# <span data-ttu-id="003d0-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="003d0-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="003d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="003d0-102">SYNOPSIS</span></span>
<span data-ttu-id="003d0-103">建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="003d0-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="003d0-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="003d0-105">DESCRIPTION</span></span>
<span data-ttu-id="003d0-106">**新的-AzureRmApiManagement** Cmdlet 會在 Azure api 管理中建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="003d0-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="003d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="003d0-107">EXAMPLES</span></span>

### <span data-ttu-id="003d0-108">範例1：建立開發人員層 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="003d0-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="003d0-109">這個命令會建立開發人員層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="003d0-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="003d0-110">該命令會指定組織和系統管理員的位址。</span><span class="sxs-lookup"><span data-stu-id="003d0-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="003d0-111">該命令不會指定 *SKU* 參數。</span><span class="sxs-lookup"><span data-stu-id="003d0-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="003d0-112">因此，此 Cmdlet 會使用開發人員的預設值。</span><span class="sxs-lookup"><span data-stu-id="003d0-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="003d0-113">範例2：建立具有三個單位的標準層服務</span><span class="sxs-lookup"><span data-stu-id="003d0-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="003d0-114">這個命令會建立一個具有三個單位的標準層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="003d0-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="003d0-115">範例3：為外部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="003d0-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="003d0-116">這個命令會在您的 Azure 虛擬網路子網中建立一個高級層 API 管理服務，並在其 [西部] 中有一個具有主要區域的外部閘道端點。</span><span class="sxs-lookup"><span data-stu-id="003d0-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="003d0-117">範例4：為內部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="003d0-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="003d0-118">這個命令會在 Azure 虛擬網路子網中建立一個高級層 API 管理服務，並在其 [西部] 中有一個具有主要區域的內部方閘道端點。</span><span class="sxs-lookup"><span data-stu-id="003d0-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="003d0-119">參數</span><span class="sxs-lookup"><span data-stu-id="003d0-119">PARAMETERS</span></span>

### <span data-ttu-id="003d0-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="003d0-120">-AdditionalRegions</span></span>
<span data-ttu-id="003d0-121">Azure API Management 的其他部署區域。</span><span class="sxs-lookup"><span data-stu-id="003d0-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="003d0-122">-AdminEmail</span></span>
<span data-ttu-id="003d0-123">指定 API 管理系統傳送之所有通知的原始電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="003d0-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-124">-容量</span><span class="sxs-lookup"><span data-stu-id="003d0-124">-Capacity</span></span>
<span data-ttu-id="003d0-125">指定 Azure API 管理服務的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="003d0-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="003d0-126">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="003d0-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-127">-位置</span><span class="sxs-lookup"><span data-stu-id="003d0-127">-Location</span></span>
<span data-ttu-id="003d0-128">指定此 Cmdlet 建立 API 管理部署的位置。</span><span class="sxs-lookup"><span data-stu-id="003d0-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="003d0-129">若要取得有效的位置，請使用 Get-AzureLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="003d0-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="003d0-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="003d0-130">Valid values are:</span></span> 

- <span data-ttu-id="003d0-131">美國中北部</span><span class="sxs-lookup"><span data-stu-id="003d0-131">North Central US</span></span>
- <span data-ttu-id="003d0-132">美國中南部</span><span class="sxs-lookup"><span data-stu-id="003d0-132">South Central US</span></span>
- <span data-ttu-id="003d0-133">美國中部</span><span class="sxs-lookup"><span data-stu-id="003d0-133">Central US</span></span>
- <span data-ttu-id="003d0-134">西歐</span><span class="sxs-lookup"><span data-stu-id="003d0-134">West Europe</span></span>
- <span data-ttu-id="003d0-135">北歐</span><span class="sxs-lookup"><span data-stu-id="003d0-135">North Europe</span></span>
- <span data-ttu-id="003d0-136">美國西部</span><span class="sxs-lookup"><span data-stu-id="003d0-136">West US</span></span>
- <span data-ttu-id="003d0-137">東美國</span><span class="sxs-lookup"><span data-stu-id="003d0-137">East US</span></span>
- <span data-ttu-id="003d0-138">東美國2</span><span class="sxs-lookup"><span data-stu-id="003d0-138">East US 2</span></span>
- <span data-ttu-id="003d0-139">日本東</span><span class="sxs-lookup"><span data-stu-id="003d0-139">Japan East</span></span>
- <span data-ttu-id="003d0-140">日本西部</span><span class="sxs-lookup"><span data-stu-id="003d0-140">Japan West</span></span>
- <span data-ttu-id="003d0-141">巴西南部</span><span class="sxs-lookup"><span data-stu-id="003d0-141">Brazil South</span></span>
- <span data-ttu-id="003d0-142">東南亞</span><span class="sxs-lookup"><span data-stu-id="003d0-142">Southeast Asia</span></span>
- <span data-ttu-id="003d0-143">東亞</span><span class="sxs-lookup"><span data-stu-id="003d0-143">East Asia</span></span>
- <span data-ttu-id="003d0-144">澳大利亞東</span><span class="sxs-lookup"><span data-stu-id="003d0-144">Australia East</span></span>
- <span data-ttu-id="003d0-145">澳大利亞東南部</span><span class="sxs-lookup"><span data-stu-id="003d0-145">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="003d0-146">-Name</span></span>
<span data-ttu-id="003d0-147">指定 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="003d0-147">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-148">-組織</span><span class="sxs-lookup"><span data-stu-id="003d0-148">-Organization</span></span>
<span data-ttu-id="003d0-149">指定組織的名稱。</span><span class="sxs-lookup"><span data-stu-id="003d0-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="003d0-150">API 管理會在電子郵件通知的開發人員入口網站中使用這個位址。</span><span class="sxs-lookup"><span data-stu-id="003d0-150">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003d0-151">-ResourceGroupName</span></span>
<span data-ttu-id="003d0-152">指定此 Cmdlet 建立 API 管理部署所依據之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="003d0-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="003d0-153">-Sku</span></span>
<span data-ttu-id="003d0-154">指定 API 管理服務的層級。</span><span class="sxs-lookup"><span data-stu-id="003d0-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="003d0-155">有效值為：</span><span class="sxs-lookup"><span data-stu-id="003d0-155">Valid values are:</span></span> 

- <span data-ttu-id="003d0-156">人員</span><span class="sxs-lookup"><span data-stu-id="003d0-156">Developer</span></span> 
- <span data-ttu-id="003d0-157">標準</span><span class="sxs-lookup"><span data-stu-id="003d0-157">Standard</span></span> 
- <span data-ttu-id="003d0-158">佳</span><span class="sxs-lookup"><span data-stu-id="003d0-158">Premium</span></span> 

<span data-ttu-id="003d0-159">預設為 [開發人員]。</span><span class="sxs-lookup"><span data-stu-id="003d0-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-160">-標記</span><span class="sxs-lookup"><span data-stu-id="003d0-160">-Tags</span></span>
<span data-ttu-id="003d0-161">指定標記的字典。</span><span class="sxs-lookup"><span data-stu-id="003d0-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="003d0-162">-VirtualNetwork</span></span>
<span data-ttu-id="003d0-163">主 Azure API 管理部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="003d0-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="003d0-164">-VpnType</span></span>
<span data-ttu-id="003d0-165">ApiManagement 部署的虛擬網路類型。</span><span class="sxs-lookup"><span data-stu-id="003d0-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="003d0-166">有效值為</span><span class="sxs-lookup"><span data-stu-id="003d0-166">Valid Values are</span></span> 
- <span data-ttu-id="003d0-167">"無" (預設值。</span><span class="sxs-lookup"><span data-stu-id="003d0-167">"None" (Default Value.</span></span> <span data-ttu-id="003d0-168">ApiManagement 不是任何虛擬網路的一部分 ") </span><span class="sxs-lookup"><span data-stu-id="003d0-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="003d0-169">「外部」 (ApiManagement 部署是在擁有網際網路相關端點的虛擬網路內設定) </span><span class="sxs-lookup"><span data-stu-id="003d0-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="003d0-170">"內部" (ApiManagement 部署是在具有內部網路相關端點的虛擬網路內設定) </span><span class="sxs-lookup"><span data-stu-id="003d0-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003d0-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003d0-171">-DefaultProfile</span></span>
<span data-ttu-id="003d0-172">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="003d0-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="003d0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003d0-173">CommonParameters</span></span>
<span data-ttu-id="003d0-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="003d0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003d0-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="003d0-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003d0-176">輸入</span><span class="sxs-lookup"><span data-stu-id="003d0-176">INPUTS</span></span>

## <span data-ttu-id="003d0-177">輸出</span><span class="sxs-lookup"><span data-stu-id="003d0-177">OUTPUTS</span></span>

### <span data-ttu-id="003d0-178">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="003d0-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="003d0-179">筆記</span><span class="sxs-lookup"><span data-stu-id="003d0-179">NOTES</span></span>

## <span data-ttu-id="003d0-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="003d0-180">RELATED LINKS</span></span>

[<span data-ttu-id="003d0-181">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="003d0-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="003d0-182">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="003d0-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="003d0-183">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="003d0-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="003d0-184">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="003d0-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


