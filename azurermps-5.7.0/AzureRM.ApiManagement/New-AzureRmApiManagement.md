---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455560"
---
# <span data-ttu-id="96325-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="96325-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="96325-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96325-102">SYNOPSIS</span></span>
<span data-ttu-id="96325-103">建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="96325-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96325-104">句法</span><span class="sxs-lookup"><span data-stu-id="96325-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96325-105">說明</span><span class="sxs-lookup"><span data-stu-id="96325-105">DESCRIPTION</span></span>
<span data-ttu-id="96325-106">**新的-AzureRmApiManagement** Cmdlet 會在 Azure api 管理中建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="96325-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="96325-107">示例</span><span class="sxs-lookup"><span data-stu-id="96325-107">EXAMPLES</span></span>

### <span data-ttu-id="96325-108">範例1：建立開發人員層 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="96325-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="96325-109">這個命令會建立開發人員層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="96325-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="96325-110">該命令會指定組織和系統管理員的位址。</span><span class="sxs-lookup"><span data-stu-id="96325-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="96325-111">該命令不會指定 *SKU* 參數。</span><span class="sxs-lookup"><span data-stu-id="96325-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="96325-112">因此，此 Cmdlet 會使用開發人員的預設值。</span><span class="sxs-lookup"><span data-stu-id="96325-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="96325-113">範例2：建立具有三個單位的標準層服務</span><span class="sxs-lookup"><span data-stu-id="96325-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="96325-114">這個命令會建立一個具有三個單位的標準層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="96325-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="96325-115">範例3：為外部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="96325-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="96325-116">這個命令會在您的 Azure 虛擬網路子網中建立一個高級層 API 管理服務，並在其 [西部] 中有一個具有主要區域的外部閘道端點。</span><span class="sxs-lookup"><span data-stu-id="96325-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="96325-117">範例4：為內部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="96325-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="96325-118">這個命令會在 Azure 虛擬網路子網中建立一個高級層 API 管理服務，並在其 [西部] 中有一個具有主要區域的內部方閘道端點。</span><span class="sxs-lookup"><span data-stu-id="96325-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="96325-119">參數</span><span class="sxs-lookup"><span data-stu-id="96325-119">PARAMETERS</span></span>

### <span data-ttu-id="96325-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="96325-120">-AdditionalRegions</span></span>
<span data-ttu-id="96325-121">Azure API Management 的其他部署區域。</span><span class="sxs-lookup"><span data-stu-id="96325-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="96325-122">-AdminEmail</span></span>
<span data-ttu-id="96325-123">指定 API 管理系統傳送之所有通知的原始電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="96325-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-124">-容量</span><span class="sxs-lookup"><span data-stu-id="96325-124">-Capacity</span></span>
<span data-ttu-id="96325-125">指定 Azure API 管理服務的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="96325-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="96325-126">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="96325-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96325-127">-DefaultProfile</span></span>
<span data-ttu-id="96325-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96325-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="96325-129">-位置</span><span class="sxs-lookup"><span data-stu-id="96325-129">-Location</span></span>
<span data-ttu-id="96325-130">指定建立 Api 管理服務的位置。</span><span class="sxs-lookup"><span data-stu-id="96325-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="96325-131">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="96325-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="96325-132">-Name</span></span>
<span data-ttu-id="96325-133">指定 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="96325-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-134">-組織</span><span class="sxs-lookup"><span data-stu-id="96325-134">-Organization</span></span>
<span data-ttu-id="96325-135">指定組織的名稱。</span><span class="sxs-lookup"><span data-stu-id="96325-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="96325-136">API 管理會在電子郵件通知的開發人員入口網站中使用這個位址。</span><span class="sxs-lookup"><span data-stu-id="96325-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96325-137">-ResourceGroupName</span></span>
<span data-ttu-id="96325-138">指定此 Cmdlet 建立 API 管理部署所依據之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96325-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="96325-139">-Sku</span></span>
<span data-ttu-id="96325-140">指定 API 管理服務的層級。</span><span class="sxs-lookup"><span data-stu-id="96325-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="96325-141">有效值為：</span><span class="sxs-lookup"><span data-stu-id="96325-141">Valid values are:</span></span> 

- <span data-ttu-id="96325-142">人員</span><span class="sxs-lookup"><span data-stu-id="96325-142">Developer</span></span> 
- <span data-ttu-id="96325-143">標準</span><span class="sxs-lookup"><span data-stu-id="96325-143">Standard</span></span> 
- <span data-ttu-id="96325-144">佳</span><span class="sxs-lookup"><span data-stu-id="96325-144">Premium</span></span> 

<span data-ttu-id="96325-145">預設為 [開發人員]。</span><span class="sxs-lookup"><span data-stu-id="96325-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="96325-146">-Tag</span></span>
<span data-ttu-id="96325-147">[標記字典]。</span><span class="sxs-lookup"><span data-stu-id="96325-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="96325-148">-VirtualNetwork</span></span>
<span data-ttu-id="96325-149">主 Azure API 管理部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="96325-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96325-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="96325-150">-VpnType</span></span>
<span data-ttu-id="96325-151">ApiManagement 部署的虛擬網路類型。</span><span class="sxs-lookup"><span data-stu-id="96325-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="96325-152">有效值為</span><span class="sxs-lookup"><span data-stu-id="96325-152">Valid Values are</span></span> 
- <span data-ttu-id="96325-153">"無" (預設值。</span><span class="sxs-lookup"><span data-stu-id="96325-153">"None" (Default Value.</span></span> <span data-ttu-id="96325-154">ApiManagement 不是任何虛擬網路的一部分 ") </span><span class="sxs-lookup"><span data-stu-id="96325-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="96325-155">「外部」 (ApiManagement 部署是在擁有網際網路相關端點的虛擬網路內設定) </span><span class="sxs-lookup"><span data-stu-id="96325-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="96325-156">"內部" (ApiManagement 部署是在具有內部網路相關端點的虛擬網路內設定) </span><span class="sxs-lookup"><span data-stu-id="96325-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96325-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96325-157">CommonParameters</span></span>
<span data-ttu-id="96325-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96325-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96325-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96325-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96325-160">輸入</span><span class="sxs-lookup"><span data-stu-id="96325-160">INPUTS</span></span>

### <span data-ttu-id="96325-161">所有</span><span class="sxs-lookup"><span data-stu-id="96325-161">None</span></span>
<span data-ttu-id="96325-162">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="96325-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96325-163">輸出</span><span class="sxs-lookup"><span data-stu-id="96325-163">OUTPUTS</span></span>

### <span data-ttu-id="96325-164">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="96325-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="96325-165">筆記</span><span class="sxs-lookup"><span data-stu-id="96325-165">NOTES</span></span>

## <span data-ttu-id="96325-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="96325-166">RELATED LINKS</span></span>

[<span data-ttu-id="96325-167">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="96325-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="96325-168">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="96325-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="96325-169">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="96325-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="96325-170">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="96325-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


