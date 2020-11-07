---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967176"
---
# <span data-ttu-id="3cce1-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cce1-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="3cce1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3cce1-102">SYNOPSIS</span></span>
<span data-ttu-id="3cce1-103">建立 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="3cce1-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="3cce1-104">句法</span><span class="sxs-lookup"><span data-stu-id="3cce1-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3cce1-105">說明</span><span class="sxs-lookup"><span data-stu-id="3cce1-105">DESCRIPTION</span></span>
<span data-ttu-id="3cce1-106">**AzureEnvironment** Cmdlet 會建立新的自訂 Azure 帳戶環境，並將它儲存在您的漫遊使用者設定檔中。</span><span class="sxs-lookup"><span data-stu-id="3cce1-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="3cce1-107">Cmdlet 會傳回代表新環境的物件。</span><span class="sxs-lookup"><span data-stu-id="3cce1-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="3cce1-108">當命令完成時，您可以在 Windows PowerShell 中使用環境。</span><span class="sxs-lookup"><span data-stu-id="3cce1-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="3cce1-109">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="3cce1-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="3cce1-110">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="3cce1-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="3cce1-111">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="3cce1-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="3cce1-112">只有這個 Cmdlet 的 **Name** 參數是強制性的。</span><span class="sxs-lookup"><span data-stu-id="3cce1-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="3cce1-113">如果您省略參數，則其值為 null ($Null) ，而使用該端點的服務可能無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="3cce1-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="3cce1-114">若要新增或變更環境屬性的值，請使用 **AzureEnvironment** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cce1-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="3cce1-115">注意：變更您的環境可能會導致您的帳戶失敗。</span><span class="sxs-lookup"><span data-stu-id="3cce1-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="3cce1-116">通常只會在測試或疑難排解中新增環境。</span><span class="sxs-lookup"><span data-stu-id="3cce1-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="3cce1-117">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cce1-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3cce1-118">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="3cce1-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="3cce1-119">示例</span><span class="sxs-lookup"><span data-stu-id="3cce1-119">EXAMPLES</span></span>

### <span data-ttu-id="3cce1-120">範例1：新增 Azure 環境</span><span class="sxs-lookup"><span data-stu-id="3cce1-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="3cce1-121">這個命令會建立 ContosoEnv 的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="3cce1-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="3cce1-122">參數</span><span class="sxs-lookup"><span data-stu-id="3cce1-122">PARAMETERS</span></span>

### <span data-ttu-id="3cce1-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cce1-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3cce1-124">指定新環境中的 Azure Active Directory 驗證端點。</span><span class="sxs-lookup"><span data-stu-id="3cce1-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3cce1-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3cce1-126">指定管理 API 的資源識別碼，其存取權由 Azure Active Directory 管理。</span><span class="sxs-lookup"><span data-stu-id="3cce1-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3cce1-127">-AdTenant</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3cce1-128">-AzureKeyVaultDnsSuffix</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3cce1-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3cce1-130">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cce1-131">-GalleryEndpoint</span></span>
<span data-ttu-id="3cce1-132">指定 Azure 資源管理器圖庫的端點，儲存資源群組圖庫範本。</span><span class="sxs-lookup"><span data-stu-id="3cce1-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="3cce1-133">如需有關 Azure 資源群組和圖庫範本的詳細資訊，請參閱取得 AzureResourceGroupGalleryTemplate 的說明主題 https://go.microsoft.com/fwlink/?LinkID=393052 。</span><span class="sxs-lookup"><span data-stu-id="3cce1-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cce1-134">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3cce1-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="3cce1-136">指定新環境中 Azure 管理入口網站的 URL。</span><span class="sxs-lookup"><span data-stu-id="3cce1-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cce1-137">-Name</span></span>
<span data-ttu-id="3cce1-138">指定環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cce1-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="3cce1-139">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="3cce1-139">This parameter is required.</span></span>
<span data-ttu-id="3cce1-140">請勿使用預設環境、AzureCloud 和 AzureChinaCloud 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cce1-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-141">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3cce1-141">-Profile</span></span>
<span data-ttu-id="3cce1-142">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3cce1-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3cce1-143">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3cce1-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3cce1-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3cce1-145">指定您帳戶的發佈設定檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="3cce1-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="3cce1-146">Azure 發佈設定檔案是一個 XML 檔案，其中包含您帳戶的相關資訊，以及允許 Windows PowerShell 代表您的 Azure 帳戶的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="3cce1-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cce1-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3cce1-148">指定 Azure 資源管理器資料的端點，包括與該帳戶相關聯之資源群組的資料。</span><span class="sxs-lookup"><span data-stu-id="3cce1-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="3cce1-149">如需有關 Azure 資源管理員的詳細資訊，請參閱 [Azure 資源管理器 Cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) 並 [使用 Windows PowerShell 與資源管理員](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767) 。</span><span class="sxs-lookup"><span data-stu-id="3cce1-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cce1-150">-ServiceEndpoint</span></span>
<span data-ttu-id="3cce1-151">指定 Azure 服務端點的 URL。</span><span class="sxs-lookup"><span data-stu-id="3cce1-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="3cce1-152">Azure 服務端點會判斷您的應用程式是由全域 Azure 平臺、由中國由世紀運營的 Azure 或私人 Azure 安裝來管理。</span><span class="sxs-lookup"><span data-stu-id="3cce1-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3cce1-153">-SqlDatabaseDnsSuffix</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3cce1-154">-StorageEndpoint</span></span>
<span data-ttu-id="3cce1-155">指定新環境中的儲存空間服務預設端點。</span><span class="sxs-lookup"><span data-stu-id="3cce1-155">Specifies the default endpoint of storage services in the new environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3cce1-156">-TrafficManagerDnsSuffix</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cce1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cce1-157">CommonParameters</span></span>
<span data-ttu-id="3cce1-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3cce1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cce1-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3cce1-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cce1-160">輸入</span><span class="sxs-lookup"><span data-stu-id="3cce1-160">INPUTS</span></span>

### <span data-ttu-id="3cce1-161">所有</span><span class="sxs-lookup"><span data-stu-id="3cce1-161">None</span></span>
<span data-ttu-id="3cce1-162">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cce1-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3cce1-163">輸出</span><span class="sxs-lookup"><span data-stu-id="3cce1-163">OUTPUTS</span></span>

### <span data-ttu-id="3cce1-164">WindowsAzure. 常見. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cce1-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="3cce1-165">筆記</span><span class="sxs-lookup"><span data-stu-id="3cce1-165">NOTES</span></span>

## <span data-ttu-id="3cce1-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cce1-166">RELATED LINKS</span></span>

[<span data-ttu-id="3cce1-167">AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cce1-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="3cce1-168">移除-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cce1-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="3cce1-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3cce1-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


