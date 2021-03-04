---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905701"
---
# <span data-ttu-id="674bf-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="674bf-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="674bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="674bf-102">SYNOPSIS</span></span>
<span data-ttu-id="674bf-103">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="674bf-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="674bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="674bf-104">SYNTAX</span></span>

### <span data-ttu-id="674bf-105">名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="674bf-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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

### <span data-ttu-id="674bf-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="674bf-107">描述</span><span class="sxs-lookup"><span data-stu-id="674bf-107">DESCRIPTION</span></span>
<span data-ttu-id="674bf-108">此Set-AzEnvironment Cmdlet 會設定端點和中繼資料，以連接至 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="674bf-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="674bf-109">例子</span><span class="sxs-lookup"><span data-stu-id="674bf-109">EXAMPLES</span></span>

### <span data-ttu-id="674bf-110">範例 1：建立及修改新環境</span><span class="sxs-lookup"><span data-stu-id="674bf-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="674bf-111">在此範例中，我們將使用 Add-AzEnvironment 建立具有範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzEnvironment 變更所建立環境 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="674bf-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="674bf-112">參數</span><span class="sxs-lookup"><span data-stu-id="674bf-112">PARAMETERS</span></span>

### <span data-ttu-id="674bf-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="674bf-114">指定 Azure Active Directory 驗證的基本授權。</span><span class="sxs-lookup"><span data-stu-id="674bf-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="674bf-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="674bf-116">指定向 AZURE Resource Manager 或 RDFE 端點的服務管理 (驗證) 物件。</span><span class="sxs-lookup"><span data-stu-id="674bf-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="674bf-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="674bf-117">-AdTenant</span></span>
<span data-ttu-id="674bf-118">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="674bf-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="674bf-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-119">-ARMEndpoint</span></span>
<span data-ttu-id="674bf-120">Azure Resource Manager 端點。</span><span class="sxs-lookup"><span data-stu-id="674bf-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="674bf-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="674bf-122">Azure Analysis Services 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="674bf-124">與 Azure Log Analytics API 通訊時使用的端點。</span><span class="sxs-lookup"><span data-stu-id="674bf-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="674bf-126">這是所要求權杖收件者之 Azure 識別服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="674bf-128">Azure 認證服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="674bf-130">Azure Data Lake Analytics 工作與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="674bf-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="674bf-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="674bf-132">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="674bf-133">範例：azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="674bf-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="674bf-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="674bf-135">Azure Key Vault 服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="674bf-136">範例為vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="674bf-136">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="674bf-138">受要求權杖收件者的 Azure Key Vault 資料服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="674bf-140">與 Azure Log Analytics API 通訊時使用的端點。</span><span class="sxs-lookup"><span data-stu-id="674bf-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="674bf-142">使用 Azure Log Analytics API 驗證權杖的物件。</span><span class="sxs-lookup"><span data-stu-id="674bf-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="674bf-144">這是要求權杖收件者的 Azure Synapse Analytics 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="674bf-146">Azure Synapse Analytics 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="674bf-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="674bf-148">受要求權杖收件者的 Azure Batch 服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="674bf-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="674bf-150">Azure Container Registry 的尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-150">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="674bf-151">-DataLakeAudience</span></span>
<span data-ttu-id="674bf-152">使用 AD Data Lake 服務端點驗證權杖的物件。</span><span class="sxs-lookup"><span data-stu-id="674bf-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="674bf-153">-DefaultProfile</span></span>
<span data-ttu-id="674bf-154">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="674bf-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="674bf-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="674bf-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="674bf-156">表示已允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="674bf-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="674bf-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-157">-GalleryEndpoint</span></span>
<span data-ttu-id="674bf-158">指定部署範本 Azure Resource Manager 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="674bf-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="674bf-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="674bf-159">-GraphAudience</span></span>
<span data-ttu-id="674bf-160">使用 AD Graph 端點驗證權杖的觀眾。</span><span class="sxs-lookup"><span data-stu-id="674bf-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="674bf-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-161">-GraphEndpoint</span></span>
<span data-ttu-id="674bf-162">指定 Graph 的 URL (Active Directory 中繼資料) 要求。</span><span class="sxs-lookup"><span data-stu-id="674bf-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="674bf-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="674bf-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="674bf-164">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="674bf-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="674bf-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="674bf-165">-Name</span></span>
<span data-ttu-id="674bf-166">指定要修改的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="674bf-166">Specifies the name of the environment to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="674bf-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="674bf-168">指定可從中下載 .publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="674bf-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="674bf-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="674bf-170">指定 Azure Resource Manager 要求 URL。</span><span class="sxs-lookup"><span data-stu-id="674bf-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="674bf-171">-範圍</span><span class="sxs-lookup"><span data-stu-id="674bf-171">-Scope</span></span>
<span data-ttu-id="674bf-172">決定上下文變更的範圍，例如，變更是否僅適用于目前的程式，或適用于此使用者啟動的所有會話。</span><span class="sxs-lookup"><span data-stu-id="674bf-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="674bf-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-173">-ServiceEndpoint</span></span>
<span data-ttu-id="674bf-174">指定 RDFE 要求 (服務管理) 端點。</span><span class="sxs-lookup"><span data-stu-id="674bf-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="674bf-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="674bf-176">指定 Azure SQL Database 伺服器的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="674bf-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="674bf-177">-StorageEndpoint</span></span>
<span data-ttu-id="674bf-178">指定儲存空間的端點 (Blob、資料表、佇列和檔案) 存取。</span><span class="sxs-lookup"><span data-stu-id="674bf-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="674bf-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="674bf-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="674bf-180">指定 Azure Traffic Manager 服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="674bf-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="674bf-181">-確認</span><span class="sxs-lookup"><span data-stu-id="674bf-181">-Confirm</span></span>
<span data-ttu-id="674bf-182">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="674bf-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="674bf-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="674bf-183">-WhatIf</span></span>
<span data-ttu-id="674bf-184">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="674bf-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="674bf-185">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="674bf-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="674bf-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="674bf-186">CommonParameters</span></span>
<span data-ttu-id="674bf-187">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="674bf-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="674bf-188">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="674bf-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="674bf-189">輸入</span><span class="sxs-lookup"><span data-stu-id="674bf-189">INPUTS</span></span>

### <span data-ttu-id="674bf-190">System.String</span><span class="sxs-lookup"><span data-stu-id="674bf-190">System.String</span></span>

### <span data-ttu-id="674bf-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="674bf-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="674bf-192">輸出</span><span class="sxs-lookup"><span data-stu-id="674bf-192">OUTPUTS</span></span>

### <span data-ttu-id="674bf-193">Microsoft.Azure.Commands.Profile.models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="674bf-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="674bf-194">筆記</span><span class="sxs-lookup"><span data-stu-id="674bf-194">NOTES</span></span>

## <span data-ttu-id="674bf-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="674bf-195">RELATED LINKS</span></span>

[<span data-ttu-id="674bf-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="674bf-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="674bf-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="674bf-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="674bf-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="674bf-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

