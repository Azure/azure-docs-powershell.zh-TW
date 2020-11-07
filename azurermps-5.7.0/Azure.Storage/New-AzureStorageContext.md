---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 678453cc050ae31158f4f08e1efcda00338aca98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624116"
---
# <span data-ttu-id="cad78-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="cad78-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="cad78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cad78-102">SYNOPSIS</span></span>
<span data-ttu-id="cad78-103">建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cad78-104">句法</span><span class="sxs-lookup"><span data-stu-id="cad78-104">SYNTAX</span></span>

### <span data-ttu-id="cad78-105">AccountNameAndKey (預設) </span><span class="sxs-lookup"><span data-stu-id="cad78-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="cad78-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="cad78-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="cad78-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="cad78-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cad78-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="cad78-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="cad78-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="cad78-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="cad78-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cad78-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="cad78-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="cad78-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="cad78-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="cad78-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="cad78-113">說明</span><span class="sxs-lookup"><span data-stu-id="cad78-113">DESCRIPTION</span></span>
<span data-ttu-id="cad78-114">**新的-AzureStorageCoNtext** Cmdlet 會建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="cad78-115">示例</span><span class="sxs-lookup"><span data-stu-id="cad78-115">EXAMPLES</span></span>

### <span data-ttu-id="cad78-116">範例1：透過指定儲存空間帳戶名稱和金鑰來建立內容</span><span class="sxs-lookup"><span data-stu-id="cad78-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="cad78-117">這個命令會為使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="cad78-118">範例2：透過指定連接字串來建立內容</span><span class="sxs-lookup"><span data-stu-id="cad78-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="cad78-119">這個命令會根據帳戶 ContosoGeneral 的指定連接字串來建立內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="cad78-120">範例3：建立匿名儲存空間帳戶的內容</span><span class="sxs-lookup"><span data-stu-id="cad78-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="cad78-121">這個命令會建立名為 ContosoGeneral 的帳戶匿名使用的內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="cad78-122">該命令會將 HTTP 指定為連線通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cad78-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="cad78-123">範例4：使用本機開發儲存空間帳戶建立內容</span><span class="sxs-lookup"><span data-stu-id="cad78-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="cad78-124">這個命令會使用本機開發儲存空間帳戶來建立內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="cad78-125">命令會指定 *本機* 參數。</span><span class="sxs-lookup"><span data-stu-id="cad78-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="cad78-126">範例5：取得本機開發人員儲存空間帳戶的容器</span><span class="sxs-lookup"><span data-stu-id="cad78-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="cad78-127">這個命令會使用本機開發儲存空間帳戶建立內容，然後使用管線運算子將新的內容傳送到 **AzureStorageContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cad78-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cad78-128">此命令會取得本機開發人員儲存空間帳戶的 Azure 儲存體容器。</span><span class="sxs-lookup"><span data-stu-id="cad78-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="cad78-129">範例6：取得多個容器</span><span class="sxs-lookup"><span data-stu-id="cad78-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="cad78-130">第一個命令會使用本機開發儲存空間帳戶建立內容，然後將該內容儲存在 $CoNtext 01 變數中。</span><span class="sxs-lookup"><span data-stu-id="cad78-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>

<span data-ttu-id="cad78-131">第二個命令會針對使用指定金鑰的帳戶（名為 ContosoGeneral）建立內容，然後將該內容儲存在 $CoNtext 02 變數中。</span><span class="sxs-lookup"><span data-stu-id="cad78-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>

<span data-ttu-id="cad78-132">最後一個命令會使用 **AzureStorageContainer** ，透過 $CoNtext 01 和 $CoNtext 02 中的內容來取得所儲存之上下文的容器。</span><span class="sxs-lookup"><span data-stu-id="cad78-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="cad78-133">範例7：使用端點建立內容</span><span class="sxs-lookup"><span data-stu-id="cad78-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="cad78-134">這個命令會建立具有指定儲存端點的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="cad78-135">此命令會為使用指定金鑰的帳戶建立名為 ContosoGeneral 的內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="cad78-136">範例8：建立具有指定環境的內容</span><span class="sxs-lookup"><span data-stu-id="cad78-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="cad78-137">這個命令會建立具有指定 Azure 環境的 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="cad78-138">此命令會為使用指定金鑰的帳戶建立名為 ContosoGeneral 的內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="cad78-139">範例9：使用 SAS 權杖建立內容</span><span class="sxs-lookup"><span data-stu-id="cad78-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="cad78-140">第一個命令會使用名為 ContosoMain 之容器的 **新 AzureStorageContainerSASToken** Cmdlet 來產生 SAS 權杖，然後將該權杖儲存在 $SasToken 變數中。</span><span class="sxs-lookup"><span data-stu-id="cad78-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="cad78-141">該權杖用於讀取、新增、更新和刪除許可權。</span><span class="sxs-lookup"><span data-stu-id="cad78-141">That token is for read, add, update, and delete permissions.</span></span>

<span data-ttu-id="cad78-142">第二個命令會建立名為 ContosoGeneral 的帳戶的內容，該帳戶會使用儲存在 $SasToken 中的 SAS 權杖，然後將該內容儲存在 $CoNtext 變數中。</span><span class="sxs-lookup"><span data-stu-id="cad78-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>

<span data-ttu-id="cad78-143">最終命令會使用 $CoNtext 中儲存的內容，列出與名為 ContosoMain 的容器相關的所有 blob。</span><span class="sxs-lookup"><span data-stu-id="cad78-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="cad78-144">參數</span><span class="sxs-lookup"><span data-stu-id="cad78-144">PARAMETERS</span></span>

### <span data-ttu-id="cad78-145">-匿名</span><span class="sxs-lookup"><span data-stu-id="cad78-145">-Anonymous</span></span>
<span data-ttu-id="cad78-146">表示此 Cmdlet 會為匿名登入建立 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-147">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="cad78-147">-ConnectionString</span></span>
<span data-ttu-id="cad78-148">指定 Azure 儲存區內容的連線字串。</span><span class="sxs-lookup"><span data-stu-id="cad78-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-149">-端點</span><span class="sxs-lookup"><span data-stu-id="cad78-149">-Endpoint</span></span>
<span data-ttu-id="cad78-150">指定 Azure 儲存區內容的端點。</span><span class="sxs-lookup"><span data-stu-id="cad78-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-151">-環境</span><span class="sxs-lookup"><span data-stu-id="cad78-151">-Environment</span></span>
<span data-ttu-id="cad78-152">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="cad78-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="cad78-153">此參數可接受的值為： AzureCloud 和 AzureChinaCloud。</span><span class="sxs-lookup"><span data-stu-id="cad78-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="cad78-154">如需詳細資訊，請輸入 `Get-Help Get-AzureEnvironment` 。</span><span class="sxs-lookup"><span data-stu-id="cad78-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-155">-本機</span><span class="sxs-lookup"><span data-stu-id="cad78-155">-Local</span></span>
<span data-ttu-id="cad78-156">指示這個 Cmdlet 使用本機開發儲存空間帳戶來建立內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-157">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="cad78-157">-Protocol</span></span>
<span data-ttu-id="cad78-158"> (HTTPs/HTTP) 傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cad78-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="cad78-159">-SasToken</span></span>
<span data-ttu-id="cad78-160">指定內容的共用存取簽名 (SAS) 標記。</span><span class="sxs-lookup"><span data-stu-id="cad78-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cad78-161">-StorageAccountKey</span></span>
<span data-ttu-id="cad78-162">指定 Azure 儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="cad78-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="cad78-163">這個 Cmdlet 會建立此參數指定之金鑰的內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cad78-164">-StorageAccountName</span></span>
<span data-ttu-id="cad78-165">指定 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cad78-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="cad78-166">這個 Cmdlet 會建立此參數指定之帳戶的內容。</span><span class="sxs-lookup"><span data-stu-id="cad78-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cad78-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad78-167">CommonParameters</span></span>
<span data-ttu-id="cad78-168">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cad78-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad78-169">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cad78-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad78-170">輸入</span><span class="sxs-lookup"><span data-stu-id="cad78-170">INPUTS</span></span>

### <span data-ttu-id="cad78-171">所有</span><span class="sxs-lookup"><span data-stu-id="cad78-171">None</span></span>
<span data-ttu-id="cad78-172">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cad78-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cad78-173">輸出</span><span class="sxs-lookup"><span data-stu-id="cad78-173">OUTPUTS</span></span>

### <span data-ttu-id="cad78-174">AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="cad78-174">AzureStorageContext</span></span>

## <span data-ttu-id="cad78-175">筆記</span><span class="sxs-lookup"><span data-stu-id="cad78-175">NOTES</span></span>

## <span data-ttu-id="cad78-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="cad78-176">RELATED LINKS</span></span>

[<span data-ttu-id="cad78-177">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cad78-177">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="cad78-178">新-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cad78-178">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


