---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ef4f5128e92a319cb2b8ca021fc9b86f484d9b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623461"
---
# <span data-ttu-id="859ef-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="859ef-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="859ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="859ef-102">SYNOPSIS</span></span>
<span data-ttu-id="859ef-103">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="859ef-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="859ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="859ef-104">SYNTAX</span></span>

### <span data-ttu-id="859ef-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="859ef-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859ef-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859ef-107">說明</span><span class="sxs-lookup"><span data-stu-id="859ef-107">DESCRIPTION</span></span>
<span data-ttu-id="859ef-108">Add-AzureRmEnvironment Cmdlet 會新增端點和中繼資料，以啟用 Azure 資源管理器 Cmdlet 與新的 Azure 資源管理器實例連線。</span><span class="sxs-lookup"><span data-stu-id="859ef-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="859ef-109">內建的環境 AzureCloud 和 AzureChinaCloud 會以現有的 Azure 資源管理器公用實例為目標。</span><span class="sxs-lookup"><span data-stu-id="859ef-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="859ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="859ef-110">EXAMPLES</span></span>

### <span data-ttu-id="859ef-111">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="859ef-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

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
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

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
```

<span data-ttu-id="859ef-112">在這個範例中，我們會使用 [載入 AzureRmEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzureRmEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="859ef-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="859ef-113">參數</span><span class="sxs-lookup"><span data-stu-id="859ef-113">PARAMETERS</span></span>

### <span data-ttu-id="859ef-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="859ef-115">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="859ef-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="859ef-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="859ef-117">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="859ef-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="859ef-118">-AdTenant</span></span>
<span data-ttu-id="859ef-119">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="859ef-119">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-120">-ARMEndpoint</span></span>
<span data-ttu-id="859ef-121">Azure 資源管理器端點</span><span class="sxs-lookup"><span data-stu-id="859ef-121">The Azure Resource Manager endpoint</span></span>

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="859ef-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="859ef-123">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="859ef-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="859ef-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="859ef-125">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="859ef-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="859ef-126">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="859ef-126">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="859ef-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="859ef-128">指定主要保存庫服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="859ef-128">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="859ef-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="859ef-130">指定授權金鑰保存庫服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="859ef-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="859ef-131">-DataLakeAudience</span></span>
<span data-ttu-id="859ef-132">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="859ef-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859ef-133">-DefaultProfile</span></span>
<span data-ttu-id="859ef-134">用於與 azure 進行通訊的 credeetnails、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="859ef-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="859ef-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="859ef-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="859ef-136">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="859ef-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-137">-GalleryEndpoint</span></span>
<span data-ttu-id="859ef-138">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="859ef-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="859ef-139">-GraphAudience</span></span>
<span data-ttu-id="859ef-140">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="859ef-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-141">-GraphEndpoint</span></span>
<span data-ttu-id="859ef-142">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="859ef-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="859ef-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="859ef-144">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="859ef-144">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="859ef-145">-Name</span></span>
<span data-ttu-id="859ef-146">指定要新增之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="859ef-146">Specifies the name of the environment to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="859ef-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="859ef-148">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="859ef-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="859ef-150">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="859ef-150">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-151">-範圍</span><span class="sxs-lookup"><span data-stu-id="859ef-151">-Scope</span></span>
<span data-ttu-id="859ef-152">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="859ef-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-153">-ServiceEndpoint</span></span>
<span data-ttu-id="859ef-154">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="859ef-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="859ef-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="859ef-156">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="859ef-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-157">-StorageEndpoint</span></span>
<span data-ttu-id="859ef-158">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="859ef-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="859ef-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="859ef-160">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="859ef-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-161">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="859ef-161">-BatchEndpointResourceId</span></span>
<span data-ttu-id="859ef-162">作為所請求標記之收件者之 Azure Batch 服務的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="859ef-162">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-163">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="859ef-163">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="859ef-164">指定 Operational Insights 查詢存取的端點。</span><span class="sxs-lookup"><span data-stu-id="859ef-164">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-165">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="859ef-165">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="859ef-166">指定授權使用 Operational Insights 服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="859ef-166">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-167">-確認</span><span class="sxs-lookup"><span data-stu-id="859ef-167">-Confirm</span></span>
<span data-ttu-id="859ef-168">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="859ef-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859ef-169">-WhatIf</span></span>
<span data-ttu-id="859ef-170">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="859ef-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="859ef-171">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="859ef-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859ef-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859ef-172">CommonParameters</span></span>
<span data-ttu-id="859ef-173">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="859ef-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859ef-174">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="859ef-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859ef-175">輸入</span><span class="sxs-lookup"><span data-stu-id="859ef-175">INPUTS</span></span>

### <span data-ttu-id="859ef-176">所有</span><span class="sxs-lookup"><span data-stu-id="859ef-176">None</span></span>
<span data-ttu-id="859ef-177">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="859ef-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="859ef-178">輸出</span><span class="sxs-lookup"><span data-stu-id="859ef-178">OUTPUTS</span></span>

### <span data-ttu-id="859ef-179">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="859ef-179">PSAzureEnvironment</span></span>
<span data-ttu-id="859ef-180">這個 Cmdlet 會傳回與 Azure 實例通訊所需的端點和元資料集合。</span><span class="sxs-lookup"><span data-stu-id="859ef-180">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="859ef-181">筆記</span><span class="sxs-lookup"><span data-stu-id="859ef-181">NOTES</span></span>

## <span data-ttu-id="859ef-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="859ef-182">RELATED LINKS</span></span>

[<span data-ttu-id="859ef-183">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="859ef-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="859ef-184">移除-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="859ef-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="859ef-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="859ef-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

