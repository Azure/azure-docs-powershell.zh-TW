---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: c39b61ab51296231b0952d1f12bd18e6d3aa13d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456455"
---
# <span data-ttu-id="dcfc5-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcfc5-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="dcfc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcfc5-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfc5-103">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcfc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcfc5-104">SYNTAX</span></span>

### <span data-ttu-id="dcfc5-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="dcfc5-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dcfc5-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcfc5-107">說明</span><span class="sxs-lookup"><span data-stu-id="dcfc5-107">DESCRIPTION</span></span>
<span data-ttu-id="dcfc5-108">Set-AzureRMEnvironment Cmdlet 會設定端點和中繼資料以連接至 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="dcfc5-109">示例</span><span class="sxs-lookup"><span data-stu-id="dcfc5-109">EXAMPLES</span></span>

### <span data-ttu-id="dcfc5-110">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="dcfc5-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="dcfc5-111">在這個範例中，我們會使用 [載入 AzureRmEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzureRmEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="dcfc5-112">參數</span><span class="sxs-lookup"><span data-stu-id="dcfc5-112">PARAMETERS</span></span>

### <span data-ttu-id="dcfc5-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="dcfc5-114">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="dcfc5-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcfc5-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="dcfc5-116">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="dcfc5-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="dcfc5-117">-AdTenant</span></span>
<span data-ttu-id="dcfc5-118">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="dcfc5-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-119">-ARMEndpoint</span></span>
<span data-ttu-id="dcfc5-120">Azure 資源管理器端點。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="dcfc5-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcfc5-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="dcfc5-122">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="dcfc5-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="dcfc5-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcfc5-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="dcfc5-124">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="dcfc5-125">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="dcfc5-125">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="dcfc5-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="dcfc5-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="dcfc5-127">指定主要保存庫服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-127">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="dcfc5-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcfc5-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="dcfc5-129">指定授權金鑰保存庫服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcfc5-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="dcfc5-130">-DataLakeAudience</span></span>
<span data-ttu-id="dcfc5-131">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="dcfc5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfc5-132">-DefaultProfile</span></span>
<span data-ttu-id="dcfc5-133">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcfc5-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="dcfc5-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="dcfc5-135">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="dcfc5-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-136">-GalleryEndpoint</span></span>
<span data-ttu-id="dcfc5-137">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="dcfc5-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="dcfc5-138">-GraphAudience</span></span>
<span data-ttu-id="dcfc5-139">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="dcfc5-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-140">-GraphEndpoint</span></span>
<span data-ttu-id="dcfc5-141">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="dcfc5-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="dcfc5-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="dcfc5-143">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-143">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="dcfc5-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="dcfc5-144">-Name</span></span>
<span data-ttu-id="dcfc5-145">指定要修改的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-145">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="dcfc5-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="dcfc5-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="dcfc5-147">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="dcfc5-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="dcfc5-149">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-149">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="dcfc5-150">-範圍</span><span class="sxs-lookup"><span data-stu-id="dcfc5-150">-Scope</span></span>
<span data-ttu-id="dcfc5-151">決定內容變更的範圍，例如，wheher 變更只適用于 cusrrent 進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-151">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="dcfc5-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-152">-ServiceEndpoint</span></span>
<span data-ttu-id="dcfc5-153">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="dcfc5-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="dcfc5-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="dcfc5-155">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="dcfc5-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcfc5-156">-StorageEndpoint</span></span>
<span data-ttu-id="dcfc5-157">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="dcfc5-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="dcfc5-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="dcfc5-159">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="dcfc5-160">-確認</span><span class="sxs-lookup"><span data-stu-id="dcfc5-160">-Confirm</span></span>
<span data-ttu-id="dcfc5-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcfc5-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcfc5-162">-WhatIf</span></span>
<span data-ttu-id="dcfc5-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcfc5-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcfc5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfc5-165">CommonParameters</span></span>
<span data-ttu-id="dcfc5-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfc5-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dcfc5-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfc5-168">輸入</span><span class="sxs-lookup"><span data-stu-id="dcfc5-168">INPUTS</span></span>

## <span data-ttu-id="dcfc5-169">輸出</span><span class="sxs-lookup"><span data-stu-id="dcfc5-169">OUTPUTS</span></span>

### <span data-ttu-id="dcfc5-170">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcfc5-170">PSAzureEnvironment</span></span>

## <span data-ttu-id="dcfc5-171">筆記</span><span class="sxs-lookup"><span data-stu-id="dcfc5-171">NOTES</span></span>

## <span data-ttu-id="dcfc5-172">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcfc5-172">RELATED LINKS</span></span>

[<span data-ttu-id="dcfc5-173">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcfc5-173">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="dcfc5-174">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcfc5-174">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="dcfc5-175">移除-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="dcfc5-175">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

