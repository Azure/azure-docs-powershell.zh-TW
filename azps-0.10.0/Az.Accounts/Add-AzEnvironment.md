---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 69f8c633cc87cac5ff2c0dc3226a09bd24e2e94c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794071"
---
# <span data-ttu-id="449d5-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="449d5-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="449d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="449d5-102">SYNOPSIS</span></span>
<span data-ttu-id="449d5-103">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="449d5-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="449d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="449d5-104">SYNTAX</span></span>

### <span data-ttu-id="449d5-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="449d5-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449d5-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="449d5-107">說明</span><span class="sxs-lookup"><span data-stu-id="449d5-107">DESCRIPTION</span></span>
<span data-ttu-id="449d5-108">Add-AzEnvironment Cmdlet 會新增端點和中繼資料，以啟用 Azure 資源管理器 Cmdlet 與新的 Azure 資源管理器實例連線。</span><span class="sxs-lookup"><span data-stu-id="449d5-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="449d5-109">內建的環境 AzureCloud 和 AzureChinaCloud 會以現有的 Azure 資源管理器公用實例為目標。</span><span class="sxs-lookup"><span data-stu-id="449d5-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="449d5-110">示例</span><span class="sxs-lookup"><span data-stu-id="449d5-110">EXAMPLES</span></span>

### <span data-ttu-id="449d5-111">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="449d5-111">Example 1: Creating and modifying a new environment</span></span>
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="449d5-112">參數</span><span class="sxs-lookup"><span data-stu-id="449d5-112">PARAMETERS</span></span>

### <span data-ttu-id="449d5-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="449d5-114">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="449d5-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="449d5-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="449d5-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="449d5-116">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="449d5-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="449d5-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="449d5-117">-AdTenant</span></span>
<span data-ttu-id="449d5-118">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="449d5-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="449d5-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-119">-ARMEndpoint</span></span>
<span data-ttu-id="449d5-120">Azure 資源管理器端點</span><span class="sxs-lookup"><span data-stu-id="449d5-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="449d5-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="449d5-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="449d5-122">Azure Analysis Services 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="449d5-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="449d5-124">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="449d5-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="449d5-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="449d5-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="449d5-126">所要求權杖之收件者之 Azure 認證服務的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="449d5-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="449d5-128">Azure 認證服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="449d5-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="449d5-130">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="449d5-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="449d5-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="449d5-132">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="449d5-133">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="449d5-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="449d5-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="449d5-135">Azure 金鑰保存庫服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="449d5-136">範例是 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="449d5-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="449d5-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="449d5-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="449d5-138">Azure 金鑰保存庫資料服務的資源識別碼，是所要求權杖的收件者。</span><span class="sxs-lookup"><span data-stu-id="449d5-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="449d5-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="449d5-140">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="449d5-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="449d5-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="449d5-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="449d5-142">針對 Azure Log Analytics API 進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="449d5-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="449d5-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="449d5-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="449d5-144">作為所請求標記之收件者之 Azure Batch 服務的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="449d5-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="449d5-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="449d5-145">-DataLakeAudience</span></span>
<span data-ttu-id="449d5-146">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="449d5-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="449d5-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449d5-147">-DefaultProfile</span></span>
<span data-ttu-id="449d5-148">用於與 azure 進行通訊的認證、租使用者與訂閱</span><span class="sxs-lookup"><span data-stu-id="449d5-148">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="449d5-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="449d5-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="449d5-150">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="449d5-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="449d5-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-151">-GalleryEndpoint</span></span>
<span data-ttu-id="449d5-152">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="449d5-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="449d5-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="449d5-153">-GraphAudience</span></span>
<span data-ttu-id="449d5-154">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="449d5-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="449d5-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-155">-GraphEndpoint</span></span>
<span data-ttu-id="449d5-156">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="449d5-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="449d5-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="449d5-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="449d5-158">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="449d5-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="449d5-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="449d5-159">-Name</span></span>
<span data-ttu-id="449d5-160">指定要新增之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="449d5-160">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="449d5-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="449d5-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="449d5-162">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="449d5-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="449d5-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="449d5-164">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="449d5-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="449d5-165">-範圍</span><span class="sxs-lookup"><span data-stu-id="449d5-165">-Scope</span></span>
<span data-ttu-id="449d5-166">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="449d5-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="449d5-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-167">-ServiceEndpoint</span></span>
<span data-ttu-id="449d5-168">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="449d5-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="449d5-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="449d5-170">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="449d5-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="449d5-171">-StorageEndpoint</span></span>
<span data-ttu-id="449d5-172">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="449d5-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="449d5-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="449d5-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="449d5-174">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="449d5-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="449d5-175">-確認</span><span class="sxs-lookup"><span data-stu-id="449d5-175">-Confirm</span></span>
<span data-ttu-id="449d5-176">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="449d5-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="449d5-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="449d5-177">-WhatIf</span></span>
<span data-ttu-id="449d5-178">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="449d5-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="449d5-179">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="449d5-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="449d5-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449d5-180">CommonParameters</span></span>
<span data-ttu-id="449d5-181">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="449d5-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449d5-182">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="449d5-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449d5-183">輸入</span><span class="sxs-lookup"><span data-stu-id="449d5-183">INPUTS</span></span>

### <span data-ttu-id="449d5-184">System.object</span><span class="sxs-lookup"><span data-stu-id="449d5-184">System.String</span></span>

### <span data-ttu-id="449d5-185">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="449d5-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="449d5-186">輸出</span><span class="sxs-lookup"><span data-stu-id="449d5-186">OUTPUTS</span></span>

### <span data-ttu-id="449d5-187">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="449d5-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="449d5-188">筆記</span><span class="sxs-lookup"><span data-stu-id="449d5-188">NOTES</span></span>

## <span data-ttu-id="449d5-189">相關連結</span><span class="sxs-lookup"><span data-stu-id="449d5-189">RELATED LINKS</span></span>

[<span data-ttu-id="449d5-190">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="449d5-190">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="449d5-191">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="449d5-191">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="449d5-192">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="449d5-192">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

