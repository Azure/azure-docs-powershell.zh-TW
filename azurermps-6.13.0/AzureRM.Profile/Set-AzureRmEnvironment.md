---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 073126f3f750f2decf7189c53733c5fcaaabee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448276"
---
# <span data-ttu-id="b63ad-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b63ad-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="b63ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b63ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b63ad-103">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="b63ad-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b63ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="b63ad-104">SYNTAX</span></span>

### <span data-ttu-id="b63ad-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="b63ad-105">Name (Default)</span></span>
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
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureAnalysisServicesEndpointSuffix] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b63ad-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b63ad-107">說明</span><span class="sxs-lookup"><span data-stu-id="b63ad-107">DESCRIPTION</span></span>
<span data-ttu-id="b63ad-108">Set-AzureRMEnvironment Cmdlet 會設定端點和中繼資料以連接至 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="b63ad-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="b63ad-109">示例</span><span class="sxs-lookup"><span data-stu-id="b63ad-109">EXAMPLES</span></span>

### <span data-ttu-id="b63ad-110">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="b63ad-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
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
```

<span data-ttu-id="b63ad-111">在這個範例中，我們會使用 [載入 AzureRmEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzureRmEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b63ad-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="b63ad-112">參數</span><span class="sxs-lookup"><span data-stu-id="b63ad-112">PARAMETERS</span></span>

### <span data-ttu-id="b63ad-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="b63ad-114">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="b63ad-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="b63ad-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b63ad-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="b63ad-116">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="b63ad-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="b63ad-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="b63ad-117">-AdTenant</span></span>
<span data-ttu-id="b63ad-118">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="b63ad-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="b63ad-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-119">-ARMEndpoint</span></span>
<span data-ttu-id="b63ad-120">Azure 資源管理器端點。</span><span class="sxs-lookup"><span data-stu-id="b63ad-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="b63ad-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b63ad-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="b63ad-122">Azure Analysis Services 服務端點的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="b63ad-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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

### <span data-ttu-id="b63ad-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b63ad-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="b63ad-124">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="b63ad-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="b63ad-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b63ad-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="b63ad-126">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="b63ad-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="b63ad-127">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="b63ad-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="b63ad-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b63ad-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="b63ad-129">指定主要保存庫服務的功能變數名稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="b63ad-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="b63ad-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b63ad-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="b63ad-131">指定授權金鑰保存庫服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="b63ad-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="b63ad-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="b63ad-133">指定 Operational Insights 查詢存取的端點。</span><span class="sxs-lookup"><span data-stu-id="b63ad-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="b63ad-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b63ad-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="b63ad-135">指定授權使用 Operational Insights 服務要求的存取權杖物件。</span><span class="sxs-lookup"><span data-stu-id="b63ad-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="b63ad-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b63ad-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="b63ad-137">作為所請求標記之收件者之 Azure Batch 服務的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b63ad-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="b63ad-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="b63ad-138">-DataLakeAudience</span></span>
<span data-ttu-id="b63ad-139">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="b63ad-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="b63ad-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63ad-140">-DefaultProfile</span></span>
<span data-ttu-id="b63ad-141">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="b63ad-141">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b63ad-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="b63ad-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="b63ad-143">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="b63ad-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="b63ad-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-144">-GalleryEndpoint</span></span>
<span data-ttu-id="b63ad-145">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="b63ad-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="b63ad-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="b63ad-146">-GraphAudience</span></span>
<span data-ttu-id="b63ad-147">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="b63ad-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="b63ad-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-148">-GraphEndpoint</span></span>
<span data-ttu-id="b63ad-149">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="b63ad-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="b63ad-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="b63ad-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="b63ad-151">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="b63ad-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="b63ad-152">-名稱</span><span class="sxs-lookup"><span data-stu-id="b63ad-152">-Name</span></span>
<span data-ttu-id="b63ad-153">指定要修改的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="b63ad-153">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="b63ad-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="b63ad-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="b63ad-155">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="b63ad-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="b63ad-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="b63ad-157">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="b63ad-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="b63ad-158">-範圍</span><span class="sxs-lookup"><span data-stu-id="b63ad-158">-Scope</span></span>
<span data-ttu-id="b63ad-159">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="b63ad-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b63ad-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-160">-ServiceEndpoint</span></span>
<span data-ttu-id="b63ad-161">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="b63ad-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="b63ad-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b63ad-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="b63ad-163">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="b63ad-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="b63ad-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="b63ad-164">-StorageEndpoint</span></span>
<span data-ttu-id="b63ad-165">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="b63ad-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="b63ad-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b63ad-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="b63ad-167">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="b63ad-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="b63ad-168">-確認</span><span class="sxs-lookup"><span data-stu-id="b63ad-168">-Confirm</span></span>
<span data-ttu-id="b63ad-169">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b63ad-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b63ad-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b63ad-170">-WhatIf</span></span>
<span data-ttu-id="b63ad-171">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b63ad-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b63ad-172">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b63ad-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b63ad-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63ad-173">CommonParameters</span></span>
<span data-ttu-id="b63ad-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b63ad-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63ad-175">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b63ad-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63ad-176">輸入</span><span class="sxs-lookup"><span data-stu-id="b63ad-176">INPUTS</span></span>

### <span data-ttu-id="b63ad-177">System.object</span><span class="sxs-lookup"><span data-stu-id="b63ad-177">System.String</span></span>

### <span data-ttu-id="b63ad-178">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b63ad-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b63ad-179">輸出</span><span class="sxs-lookup"><span data-stu-id="b63ad-179">OUTPUTS</span></span>

### <span data-ttu-id="b63ad-180">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b63ad-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="b63ad-181">筆記</span><span class="sxs-lookup"><span data-stu-id="b63ad-181">NOTES</span></span>

## <span data-ttu-id="b63ad-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="b63ad-182">RELATED LINKS</span></span>

[<span data-ttu-id="b63ad-183">附加 AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b63ad-183">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="b63ad-184">AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b63ad-184">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="b63ad-185">移除-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b63ad-185">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

