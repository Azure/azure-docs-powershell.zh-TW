---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442483"
---
# <span data-ttu-id="1f26e-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f26e-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="1f26e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f26e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f26e-103">新增 Azure 資源管理員實例的端點和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="1f26e-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="1f26e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f26e-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f26e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f26e-105">DESCRIPTION</span></span>
<span data-ttu-id="1f26e-106">Add-AzureRmEnvironment Cmdlet 會新增端點和中繼資料，以啟用 Azure 資源管理器 Cmdlet 與新的 Azure 資源管理器實例連線。</span><span class="sxs-lookup"><span data-stu-id="1f26e-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="1f26e-107">內建的環境 AzureCloud 和 AzureChinaCloud 會以現有的 Azure 資源管理器公用實例為目標。</span><span class="sxs-lookup"><span data-stu-id="1f26e-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="1f26e-108">示例</span><span class="sxs-lookup"><span data-stu-id="1f26e-108">EXAMPLES</span></span>

### <span data-ttu-id="1f26e-109">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="1f26e-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="1f26e-110">在這個範例中，我們會使用 [載入 AzureRmEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzureRmEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1f26e-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="1f26e-111">參數</span><span class="sxs-lookup"><span data-stu-id="1f26e-111">PARAMETERS</span></span>

### <span data-ttu-id="1f26e-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f26e-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="1f26e-113">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="1f26e-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1f26e-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="1f26e-115">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="1f26e-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="1f26e-116">-AdTenant</span></span>
<span data-ttu-id="1f26e-117">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="1f26e-117">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1f26e-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="1f26e-119">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="1f26e-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1f26e-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="1f26e-121">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="1f26e-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="1f26e-122">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="1f26e-122">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1f26e-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="1f26e-124">指定主要保存庫服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1f26e-124">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="1f26e-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="1f26e-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="1f26e-126">指定授權金鑰保存庫服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="1f26e-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="1f26e-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="1f26e-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="1f26e-128">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="1f26e-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f26e-129">-GalleryEndpoint</span></span>
<span data-ttu-id="1f26e-130">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="1f26e-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="1f26e-131">-GraphAudience</span></span>
<span data-ttu-id="1f26e-132">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="1f26e-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f26e-133">-GraphEndpoint</span></span>
<span data-ttu-id="1f26e-134">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="1f26e-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="1f26e-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="1f26e-136">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="1f26e-136">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f26e-137">-Name</span></span>
<span data-ttu-id="1f26e-138">指定要新增之環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f26e-138">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="1f26e-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="1f26e-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="1f26e-140">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="1f26e-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f26e-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="1f26e-142">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="1f26e-142">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f26e-143">-ServiceEndpoint</span></span>
<span data-ttu-id="1f26e-144">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="1f26e-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1f26e-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="1f26e-146">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1f26e-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f26e-147">-StorageEndpoint</span></span>
<span data-ttu-id="1f26e-148">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="1f26e-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="1f26e-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="1f26e-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="1f26e-150">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="1f26e-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f26e-151">-確認</span><span class="sxs-lookup"><span data-stu-id="1f26e-151">-Confirm</span></span>
<span data-ttu-id="1f26e-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f26e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f26e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f26e-153">-WhatIf</span></span>
<span data-ttu-id="1f26e-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f26e-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f26e-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f26e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f26e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f26e-156">CommonParameters</span></span>
<span data-ttu-id="1f26e-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f26e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f26e-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f26e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f26e-159">輸入</span><span class="sxs-lookup"><span data-stu-id="1f26e-159">INPUTS</span></span>

## <span data-ttu-id="1f26e-160">輸出</span><span class="sxs-lookup"><span data-stu-id="1f26e-160">OUTPUTS</span></span>

### <span data-ttu-id="1f26e-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f26e-161">PSAzureEnvironment</span></span>
<span data-ttu-id="1f26e-162">這個 Cmdlet 會傳回與 Azure 實例通訊所需的端點和元資料集合。</span><span class="sxs-lookup"><span data-stu-id="1f26e-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="1f26e-163">筆記</span><span class="sxs-lookup"><span data-stu-id="1f26e-163">NOTES</span></span>

## <span data-ttu-id="1f26e-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f26e-164">RELATED LINKS</span></span>

[<span data-ttu-id="1f26e-165">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f26e-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="1f26e-166">移除-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f26e-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="1f26e-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="1f26e-167">Set-AzureRMEnvironment</span></span>]()

