---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: 4e4a86d5054a5554cb473c60550d32adffae5e46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915077"
---
# <span data-ttu-id="d7518-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d7518-101">New-AzStorageContext</span></span>

## <span data-ttu-id="d7518-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7518-102">SYNOPSIS</span></span>
<span data-ttu-id="d7518-103">建立 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="d7518-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="d7518-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7518-104">SYNTAX</span></span>

### <span data-ttu-id="d7518-105">OAuthAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="d7518-105">OAuthAccount (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7518-106">AccountNameAndKey</span><span class="sxs-lookup"><span data-stu-id="d7518-106">AccountNameAndKey</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7518-107">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="d7518-107">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d7518-108">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="d7518-108">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7518-109">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d7518-109">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d7518-110">SasToken</span><span class="sxs-lookup"><span data-stu-id="d7518-110">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7518-111">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d7518-111">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="d7518-112">OAuthAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="d7518-112">OAuthAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="d7518-113">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d7518-113">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="d7518-114">Local一級</span><span class="sxs-lookup"><span data-stu-id="d7518-114">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="d7518-115">描述</span><span class="sxs-lookup"><span data-stu-id="d7518-115">DESCRIPTION</span></span>
<span data-ttu-id="d7518-116">**New-AzStorageCoNtext** Cmdlet 會建立 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="d7518-116">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>
<span data-ttu-id="d7518-117">儲存內容的預設驗證為 OAuth (Azure AD) 輸入儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d7518-117">The default Authentication of a Storage Context is OAuth (Azure AD), if only input Storage account name.</span></span>
<span data-ttu-id="d7518-118">請參閱 中的儲存服務驗證詳細資料 https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services 。</span><span class="sxs-lookup"><span data-stu-id="d7518-118">See details of authentication of the Storage Service in https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services.</span></span>

## <span data-ttu-id="d7518-119">例子</span><span class="sxs-lookup"><span data-stu-id="d7518-119">EXAMPLES</span></span>

### <span data-ttu-id="d7518-120">範例 1：指定儲存帳戶名稱和金鑰以建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-120">Example 1: Create a context by specifying a storage account name and key</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="d7518-121">此命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-121">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d7518-122">範例 2：指定連接字串以建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-122">Example 2: Create a context by specifying a connection string</span></span>
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="d7518-123">此命令會根據帳戶 ContosoGeneral 的指定連接字串建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-123">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="d7518-124">範例 3：建立匿名儲存帳戶的上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-124">Example 3: Create a context for an anonymous storage account</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="d7518-125">此命令會為名為 ContosoGeneral 的帳戶建立匿名使用上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-125">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="d7518-126">命令會指定 HTTP 做為連接通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d7518-126">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="d7518-127">範例 4：使用本地開發儲存空間帳戶建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-127">Example 4: Create a context by using the local development storage account</span></span>
```
PS C:\>New-AzStorageContext -Local
```

<span data-ttu-id="d7518-128">此命令會使用本地開發儲存帳戶建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-128">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="d7518-129">命令會指定 *Local* 參數。</span><span class="sxs-lookup"><span data-stu-id="d7518-129">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="d7518-130">範例 5：取得本地開發人員儲存帳戶的容器</span><span class="sxs-lookup"><span data-stu-id="d7518-130">Example 5: Get the container for the local developer storage account</span></span>
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="d7518-131">此命令會使用本地開發儲存帳戶建立上下文，然後使用管線運算子將新內容傳遞給 **Get-AzStorageContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d7518-131">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7518-132">該命令會為本地開發人員儲存帳戶獲得 Azure 儲存容器。</span><span class="sxs-lookup"><span data-stu-id="d7518-132">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="d7518-133">範例 6：取得多個容器</span><span class="sxs-lookup"><span data-stu-id="d7518-133">Example 6: Get multiple containers</span></span>
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="d7518-134">第一個命令會使用本地開發儲存空間帳戶建立上下文，然後將該上下文儲存在 $CoNtext 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="d7518-134">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="d7518-135">第二個命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文，然後將該上下文儲存在 $CoNtext 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="d7518-135">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="d7518-136">最後一個命令會使用 **Get-AzStorageContainer** 取得儲存在 $CoNtext 01 和 $CoNtext 02 之上下文的容器。</span><span class="sxs-lookup"><span data-stu-id="d7518-136">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="d7518-137">範例 7：使用端點建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-137">Example 7: Create a context with an endpoint</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="d7518-138">此命令會建立具有指定儲存端點的 Azure 儲存體上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-138">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="d7518-139">該命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-139">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d7518-140">範例 8：使用指定的環境建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-140">Example 8: Create a context with a specified environment</span></span>
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="d7518-141">此命令會建立具有指定 Azure 環境的 Azure 儲存上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-141">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="d7518-142">該命令會針對使用指定金鑰的 ContosoGeneral 帳戶建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-142">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="d7518-143">範例 9：使用 SAS 權杖建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-143">Example 9: Create a context by using an SAS token</span></span>
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="d7518-144">第一個命令會針對名為 ContosoMain 的容器使用 **New-AzStorageContainerSASToken** Cmdlet 來產生 SAS 權杖，然後將該權杖儲存在 $SasToken 變數中。</span><span class="sxs-lookup"><span data-stu-id="d7518-144">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="d7518-145">該權杖適用于讀取、新增、更新及刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="d7518-145">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="d7518-146">第二個命令會針對名為 ContosoGeneral 的帳戶建立上下文，該帳戶使用儲存在 $SasToken 中的 SAS 權杖，然後將該上下文儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="d7518-146">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="d7518-147">最後一個命令會使用儲存在其中上下文，列出與名為 ContosoMain 之容器相關聯的所有$CoNtext。</span><span class="sxs-lookup"><span data-stu-id="d7518-147">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

### <span data-ttu-id="d7518-148">範例 10：使用 OAuth 驗證建立上下文</span><span class="sxs-lookup"><span data-stu-id="d7518-148">Example 10: Create a context by using the OAuth Authentication</span></span>
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

<span data-ttu-id="d7518-149">此命令會使用 OAuth (Azure AD) 內容。</span><span class="sxs-lookup"><span data-stu-id="d7518-149">This command creates a context by using the OAuth (Azure AD) Authentication.</span></span>

## <span data-ttu-id="d7518-150">參數</span><span class="sxs-lookup"><span data-stu-id="d7518-150">PARAMETERS</span></span>

### <span data-ttu-id="d7518-151">-匿名</span><span class="sxs-lookup"><span data-stu-id="d7518-151">-Anonymous</span></span>
<span data-ttu-id="d7518-152">表示此 Cmdlet 會建立匿名登入的 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="d7518-152">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="d7518-153">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d7518-153">-ConnectionString</span></span>
<span data-ttu-id="d7518-154">指定 Azure 儲存體上下文的連接字串。</span><span class="sxs-lookup"><span data-stu-id="d7518-154">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="d7518-155">-端點</span><span class="sxs-lookup"><span data-stu-id="d7518-155">-Endpoint</span></span>
<span data-ttu-id="d7518-156">指定 Azure 儲存體上下文的端點。</span><span class="sxs-lookup"><span data-stu-id="d7518-156">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="d7518-157">-環境</span><span class="sxs-lookup"><span data-stu-id="d7518-157">-Environment</span></span>
<span data-ttu-id="d7518-158">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="d7518-158">Specifies the Azure environment.</span></span>
<span data-ttu-id="d7518-159">此參數可接受的值為：AzureCloud 和 AzureChinaCloud。</span><span class="sxs-lookup"><span data-stu-id="d7518-159">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="d7518-160">如需要詳細資訊，請鍵入 `Get-Help Get-AzEnvironment` 。</span><span class="sxs-lookup"><span data-stu-id="d7518-160">For more information, type `Get-Help Get-AzEnvironment`.</span></span>

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

### <span data-ttu-id="d7518-161">-本地</span><span class="sxs-lookup"><span data-stu-id="d7518-161">-Local</span></span>
<span data-ttu-id="d7518-162">表示此 Cmdlet 是使用本地開發儲存帳戶建立內容。</span><span class="sxs-lookup"><span data-stu-id="d7518-162">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="d7518-163">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="d7518-163">-Protocol</span></span>
<span data-ttu-id="d7518-164">傳輸通訊協定 (HTTPs/HTTP) 。</span><span class="sxs-lookup"><span data-stu-id="d7518-164">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="d7518-165">-SasToken</span><span class="sxs-lookup"><span data-stu-id="d7518-165">-SasToken</span></span>
<span data-ttu-id="d7518-166">指定一個共用存取簽名 (SAS) 為上下文的權杖。</span><span class="sxs-lookup"><span data-stu-id="d7518-166">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="d7518-167">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d7518-167">-StorageAccountKey</span></span>
<span data-ttu-id="d7518-168">指定 Azure 儲存體帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="d7518-168">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="d7518-169">此 Cmdlet 會為此參數指定的金鑰建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-169">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7518-170">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7518-170">-StorageAccountName</span></span>
<span data-ttu-id="d7518-171">指定 Azure 儲存體帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d7518-171">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="d7518-172">此 Cmdlet 會為此參數指定的帳號建立上下文。</span><span class="sxs-lookup"><span data-stu-id="d7518-172">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7518-173">-使用ConnectedAccount</span><span class="sxs-lookup"><span data-stu-id="d7518-173">-UseConnectedAccount</span></span>
<span data-ttu-id="d7518-174">表示此 Cmdlet 會使用 OAuth (Azure AD) Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="d7518-174">Indicates that this cmdlet creates an Azure Storage context with OAuth (Azure AD) Authentication.</span></span>
<span data-ttu-id="d7518-175">當未指定其他驗證時，Cmdlet 預設會使用 OAuth 驗證。</span><span class="sxs-lookup"><span data-stu-id="d7518-175">The cmdlet will use OAuth Authentication by default, when other authentication not specified.</span></span>

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

### <span data-ttu-id="d7518-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7518-176">CommonParameters</span></span>
<span data-ttu-id="d7518-177">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7518-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7518-178">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d7518-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7518-179">輸入</span><span class="sxs-lookup"><span data-stu-id="d7518-179">INPUTS</span></span>

### <span data-ttu-id="d7518-180">System.String</span><span class="sxs-lookup"><span data-stu-id="d7518-180">System.String</span></span>

## <span data-ttu-id="d7518-181">輸出</span><span class="sxs-lookup"><span data-stu-id="d7518-181">OUTPUTS</span></span>

### <span data-ttu-id="d7518-182">Microsoft.WindowsAzure.Commands.storage.AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="d7518-182">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="d7518-183">筆記</span><span class="sxs-lookup"><span data-stu-id="d7518-183">NOTES</span></span>

## <span data-ttu-id="d7518-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7518-184">RELATED LINKS</span></span>

[<span data-ttu-id="d7518-185">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="d7518-185">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="d7518-186">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d7518-186">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


