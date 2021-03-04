---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 62e642208e11ece3aeaab009920a5c30b53c0636
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911817"
---
# <span data-ttu-id="1c1cd-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c1cd-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="1c1cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1cd-103">新增 Azure Resource Manager 實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="1c1cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c1cd-104">SYNTAX</span></span>

### <span data-ttu-id="1c1cd-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="1c1cd-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c1cd-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c1cd-107">發現</span><span class="sxs-lookup"><span data-stu-id="1c1cd-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c1cd-108">描述</span><span class="sxs-lookup"><span data-stu-id="1c1cd-108">DESCRIPTION</span></span>
<span data-ttu-id="1c1cd-109">此Add-AzEnvironment Cmdlet 會新增端點和中繼資料，以啟用 Azure Resource Manager Cmdlet 與 Azure Resource Manager 的新實例進行連接。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="1c1cd-110">AzureCloud 和 AzureChinaCloud 的內建環境會鎖定現有的 Azure Resource Manager 公用實例。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="1c1cd-111">例子</span><span class="sxs-lookup"><span data-stu-id="1c1cd-111">EXAMPLES</span></span>

### <span data-ttu-id="1c1cd-112">範例 1：建立及修改新環境</span><span class="sxs-lookup"><span data-stu-id="1c1cd-112">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="1c1cd-113">在此範例中，我們將使用 Add-AzEnvironment 建立具有範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzEnvironment 變更所建立環境 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="1c1cd-114">範例 2：透過 Uri 探索新環境</span><span class="sxs-lookup"><span data-stu-id="1c1cd-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="1c1cd-115">在此範例中，我們將從 Uri 探索新的 `https://configuredmetadata.net` Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="1c1cd-116">參數</span><span class="sxs-lookup"><span data-stu-id="1c1cd-116">PARAMETERS</span></span>

### <span data-ttu-id="1c1cd-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="1c1cd-118">指定 Azure Active Directory 驗證的基本授權。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-120">指定向 AZURE Resource Manager 或 RDFE 端點的服務管理 (驗證) 物件。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="1c1cd-121">-AdTenant</span></span>
<span data-ttu-id="1c1cd-122">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-122">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-123">-ARMEndpoint</span></span>
<span data-ttu-id="1c1cd-124">Azure Resource Manager 端點</span><span class="sxs-lookup"><span data-stu-id="1c1cd-124">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-125">-自動探索</span><span class="sxs-lookup"><span data-stu-id="1c1cd-125">-AutoDiscover</span></span>
<span data-ttu-id="1c1cd-126">透過預設或已配置的端點探索環境。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-128">Azure Analysis Services 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="1c1cd-130">與 Azure Log Analytics API 通訊時使用的端點。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-132">這是所要求權杖收件者之 Azure 識別服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="1c1cd-134">Azure 認證服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="1c1cd-136">Azure Data Lake Analytics 工作與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="1c1cd-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="1c1cd-138">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="1c1cd-139">範例：azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="1c1cd-139">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="1c1cd-141">Azure Key Vault 服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="1c1cd-142">範例為vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="1c1cd-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-144">受要求權杖收件者的 Azure Key Vault 資料服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="1c1cd-146">與 Azure Log Analytics API 通訊時使用的端點。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-148">使用 Azure Log Analytics API 驗證權杖的物件。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-150">這是要求權杖收件者的 Azure Synapse Analytics 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="1c1cd-152">Azure Synapse Analytics 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1c1cd-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="1c1cd-154">受要求權杖收件者的 Azure Batch 服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1c1cd-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="1c1cd-156">Azure Container Registry 的尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-156">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="1c1cd-157">-DataLakeAudience</span></span>
<span data-ttu-id="1c1cd-158">使用 AD Data Lake 服務端點驗證權杖的物件。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1cd-159">-DefaultProfile</span></span>
<span data-ttu-id="1c1cd-160">用於與 Azure 通訊的認證、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1c1cd-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c1cd-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="1c1cd-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="1c1cd-162">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-163">-GalleryEndpoint</span></span>
<span data-ttu-id="1c1cd-164">指定部署範本 Azure Resource Manager 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="1c1cd-165">-GraphAudience</span></span>
<span data-ttu-id="1c1cd-166">使用 AD Graph 端點驗證權杖的觀眾。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-167">-GraphEndpoint</span></span>
<span data-ttu-id="1c1cd-168">指定 Graph 的 URL (Active Directory 中繼資料) 要求。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="1c1cd-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="1c1cd-170">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-170">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-171">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c1cd-171">-Name</span></span>
<span data-ttu-id="1c1cd-172">指定要新增的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-172">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="1c1cd-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="1c1cd-174">指定可從中下載 .publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="1c1cd-176">指定 Azure Resource Manager 要求 URL。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-176">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-177">-範圍</span><span class="sxs-lookup"><span data-stu-id="1c1cd-177">-Scope</span></span>
<span data-ttu-id="1c1cd-178">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-179">-ServiceEndpoint</span></span>
<span data-ttu-id="1c1cd-180">指定 RDFE (服務管理) 端點。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="1c1cd-182">指定 Azure SQL Database 伺服器的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c1cd-183">-StorageEndpoint</span></span>
<span data-ttu-id="1c1cd-184">指定儲存空間的端點 (Blob、資料表、佇列和檔案) 存取。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1c1cd-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="1c1cd-186">指定 Azure Traffic Manager 服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-187">-Uri</span><span class="sxs-lookup"><span data-stu-id="1c1cd-187">-Uri</span></span>
<span data-ttu-id="1c1cd-188">指定網際網路資源的 URI 以抓取環境。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-188">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-189">-確認</span><span class="sxs-lookup"><span data-stu-id="1c1cd-189">-Confirm</span></span>
<span data-ttu-id="1c1cd-190">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-190">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c1cd-191">-WhatIf</span></span>
<span data-ttu-id="1c1cd-192">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c1cd-193">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-193">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1cd-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1cd-194">CommonParameters</span></span>
<span data-ttu-id="1c1cd-195">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c1cd-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1cd-196">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c1cd-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1cd-197">輸入</span><span class="sxs-lookup"><span data-stu-id="1c1cd-197">INPUTS</span></span>

### <span data-ttu-id="1c1cd-198">System.String</span><span class="sxs-lookup"><span data-stu-id="1c1cd-198">System.String</span></span>

### <span data-ttu-id="1c1cd-199">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1c1cd-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1c1cd-200">輸出</span><span class="sxs-lookup"><span data-stu-id="1c1cd-200">OUTPUTS</span></span>

### <span data-ttu-id="1c1cd-201">Microsoft.Azure.Commands.Profile.models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c1cd-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="1c1cd-202">筆記</span><span class="sxs-lookup"><span data-stu-id="1c1cd-202">NOTES</span></span>

## <span data-ttu-id="1c1cd-203">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c1cd-203">RELATED LINKS</span></span>

[<span data-ttu-id="1c1cd-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c1cd-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="1c1cd-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c1cd-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="1c1cd-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="1c1cd-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

