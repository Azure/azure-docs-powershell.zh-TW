---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 98e90b4c8275028ab3e62e7383505775271e8d09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624256"
---
# <span data-ttu-id="8cb28-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cb28-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="8cb28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8cb28-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb28-103">建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="8cb28-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb28-104">句法</span><span class="sxs-lookup"><span data-stu-id="8cb28-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cb28-105">說明</span><span class="sxs-lookup"><span data-stu-id="8cb28-105">DESCRIPTION</span></span>
<span data-ttu-id="8cb28-106">**新的-AzureRmApiManagement** Cmdlet 會在 Azure api 管理中建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="8cb28-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="8cb28-107">示例</span><span class="sxs-lookup"><span data-stu-id="8cb28-107">EXAMPLES</span></span>

### <span data-ttu-id="8cb28-108">範例1：建立開發人員層 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="8cb28-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="8cb28-109">這個命令會建立開發人員層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="8cb28-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="8cb28-110">該命令會指定組織和系統管理員的位址。</span><span class="sxs-lookup"><span data-stu-id="8cb28-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="8cb28-111">該命令不會指定 *SKU* 參數。</span><span class="sxs-lookup"><span data-stu-id="8cb28-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="8cb28-112">因此，此 Cmdlet 會使用開發人員的預設值。</span><span class="sxs-lookup"><span data-stu-id="8cb28-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="8cb28-113">範例2：建立具有三個單位的標準層服務</span><span class="sxs-lookup"><span data-stu-id="8cb28-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="8cb28-114">這個命令會建立一個具有三個單位的標準層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="8cb28-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="8cb28-115">範例3：為外部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="8cb28-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="8cb28-116">這個命令會在您的 Azure 虛擬網路子網中建立一個高級層 API 管理服務，並在其 [西部] 中有一個具有主要區域的外部閘道端點。</span><span class="sxs-lookup"><span data-stu-id="8cb28-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="8cb28-117">範例4：為內部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="8cb28-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="8cb28-118">這個命令會在 Azure 虛擬網路子網中建立一個高級層 API 管理服務，並在其 [西部] 中有一個具有主要區域的內部方閘道端點。</span><span class="sxs-lookup"><span data-stu-id="8cb28-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="8cb28-119">參數</span><span class="sxs-lookup"><span data-stu-id="8cb28-119">PARAMETERS</span></span>

### <span data-ttu-id="8cb28-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="8cb28-120">-AdditionalRegions</span></span>
<span data-ttu-id="8cb28-121">Azure API Management 的其他部署區域。</span><span class="sxs-lookup"><span data-stu-id="8cb28-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="8cb28-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="8cb28-122">-AdminEmail</span></span>
<span data-ttu-id="8cb28-123">指定 API 管理系統傳送之所有通知的原始電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="8cb28-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="8cb28-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8cb28-124">-AssignIdentity</span></span>
<span data-ttu-id="8cb28-125">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="8cb28-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8cb28-126">-容量</span><span class="sxs-lookup"><span data-stu-id="8cb28-126">-Capacity</span></span>
<span data-ttu-id="8cb28-127">指定 Azure API 管理服務的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="8cb28-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="8cb28-128">預設值是一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="8cb28-128">The default is one (1).</span></span>

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

### <span data-ttu-id="8cb28-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cb28-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="8cb28-130">自訂主機名稱設定。</span><span class="sxs-lookup"><span data-stu-id="8cb28-130">Custom hostname configurations.</span></span> <span data-ttu-id="8cb28-131">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="8cb28-131">Default value is $null.</span></span> <span data-ttu-id="8cb28-132">傳遞 $null 會設定預設的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="8cb28-132">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb28-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb28-133">-DefaultProfile</span></span>
<span data-ttu-id="8cb28-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8cb28-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cb28-135">-位置</span><span class="sxs-lookup"><span data-stu-id="8cb28-135">-Location</span></span>
<span data-ttu-id="8cb28-136">指定建立 Api 管理服務的位置。</span><span class="sxs-lookup"><span data-stu-id="8cb28-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="8cb28-137">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="8cb28-137">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="8cb28-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="8cb28-138">-Name</span></span>
<span data-ttu-id="8cb28-139">指定 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cb28-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="8cb28-140">-組織</span><span class="sxs-lookup"><span data-stu-id="8cb28-140">-Organization</span></span>
<span data-ttu-id="8cb28-141">指定組織的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cb28-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="8cb28-142">API 管理會在電子郵件通知的開發人員入口網站中使用這個位址。</span><span class="sxs-lookup"><span data-stu-id="8cb28-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="8cb28-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cb28-143">-ResourceGroupName</span></span>
<span data-ttu-id="8cb28-144">指定此 Cmdlet 建立 API 管理部署所依據之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cb28-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="8cb28-145">-Sku</span><span class="sxs-lookup"><span data-stu-id="8cb28-145">-Sku</span></span>
<span data-ttu-id="8cb28-146">指定 API 管理服務的層級。</span><span class="sxs-lookup"><span data-stu-id="8cb28-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="8cb28-147">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8cb28-147">Valid values are:</span></span> 
- <span data-ttu-id="8cb28-148">人員</span><span class="sxs-lookup"><span data-stu-id="8cb28-148">Developer</span></span> 
- <span data-ttu-id="8cb28-149">標準</span><span class="sxs-lookup"><span data-stu-id="8cb28-149">Standard</span></span> 
- <span data-ttu-id="8cb28-150">[特優] 預設值為 [開發人員]。</span><span class="sxs-lookup"><span data-stu-id="8cb28-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb28-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cb28-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="8cb28-152">內部 CA 所頒發的憑證，以安裝在服務上。</span><span class="sxs-lookup"><span data-stu-id="8cb28-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="8cb28-153">預設值為 [$null]。</span><span class="sxs-lookup"><span data-stu-id="8cb28-153">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb28-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="8cb28-154">-Tag</span></span>
<span data-ttu-id="8cb28-155">[標記字典]。</span><span class="sxs-lookup"><span data-stu-id="8cb28-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="8cb28-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8cb28-156">-VirtualNetwork</span></span>
<span data-ttu-id="8cb28-157">主 Azure API 管理部署區域的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="8cb28-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="8cb28-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="8cb28-158">-VpnType</span></span>
<span data-ttu-id="8cb28-159">ApiManagement 部署的虛擬網路類型。</span><span class="sxs-lookup"><span data-stu-id="8cb28-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="8cb28-160">有效值為</span><span class="sxs-lookup"><span data-stu-id="8cb28-160">Valid Values are</span></span> 
- <span data-ttu-id="8cb28-161">"無" (預設值。</span><span class="sxs-lookup"><span data-stu-id="8cb28-161">"None" (Default Value.</span></span> <span data-ttu-id="8cb28-162">ApiManagement 不是任何虛擬網路的一部分 ") </span><span class="sxs-lookup"><span data-stu-id="8cb28-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="8cb28-163">「外部」 (ApiManagement 部署是在擁有網際網路相關端點的虛擬網路內設定) </span><span class="sxs-lookup"><span data-stu-id="8cb28-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="8cb28-164">"內部" (ApiManagement 部署是在具有內部網路相關端點的虛擬網路內設定) </span><span class="sxs-lookup"><span data-stu-id="8cb28-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="8cb28-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb28-165">CommonParameters</span></span>
<span data-ttu-id="8cb28-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8cb28-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb28-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8cb28-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb28-168">輸入</span><span class="sxs-lookup"><span data-stu-id="8cb28-168">INPUTS</span></span>

### <span data-ttu-id="8cb28-169">System.object</span><span class="sxs-lookup"><span data-stu-id="8cb28-169">System.String</span></span>

### <span data-ttu-id="8cb28-170">ApiManagement 為 Nullable "1 [PsApiManagementSku，ApiManagement，Version = 6.1.2.0，Culture = 中性，PublicKeyToken = null]]。））。）</span><span class="sxs-lookup"><span data-stu-id="8cb28-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8cb28-171">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8cb28-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8cb28-172">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="8cb28-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="8cb28-173">[System.object]。字典 "2 [" System.object = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]，[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="8cb28-173">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="8cb28-174">PsApiManagementRegion [] 的 ApiManagement []</span><span class="sxs-lookup"><span data-stu-id="8cb28-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="8cb28-175">PsApiManagementCustomHostNameConfiguration [] 的 ApiManagement []</span><span class="sxs-lookup"><span data-stu-id="8cb28-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="8cb28-176">PsApiManagementSystemCertificate [] 的 ApiManagement []</span><span class="sxs-lookup"><span data-stu-id="8cb28-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="8cb28-177">輸出</span><span class="sxs-lookup"><span data-stu-id="8cb28-177">OUTPUTS</span></span>

### <span data-ttu-id="8cb28-178">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="8cb28-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8cb28-179">筆記</span><span class="sxs-lookup"><span data-stu-id="8cb28-179">NOTES</span></span>

## <span data-ttu-id="8cb28-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cb28-180">RELATED LINKS</span></span>

[<span data-ttu-id="8cb28-181">備份-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cb28-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="8cb28-182">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cb28-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="8cb28-183">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cb28-183">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

[<span data-ttu-id="8cb28-184">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cb28-184">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="8cb28-185">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cb28-185">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


