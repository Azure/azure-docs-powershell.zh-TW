---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442591"
---
# <span data-ttu-id="f66aa-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f66aa-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="f66aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f66aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f66aa-103">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="f66aa-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="f66aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="f66aa-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f66aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="f66aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f66aa-106">Set-AzureRMEnvironment Cmdlet 會設定端點和中繼資料以連接至 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="f66aa-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="f66aa-107">示例</span><span class="sxs-lookup"><span data-stu-id="f66aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f66aa-108">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="f66aa-108">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="f66aa-109">在這個範例中，我們會使用 [載入 AzureRmEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzureRmEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="f66aa-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="f66aa-110">參數</span><span class="sxs-lookup"><span data-stu-id="f66aa-110">PARAMETERS</span></span>

### <span data-ttu-id="f66aa-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f66aa-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f66aa-112">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="f66aa-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f66aa-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f66aa-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f66aa-114">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="f66aa-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f66aa-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f66aa-115">-AdTenant</span></span>
<span data-ttu-id="f66aa-116">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="f66aa-116">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f66aa-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f66aa-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f66aa-118">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="f66aa-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f66aa-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f66aa-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f66aa-120">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="f66aa-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="f66aa-121">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f66aa-121">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f66aa-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f66aa-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f66aa-123">指定主要保存庫服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="f66aa-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="f66aa-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f66aa-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f66aa-125">指定授權金鑰保存庫服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="f66aa-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="f66aa-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f66aa-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f66aa-127">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="f66aa-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f66aa-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f66aa-128">-GalleryEndpoint</span></span>
<span data-ttu-id="f66aa-129">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="f66aa-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f66aa-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f66aa-130">-GraphAudience</span></span>
<span data-ttu-id="f66aa-131">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="f66aa-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f66aa-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f66aa-132">-GraphEndpoint</span></span>
<span data-ttu-id="f66aa-133">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="f66aa-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f66aa-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f66aa-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="f66aa-135">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="f66aa-135">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f66aa-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="f66aa-136">-Name</span></span>
<span data-ttu-id="f66aa-137">指定要修改的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="f66aa-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="f66aa-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f66aa-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f66aa-139">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="f66aa-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f66aa-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f66aa-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f66aa-141">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="f66aa-141">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f66aa-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f66aa-142">-ServiceEndpoint</span></span>
<span data-ttu-id="f66aa-143">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="f66aa-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f66aa-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f66aa-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f66aa-145">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="f66aa-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f66aa-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f66aa-146">-StorageEndpoint</span></span>
<span data-ttu-id="f66aa-147">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="f66aa-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f66aa-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f66aa-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f66aa-149">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="f66aa-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f66aa-150">-確認</span><span class="sxs-lookup"><span data-stu-id="f66aa-150">-Confirm</span></span>
<span data-ttu-id="f66aa-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f66aa-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f66aa-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f66aa-152">-WhatIf</span></span>
<span data-ttu-id="f66aa-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f66aa-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f66aa-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f66aa-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f66aa-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66aa-155">CommonParameters</span></span>
<span data-ttu-id="f66aa-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f66aa-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66aa-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f66aa-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66aa-158">輸入</span><span class="sxs-lookup"><span data-stu-id="f66aa-158">INPUTS</span></span>

## <span data-ttu-id="f66aa-159">輸出</span><span class="sxs-lookup"><span data-stu-id="f66aa-159">OUTPUTS</span></span>

### <span data-ttu-id="f66aa-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f66aa-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="f66aa-161">筆記</span><span class="sxs-lookup"><span data-stu-id="f66aa-161">NOTES</span></span>

## <span data-ttu-id="f66aa-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="f66aa-162">RELATED LINKS</span></span>

[<span data-ttu-id="f66aa-163">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f66aa-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="f66aa-164">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f66aa-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="f66aa-165">移除-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f66aa-165">Remove-AzureRMEnvironment</span></span>]()

