---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 47f57068af722bd9f34826176d2a31cdfd9843a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611765"
---
# <span data-ttu-id="4d613-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d613-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="4d613-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d613-102">SYNOPSIS</span></span>
<span data-ttu-id="4d613-103">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4d613-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="4d613-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d613-104">SYNTAX</span></span>

### <span data-ttu-id="4d613-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="4d613-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d613-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d613-107">說明</span><span class="sxs-lookup"><span data-stu-id="4d613-107">DESCRIPTION</span></span>
<span data-ttu-id="4d613-108">Add-AzEnvironment Cmdlet 會新增端點和中繼資料，以啟用 Azure 資源管理器 Cmdlet 與新的 Azure 資源管理器實例連線。</span><span class="sxs-lookup"><span data-stu-id="4d613-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="4d613-109">內建的環境 AzureCloud 和 AzureChinaCloud 會以現有的 Azure 資源管理器公用實例為目標。</span><span class="sxs-lookup"><span data-stu-id="4d613-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="4d613-110">示例</span><span class="sxs-lookup"><span data-stu-id="4d613-110">EXAMPLES</span></span>

### <span data-ttu-id="4d613-111">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="4d613-111">Example 1: Creating and modifying a new environment</span></span>
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="4d613-112">參數</span><span class="sxs-lookup"><span data-stu-id="4d613-112">PARAMETERS</span></span>

### <span data-ttu-id="4d613-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4d613-114">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="4d613-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="4d613-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d613-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4d613-116">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="4d613-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="4d613-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="4d613-117">-AdTenant</span></span>
<span data-ttu-id="4d613-118">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="4d613-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="4d613-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-119">-ARMEndpoint</span></span>
<span data-ttu-id="4d613-120">Azure 資源管理器端點</span><span class="sxs-lookup"><span data-stu-id="4d613-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="4d613-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d613-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="4d613-122">Azure Analysis Services 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d613-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="4d613-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d613-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="4d613-124">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="4d613-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4d613-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d613-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="4d613-126">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="4d613-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="4d613-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4d613-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="4d613-128">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="4d613-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="4d613-129">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="4d613-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="4d613-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4d613-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="4d613-131">Azure 金鑰保存庫服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="4d613-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="4d613-132">範例是 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="4d613-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="4d613-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d613-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="4d613-134">Azure 金鑰保存庫資料服務的資源識別碼，是所要求權杖的收件者。</span><span class="sxs-lookup"><span data-stu-id="4d613-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4d613-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="4d613-136">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="4d613-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4d613-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d613-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="4d613-138">針對 Azure Log Analytics API 進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="4d613-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4d613-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4d613-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="4d613-140">作為所請求標記之收件者之 Azure Batch 服務的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4d613-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="4d613-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="4d613-141">-DataLakeAudience</span></span>
<span data-ttu-id="4d613-142">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="4d613-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="4d613-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d613-143">-DefaultProfile</span></span>
<span data-ttu-id="4d613-144">用於與 azure 進行通訊的 credeetnails、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4d613-144">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d613-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4d613-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="4d613-146">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="4d613-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="4d613-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-147">-GalleryEndpoint</span></span>
<span data-ttu-id="4d613-148">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="4d613-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="4d613-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="4d613-149">-GraphAudience</span></span>
<span data-ttu-id="4d613-150">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="4d613-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="4d613-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-151">-GraphEndpoint</span></span>
<span data-ttu-id="4d613-152">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="4d613-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="4d613-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="4d613-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="4d613-154">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="4d613-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="4d613-155">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d613-155">-Name</span></span>
<span data-ttu-id="4d613-156">指定要新增之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d613-156">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="4d613-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4d613-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4d613-158">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="4d613-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="4d613-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4d613-160">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="4d613-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="4d613-161">-範圍</span><span class="sxs-lookup"><span data-stu-id="4d613-161">-Scope</span></span>
<span data-ttu-id="4d613-162">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="4d613-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4d613-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-163">-ServiceEndpoint</span></span>
<span data-ttu-id="4d613-164">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="4d613-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="4d613-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4d613-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="4d613-166">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="4d613-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="4d613-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d613-167">-StorageEndpoint</span></span>
<span data-ttu-id="4d613-168">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="4d613-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="4d613-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4d613-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="4d613-170">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="4d613-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="4d613-171">-確認</span><span class="sxs-lookup"><span data-stu-id="4d613-171">-Confirm</span></span>
<span data-ttu-id="4d613-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d613-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d613-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d613-173">-WhatIf</span></span>
<span data-ttu-id="4d613-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d613-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d613-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d613-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d613-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d613-176">CommonParameters</span></span>
<span data-ttu-id="4d613-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d613-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d613-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d613-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d613-179">輸入</span><span class="sxs-lookup"><span data-stu-id="4d613-179">INPUTS</span></span>

### <span data-ttu-id="4d613-180">System.object</span><span class="sxs-lookup"><span data-stu-id="4d613-180">System.String</span></span>

### <span data-ttu-id="4d613-181">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4d613-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d613-182">輸出</span><span class="sxs-lookup"><span data-stu-id="4d613-182">OUTPUTS</span></span>

### <span data-ttu-id="4d613-183">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d613-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="4d613-184">筆記</span><span class="sxs-lookup"><span data-stu-id="4d613-184">NOTES</span></span>

## <span data-ttu-id="4d613-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d613-185">RELATED LINKS</span></span>

[<span data-ttu-id="4d613-186">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d613-186">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="4d613-187">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d613-187">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="4d613-188">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4d613-188">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

