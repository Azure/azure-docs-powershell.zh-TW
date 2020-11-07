---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: eca1322f1638039fce6c478b19e94b586fd83bbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793075"
---
# <span data-ttu-id="fed53-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fed53-101">New-AzStorageContext</span></span>

## <span data-ttu-id="fed53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fed53-102">SYNOPSIS</span></span>
<span data-ttu-id="fed53-103">建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="fed53-104">句法</span><span class="sxs-lookup"><span data-stu-id="fed53-104">SYNTAX</span></span>

### <span data-ttu-id="fed53-105">OAuthAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="fed53-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="fed53-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="fed53-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="fed53-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="fed53-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="fed53-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="fed53-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fed53-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="fed53-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="fed53-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="fed53-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="fed53-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="fed53-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="fed53-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="fed53-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="fed53-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="fed53-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="fed53-114">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="fed53-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="fed53-115">說明</span><span class="sxs-lookup"><span data-stu-id="fed53-115">DESCRIPTION</span></span>
<span data-ttu-id="fed53-116">**新的-AzStorageCoNtext** Cmdlet 會建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="fed53-117">儲存內容的預設驗證是 OAuth (Azure AD) ，如果只輸入儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fed53-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="fed53-118">請參閱中的儲存服務驗證詳細資料 https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services 。</span><span class="sxs-lookup"><span data-stu-id="fed53-118">See details of authentication of the Storage Service in https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="fed53-119">示例</span><span class="sxs-lookup"><span data-stu-id="fed53-119">EXAMPLES</span></span>

### <span data-ttu-id="fed53-120">範例1：透過指定儲存空間帳戶名稱和金鑰來建立內容</span><span class="sxs-lookup"><span data-stu-id="fed53-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="fed53-121">這個命令會為使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="fed53-122">範例2：透過指定連接字串來建立內容</span><span class="sxs-lookup"><span data-stu-id="fed53-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="fed53-123">這個命令會根據帳戶 ContosoGeneral 的指定連接字串來建立內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="fed53-124">範例3：建立匿名儲存空間帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="fed53-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="fed53-125">這個命令會建立名為 ContosoGeneral 的帳戶匿名使用的內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="fed53-126">該命令會將 HTTP 指定為連線通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fed53-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="fed53-127">範例4：使用本機開發儲存空間帳戶建立內容</span><span class="sxs-lookup"><span data-stu-id="fed53-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="fed53-128">這個命令會使用本機開發儲存空間帳戶來建立內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="fed53-129">命令會指定 *本機* 參數。</span><span class="sxs-lookup"><span data-stu-id="fed53-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="fed53-130">範例5：取得本機開發人員儲存空間帳戶的容器</span><span class="sxs-lookup"><span data-stu-id="fed53-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="fed53-131">這個命令會使用本機開發儲存空間帳戶建立內容，然後使用管線運算子將新的內容傳送到 **AzStorageContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fed53-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fed53-132">此命令會取得本機開發人員儲存空間帳戶的 Azure 儲存體容器。</span><span class="sxs-lookup"><span data-stu-id="fed53-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="fed53-133">範例6：取得多個容器</span><span class="sxs-lookup"><span data-stu-id="fed53-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="fed53-134">第一個命令會使用本機開發儲存空間帳戶建立內容，然後將該內容儲存在 $CoNtext 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="fed53-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="fed53-135">第二個命令會針對使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容，然後將該內容儲存在 $CoNtext 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="fed53-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="fed53-136">最後一個命令會使用 **AzStorageContainer** ，透過 $CoNtext 01 和 $CoNtext 02 中的內容來取得所儲存之上下文的容器。</span><span class="sxs-lookup"><span data-stu-id="fed53-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="fed53-137">範例7：使用端點建立內容</span><span class="sxs-lookup"><span data-stu-id="fed53-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="fed53-138">這個命令會建立具有指定儲存端點的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="fed53-139">此命令會為使用指定金鑰的帳戶建立名為 ContosoGeneral 的內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="fed53-140">範例8：建立具有指定環境的內容</span><span class="sxs-lookup"><span data-stu-id="fed53-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="fed53-141">這個命令會建立具有指定 Azure 環境的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="fed53-142">此命令會為使用指定金鑰的帳戶建立名為 ContosoGeneral 的內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="fed53-143">範例9：使用 SAS 權杖建立內容</span><span class="sxs-lookup"><span data-stu-id="fed53-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="fed53-144">第一個命令會使用名為 ContosoMain 之容器的 **新 AzStorageContainerSASToken** Cmdlet 來產生 SAS 權杖，然後將該權杖儲存在 $SasToken 變數中。</span><span class="sxs-lookup"><span data-stu-id="fed53-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="fed53-145">該權杖用於讀取、新增、更新和刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="fed53-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="fed53-146">第二個命令會建立名為 ContosoGeneral 的帳戶的內容，該帳戶會使用儲存在 $SasToken 中的 SAS 權杖，然後將該內容儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="fed53-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="fed53-147">最終命令會使用 $CoNtext 中儲存的內容，列出與名為 ContosoMain 的容器相關的所有 blob。</span><span class="sxs-lookup"><span data-stu-id="fed53-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="fed53-148">範例10：使用 OAuth 驗證建立內容</span><span class="sxs-lookup"><span data-stu-id="fed53-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="fed53-149">這個命令會使用 OAuth (Azure AD) 驗證來建立內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-149">This command creates a context by using the OAuth (Azure AD)  Authentication.</span></span>

## <span data-ttu-id="fed53-150">參數</span><span class="sxs-lookup"><span data-stu-id="fed53-150">PARAMETERS</span></span>

### <span data-ttu-id="fed53-151">-匿名</span><span class="sxs-lookup"><span data-stu-id="fed53-151">-Anonymous</span></span>
<span data-ttu-id="fed53-152">表示此 Cmdlet 會為匿名登入建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-153">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="fed53-153">-ConnectionString</span></span>
<span data-ttu-id="fed53-154">指定 Azure 儲存區內容的連線字串。</span><span class="sxs-lookup"><span data-stu-id="fed53-154">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-155">-端點</span><span class="sxs-lookup"><span data-stu-id="fed53-155">-Endpoint</span></span>
<span data-ttu-id="fed53-156">指定 Azure 儲存區內容的端點。</span><span class="sxs-lookup"><span data-stu-id="fed53-156">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-157">-環境</span><span class="sxs-lookup"><span data-stu-id="fed53-157">-Environment</span></span>
<span data-ttu-id="fed53-158">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="fed53-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="fed53-159">此參數可接受的值為： AzureCloud 和 AzureChinaCloud。</span><span class="sxs-lookup"><span data-stu-id="fed53-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="fed53-160">如需詳細資訊，請輸入 `Get-Help Get-AzEnvironment` 。</span><span class="sxs-lookup"><span data-stu-id="fed53-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-161">-本機</span><span class="sxs-lookup"><span data-stu-id="fed53-161">-Local</span></span>
<span data-ttu-id="fed53-162">指示這個 Cmdlet 使用本機開發儲存空間帳戶來建立內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-163">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="fed53-163">-Protocol</span></span>
<span data-ttu-id="fed53-164"> (HTTPs/HTTP) 傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="fed53-164">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="fed53-165">-SasToken</span></span>
<span data-ttu-id="fed53-166">指定內容的共用存取簽名 (SAS) 標記。</span><span class="sxs-lookup"><span data-stu-id="fed53-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fed53-167">-StorageAccountKey</span></span>
<span data-ttu-id="fed53-168">指定 Azure 儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="fed53-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="fed53-169">這個 Cmdlet 會建立此參數指定之金鑰的內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fed53-170">-StorageAccountName</span></span>
<span data-ttu-id="fed53-171">指定 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fed53-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="fed53-172">這個 Cmdlet 會建立此參數指定之帳戶的內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-173">-UseConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="fed53-173">-UseConnectedAccount</span></span>
<span data-ttu-id="fed53-174">表示此 Cmdlet 會使用 OAuth (Azure AD) 驗證來建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fed53-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="fed53-175">預設情況下，如果未指定其他驗證，則 Cmdlet 會使用 OAuth 驗證。</span><span class="sxs-lookup"><span data-stu-id="fed53-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed53-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed53-176">CommonParameters</span></span>
<span data-ttu-id="fed53-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fed53-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed53-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fed53-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed53-179">輸入</span><span class="sxs-lookup"><span data-stu-id="fed53-179">INPUTS</span></span>

### <span data-ttu-id="fed53-180">System.object</span><span class="sxs-lookup"><span data-stu-id="fed53-180">System.String</span></span>

## <span data-ttu-id="fed53-181">輸出</span><span class="sxs-lookup"><span data-stu-id="fed53-181">OUTPUTS</span></span>

### <span data-ttu-id="fed53-182">AzureStorageCoNtext 中的 WindowsAzure</span><span class="sxs-lookup"><span data-stu-id="fed53-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="fed53-183">筆記</span><span class="sxs-lookup"><span data-stu-id="fed53-183">NOTES</span></span>

## <span data-ttu-id="fed53-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="fed53-184">RELATED LINKS</span></span>

[<span data-ttu-id="fed53-185">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fed53-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="fed53-186">新-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="fed53-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

