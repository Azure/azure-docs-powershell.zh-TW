---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611708"
---
# <span data-ttu-id="d9d5f-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9d5f-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="d9d5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d5f-103">設定 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="d9d5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9d5f-104">SYNTAX</span></span>

### <span data-ttu-id="d9d5f-105">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="d9d5f-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9d5f-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d5f-107">說明</span><span class="sxs-lookup"><span data-stu-id="d9d5f-107">DESCRIPTION</span></span>
<span data-ttu-id="d9d5f-108">Set-AzEnvironment Cmdlet 會設定端點和中繼資料以連接至 Azure 實例。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="d9d5f-109">示例</span><span class="sxs-lookup"><span data-stu-id="d9d5f-109">EXAMPLES</span></span>

### <span data-ttu-id="d9d5f-110">範例1：建立及修改新的環境</span><span class="sxs-lookup"><span data-stu-id="d9d5f-110">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="d9d5f-111">在這個範例中，我們會使用 [載入 AzEnvironment] 來建立含範例端點的新 Azure 環境，然後使用 Cmdlet Set-AzEnvironment 變更已建立之環境的 ActiveDirectoryEndpoint 和 GraphEndpoint 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="d9d5f-112">參數</span><span class="sxs-lookup"><span data-stu-id="d9d5f-112">PARAMETERS</span></span>

### <span data-ttu-id="d9d5f-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="d9d5f-114">指定 Azure Active Directory 驗證的基本機構。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="d9d5f-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9d5f-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="d9d5f-116">針對將要求傳送到 Azure 資源管理器或服務管理 (RDFE) 端點的標記指定物件。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="d9d5f-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="d9d5f-117">-AdTenant</span></span>
<span data-ttu-id="d9d5f-118">指定預設的 Active Directory 租使用者。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="d9d5f-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-119">-ARMEndpoint</span></span>
<span data-ttu-id="d9d5f-120">Azure 資源管理器端點。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="d9d5f-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9d5f-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="d9d5f-122">Azure Analysis Services 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="d9d5f-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9d5f-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="d9d5f-124">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="d9d5f-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9d5f-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="d9d5f-126">Azure Data Lake Analytics 作業與目錄服務的 Dns 尾碼</span><span class="sxs-lookup"><span data-stu-id="d9d5f-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="d9d5f-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d9d5f-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="d9d5f-128">Azure Data Lake Store FileSystem 的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="d9d5f-129">範例： azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="d9d5f-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="d9d5f-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d9d5f-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="d9d5f-131">Azure 金鑰保存庫服務的 Dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="d9d5f-132">範例是 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="d9d5f-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="d9d5f-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9d5f-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="d9d5f-134">Azure 金鑰保存庫資料服務的資源識別碼，是所要求權杖的收件者。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="d9d5f-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="d9d5f-136">與 Azure Log Analytics API 進行通訊時要使用的端點。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="d9d5f-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9d5f-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="d9d5f-138">針對 Azure Log Analytics API 進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="d9d5f-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d9d5f-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="d9d5f-140">作為所請求標記之收件者之 Azure Batch 服務的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d9d5f-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="d9d5f-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="d9d5f-141">-DataLakeAudience</span></span>
<span data-ttu-id="d9d5f-142">針對 AD Data Lake services 端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="d9d5f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d5f-143">-DefaultProfile</span></span>
<span data-ttu-id="d9d5f-144">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9d5f-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9d5f-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="d9d5f-146">表示允許 Active Directory Federation Services (ADFS) 內部部署驗證。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="d9d5f-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-147">-GalleryEndpoint</span></span>
<span data-ttu-id="d9d5f-148">指定 [部署範本] 的 [Azure 資源管理器] 圖庫的端點。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="d9d5f-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="d9d5f-149">-GraphAudience</span></span>
<span data-ttu-id="d9d5f-150">使用廣告圖端點進行驗證的標記物件。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="d9d5f-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-151">-GraphEndpoint</span></span>
<span data-ttu-id="d9d5f-152">指定 (Active Directory 中繼資料) 要求的圖形 URL。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="d9d5f-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="d9d5f-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="d9d5f-154">指定管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="d9d5f-155">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9d5f-155">-Name</span></span>
<span data-ttu-id="d9d5f-156">指定要修改的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="d9d5f-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="d9d5f-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="d9d5f-158">指定可從中下載 publishsettings 檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="d9d5f-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="d9d5f-160">指定 Azure 資源管理員要求的 URL。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="d9d5f-161">-範圍</span><span class="sxs-lookup"><span data-stu-id="d9d5f-161">-Scope</span></span>
<span data-ttu-id="d9d5f-162">決定內容變更的範圍，例如，變更只適用于目前的進程，或只適用于此使用者開始的所有會話。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d9d5f-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-163">-ServiceEndpoint</span></span>
<span data-ttu-id="d9d5f-164">指定服務管理 (RDFE) 要求的端點。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="d9d5f-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d9d5f-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="d9d5f-166">指定 Azure SQL 資料庫伺服器的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="d9d5f-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="d9d5f-167">-StorageEndpoint</span></span>
<span data-ttu-id="d9d5f-168">指定儲存 (blob、資料表、佇列及檔案) 存取的端點。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="d9d5f-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d9d5f-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="d9d5f-170">指定 Azure 流量管理器服務的網功能變數名稱稱尾碼。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="d9d5f-171">-確認</span><span class="sxs-lookup"><span data-stu-id="d9d5f-171">-Confirm</span></span>
<span data-ttu-id="d9d5f-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d5f-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d5f-173">-WhatIf</span></span>
<span data-ttu-id="d9d5f-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9d5f-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d5f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d5f-176">CommonParameters</span></span>
<span data-ttu-id="d9d5f-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d5f-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d5f-179">輸入</span><span class="sxs-lookup"><span data-stu-id="d9d5f-179">INPUTS</span></span>

### <span data-ttu-id="d9d5f-180">System.object</span><span class="sxs-lookup"><span data-stu-id="d9d5f-180">System.String</span></span>

### <span data-ttu-id="d9d5f-181">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d9d5f-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9d5f-182">輸出</span><span class="sxs-lookup"><span data-stu-id="d9d5f-182">OUTPUTS</span></span>

### <span data-ttu-id="d9d5f-183">PSAzureEnvironment 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="d9d5f-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="d9d5f-184">筆記</span><span class="sxs-lookup"><span data-stu-id="d9d5f-184">NOTES</span></span>

## <span data-ttu-id="d9d5f-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9d5f-185">RELATED LINKS</span></span>

[<span data-ttu-id="d9d5f-186">附加 AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9d5f-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="d9d5f-187">AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9d5f-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="d9d5f-188">移除-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="d9d5f-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

