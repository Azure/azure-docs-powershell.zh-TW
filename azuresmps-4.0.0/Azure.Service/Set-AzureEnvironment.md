---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967413"
---
# <span data-ttu-id="a09ac-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a09ac-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="a09ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a09ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a09ac-103">變更 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="a09ac-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="a09ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a09ac-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a09ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="a09ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a09ac-106">**AzureEnvironment** Cmdlet 會變更 Azure 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="a09ac-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="a09ac-107">它會傳回代表環境及其新屬性值的物件。</span><span class="sxs-lookup"><span data-stu-id="a09ac-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="a09ac-108">使用 **Name** 參數來識別環境及其他參數，以變更屬性值。</span><span class="sxs-lookup"><span data-stu-id="a09ac-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="a09ac-109">您無法使用 [ **設定-AzureEnvironment** ] 來變更 Azure 環境的名稱。</span><span class="sxs-lookup"><span data-stu-id="a09ac-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="a09ac-110">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="a09ac-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="a09ac-111">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="a09ac-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="a09ac-112">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="a09ac-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="a09ac-113">注意：請勿變更 AzureCloud 或 AzureChinaCloud 環境的屬性。</span><span class="sxs-lookup"><span data-stu-id="a09ac-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="a09ac-114">使用此 Cmdlet 來變更您建立的私人環境值。</span><span class="sxs-lookup"><span data-stu-id="a09ac-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="a09ac-115">示例</span><span class="sxs-lookup"><span data-stu-id="a09ac-115">EXAMPLES</span></span>

### <span data-ttu-id="a09ac-116">範例1：變更環境屬性</span><span class="sxs-lookup"><span data-stu-id="a09ac-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="a09ac-117">這個命令會變更 ContosoEnv 環境的 **PublishSettingsFileUrl** 和 **StorageEndpoint** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a09ac-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="a09ac-118">參數</span><span class="sxs-lookup"><span data-stu-id="a09ac-118">PARAMETERS</span></span>

### <span data-ttu-id="a09ac-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a09ac-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="a09ac-120">將 Azure Active Directory 驗證的端點變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="a09ac-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

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

### <span data-ttu-id="a09ac-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a09ac-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="a09ac-122">指定管理 API 的資源識別碼，其存取權由 Azure Active Directory 管理。</span><span class="sxs-lookup"><span data-stu-id="a09ac-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="a09ac-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="a09ac-123">-AdTenant</span></span>
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

### <span data-ttu-id="a09ac-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a09ac-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="a09ac-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a09ac-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="a09ac-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="a09ac-126">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="a09ac-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a09ac-127">-GalleryEndpoint</span></span>
<span data-ttu-id="a09ac-128">將 Azure 資源管理器圖庫的端點變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="a09ac-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="a09ac-129">圖庫端點是資源群組圖庫範本的位置。</span><span class="sxs-lookup"><span data-stu-id="a09ac-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="a09ac-130">如需有關 Azure 資源群組和圖庫範本的詳細資訊，請參閱 [取得 AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052)的說明主題。</span><span class="sxs-lookup"><span data-stu-id="a09ac-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

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

### <span data-ttu-id="a09ac-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="a09ac-131">-GraphEndpoint</span></span>
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

### <span data-ttu-id="a09ac-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="a09ac-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="a09ac-133">將 Azure 管理入口網站的 URL 變更為指定的值。</span><span class="sxs-lookup"><span data-stu-id="a09ac-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="a09ac-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a09ac-134">-Name</span></span>
<span data-ttu-id="a09ac-135">識別所變更的環境。</span><span class="sxs-lookup"><span data-stu-id="a09ac-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="a09ac-136">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a09ac-136">This parameter is required.</span></span>
<span data-ttu-id="a09ac-137">參數值區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a09ac-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="a09ac-138">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="a09ac-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a09ac-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a09ac-139">-Profile</span></span>
<span data-ttu-id="a09ac-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a09ac-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a09ac-141">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a09ac-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a09ac-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="a09ac-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="a09ac-143">變更指定環境中發佈設定檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="a09ac-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="a09ac-144">Azure 發佈設定檔案是一個 XML 檔案，其中包含您帳戶的相關資訊，以及允許 Windows PowerShell 代表您的 Azure 帳戶的管理憑證。</span><span class="sxs-lookup"><span data-stu-id="a09ac-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="a09ac-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a09ac-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="a09ac-146">變更 Azure 資源管理器資料的端點，包括與該帳戶相關聯之資源群組的資料。</span><span class="sxs-lookup"><span data-stu-id="a09ac-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="a09ac-147">如需有關 Azure 資源管理員的詳細資訊，請參閱 [Azure 資源管理器 Cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) 並 [使用 Windows PowerShell 與資源管理員](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767) 。</span><span class="sxs-lookup"><span data-stu-id="a09ac-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="a09ac-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a09ac-148">-ServiceEndpoint</span></span>
<span data-ttu-id="a09ac-149">變更指定環境中 Azure 服務端點的 URL。</span><span class="sxs-lookup"><span data-stu-id="a09ac-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="a09ac-150">Azure 服務端點會判斷您的應用程式是由全域 Azure 平臺、由中國由世紀運營的 Azure 或私人 Azure 安裝來管理。</span><span class="sxs-lookup"><span data-stu-id="a09ac-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="a09ac-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a09ac-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="a09ac-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="a09ac-152">-StorageEndpoint</span></span>
<span data-ttu-id="a09ac-153">變更指定環境中儲存服務的預設端點。</span><span class="sxs-lookup"><span data-stu-id="a09ac-153">Changes the default endpoint of storage services in the specified environment.</span></span>

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

### <span data-ttu-id="a09ac-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a09ac-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="a09ac-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09ac-155">CommonParameters</span></span>
<span data-ttu-id="a09ac-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a09ac-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09ac-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a09ac-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09ac-158">輸入</span><span class="sxs-lookup"><span data-stu-id="a09ac-158">INPUTS</span></span>

### <span data-ttu-id="a09ac-159">所有</span><span class="sxs-lookup"><span data-stu-id="a09ac-159">None</span></span>
<span data-ttu-id="a09ac-160">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a09ac-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a09ac-161">輸出</span><span class="sxs-lookup"><span data-stu-id="a09ac-161">OUTPUTS</span></span>

### <span data-ttu-id="a09ac-162">WindowsAzure. 常見. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a09ac-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="a09ac-163">筆記</span><span class="sxs-lookup"><span data-stu-id="a09ac-163">NOTES</span></span>

## <span data-ttu-id="a09ac-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="a09ac-164">RELATED LINKS</span></span>

[<span data-ttu-id="a09ac-165">附加 AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a09ac-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="a09ac-166">AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a09ac-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="a09ac-167">移除-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a09ac-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


