---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 79387b634bc42a4885139db35ad68a9145c02dba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916605"
---
# <span data-ttu-id="9e4e9-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-101">New-AzApiManagement</span></span>

## <span data-ttu-id="9e4e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9e4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4e9-103">建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="9e4e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="9e4e9-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4e9-105">描述</span><span class="sxs-lookup"><span data-stu-id="9e4e9-105">DESCRIPTION</span></span>
<span data-ttu-id="9e4e9-106">**New-AzApiManagement** Cmdlet 在 Azure API 管理中建立 API 管理部署。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="9e4e9-107">例子</span><span class="sxs-lookup"><span data-stu-id="9e4e9-107">EXAMPLES</span></span>

### <span data-ttu-id="9e4e9-108">範例 1：建立開發人員層 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="9e4e9-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="9e4e9-109">此命令會建立開發人員層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="9e4e9-110">命令會指定組織和系統管理員位址。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="9e4e9-111">命令不會指定 *SKU* 參數。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="9e4e9-112">因此，Cmdlet 會使用 Developer 的預設值。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="9e4e9-113">範例 2：建立具有三個單位的標準層服務</span><span class="sxs-lookup"><span data-stu-id="9e4e9-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="9e4e9-114">此命令會建立有三個單位的標準層 API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="9e4e9-115">範例 3：建立消費層級服務</span><span class="sxs-lookup"><span data-stu-id="9e4e9-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="9e4e9-116">此命令會建立消費層級 API 管理服務，並啟用西歐的用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="9e4e9-117">範例 4：為外部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="9e4e9-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="9e4e9-118">此命令在 Azure 虛擬網路子網中建立進位層 API 管理服務，其外部閘道端點具有美國西部的主區域。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="9e4e9-119">範例 5：為內部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="9e4e9-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="9e4e9-120">此命令在 Azure 虛擬網路子網中建立進一層 API 管理服務，其內部閘道端點具有美國西部的主區域。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="9e4e9-121">範例 6：建立 API 管理服務並啟用 TLS 1.0 通訊協定</span><span class="sxs-lookup"><span data-stu-id="9e4e9-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="9e4e9-122">此命令會建立標準 SKU Api 管理服務，並啟用 Frontend 用戶端上的 TLS 1.0，以在 ApiManagement 閘道和後端之間啟用 ApiManagement 閘道和後端用戶端。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="9e4e9-123">參數</span><span class="sxs-lookup"><span data-stu-id="9e4e9-123">PARAMETERS</span></span>

### <span data-ttu-id="9e4e9-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="9e4e9-124">-AdditionalRegions</span></span>
<span data-ttu-id="9e4e9-125">Azure API 管理的其他部署區域。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="9e4e9-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="9e4e9-126">-AdminEmail</span></span>
<span data-ttu-id="9e4e9-127">指定 API 管理系統傳送之所有通知的原始電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="9e4e9-128">-容量</span><span class="sxs-lookup"><span data-stu-id="9e4e9-128">-Capacity</span></span>
<span data-ttu-id="9e4e9-129">指定 Azure API 管理服務的 SKU 容量。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="9e4e9-130">預設值為 1 (1) 。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-130">The default is one (1).</span></span>

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

### <span data-ttu-id="9e4e9-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e4e9-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="9e4e9-132">自訂主機名稱組配置。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-132">Custom hostname configurations.</span></span> <span data-ttu-id="9e4e9-133">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-133">Default value is $null.</span></span> <span data-ttu-id="9e4e9-134">傳遞$null會設定預設主機名稱。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="9e4e9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4e9-135">-DefaultProfile</span></span>
<span data-ttu-id="9e4e9-136">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e4e9-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9e4e9-137">-EnableClientCertificate</span></span>
<span data-ttu-id="9e4e9-138">標號僅適用于消費 SKU ApiManagement Service。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="9e4e9-139">這會強制針對每個閘道要求呈現用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="9e4e9-140">這也可以啟用閘道上之策略中的憑證驗證功能。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="9e4e9-141">-位置</span><span class="sxs-lookup"><span data-stu-id="9e4e9-141">-Location</span></span>
<span data-ttu-id="9e4e9-142">指定建立 Api 管理服務的位置。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="9e4e9-143">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" |其中 {$_.ResourceTypes[0]。ResourceTypeName -eq "service"} |Select-Object位置</span><span class="sxs-lookup"><span data-stu-id="9e4e9-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="9e4e9-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e4e9-144">-Name</span></span>
<span data-ttu-id="9e4e9-145">指定 API 管理部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="9e4e9-146">-組織</span><span class="sxs-lookup"><span data-stu-id="9e4e9-146">-Organization</span></span>
<span data-ttu-id="9e4e9-147">指定組織的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="9e4e9-148">API 管理在電子郵件通知中的開發人員入口網站使用此位址。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="9e4e9-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4e9-149">-ResourceGroupName</span></span>
<span data-ttu-id="9e4e9-150">指定此 Cmdlet 建立 API 管理部署的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="9e4e9-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="9e4e9-151">-Sku</span></span>
<span data-ttu-id="9e4e9-152">指定 API 管理服務的層級。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="9e4e9-153">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="9e4e9-153">Valid values are:</span></span> 
- <span data-ttu-id="9e4e9-154">開發 人員</span><span class="sxs-lookup"><span data-stu-id="9e4e9-154">Developer</span></span> 
- <span data-ttu-id="9e4e9-155">標準</span><span class="sxs-lookup"><span data-stu-id="9e4e9-155">Standard</span></span> 
- <span data-ttu-id="9e4e9-156">Premium 預設為開發人員。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4e9-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="9e4e9-157">-SslSetting</span></span>
<span data-ttu-id="9e4e9-158">ApiManagement 服務的 Ssl 設定。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="9e4e9-159">預設值會$null</span><span class="sxs-lookup"><span data-stu-id="9e4e9-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4e9-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9e4e9-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="9e4e9-161">為此伺服器產生並指派 Azure Active Directory 身分識別，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9e4e9-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e4e9-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="9e4e9-163">由內部 CA 所發行的憑證，以安裝在服務上。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="9e4e9-164">預設值會$null。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-164">Default value is $null.</span></span>

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

### <span data-ttu-id="9e4e9-165">-標記</span><span class="sxs-lookup"><span data-stu-id="9e4e9-165">-Tag</span></span>
<span data-ttu-id="9e4e9-166">標記字典。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="9e4e9-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9e4e9-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="9e4e9-168">指派使用者身分驗證至此伺服器，以用於 Azure KeyVault 等重要管理服務。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4e9-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e4e9-169">-VirtualNetwork</span></span>
<span data-ttu-id="9e4e9-170">主 Azure API 管理部署地區的虛擬網路群組原則。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="9e4e9-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="9e4e9-171">-VpnType</span></span>
<span data-ttu-id="9e4e9-172">ApiManagement 部署的虛擬網路類型。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="9e4e9-173">有效的值為</span><span class="sxs-lookup"><span data-stu-id="9e4e9-173">Valid Values are</span></span> 
- <span data-ttu-id="9e4e9-174">"None" (預設值。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-174">"None" (Default Value.</span></span> <span data-ttu-id="9e4e9-175">ApiManagement 不是任何虛擬網路的一部分") </span><span class="sxs-lookup"><span data-stu-id="9e4e9-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="9e4e9-176">「外部」 (ApiManagement 部署是在具有網際網路對端點的虛擬網路中設定) </span><span class="sxs-lookup"><span data-stu-id="9e4e9-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="9e4e9-177">「內部」 (ApiManagement 部署是在有內部網路對端點的虛擬網路中設定) </span><span class="sxs-lookup"><span data-stu-id="9e4e9-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="9e4e9-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4e9-178">CommonParameters</span></span>
<span data-ttu-id="9e4e9-179">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9e4e9-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4e9-180">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e4e9-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4e9-181">輸入</span><span class="sxs-lookup"><span data-stu-id="9e4e9-181">INPUTS</span></span>

### <span data-ttu-id="9e4e9-182">System.String</span><span class="sxs-lookup"><span data-stu-id="9e4e9-182">System.String</span></span>

### <span data-ttu-id="9e4e9-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9e4e9-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9e4e9-184">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e4e9-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e4e9-185">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e4e9-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="9e4e9-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e4e9-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e4e9-187">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="9e4e9-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="9e4e9-188">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="9e4e9-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="9e4e9-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="9e4e9-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="9e4e9-190">輸出</span><span class="sxs-lookup"><span data-stu-id="9e4e9-190">OUTPUTS</span></span>

### <span data-ttu-id="9e4e9-191">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9e4e9-192">筆記</span><span class="sxs-lookup"><span data-stu-id="9e4e9-192">NOTES</span></span>

## <span data-ttu-id="9e4e9-193">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e4e9-193">RELATED LINKS</span></span>

[<span data-ttu-id="9e4e9-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="9e4e9-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="9e4e9-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="9e4e9-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="9e4e9-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e4e9-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


