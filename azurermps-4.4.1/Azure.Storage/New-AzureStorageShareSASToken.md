---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 84f280bf5e3297796bb8b56e5a5d42e513b79e79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446906"
---
# <span data-ttu-id="58e7c-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="58e7c-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="58e7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="58e7c-103">產生 Azure 儲存空間共用的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="58e7c-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="58e7c-104">SYNTAX</span></span>

### <span data-ttu-id="58e7c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="58e7c-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="58e7c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="58e7c-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="58e7c-107">說明</span><span class="sxs-lookup"><span data-stu-id="58e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="58e7c-108">**新的-AzureStorageShareSASToken** Cmdlet 會針對 Azure 儲存空間共用產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="58e7c-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="58e7c-109">示例</span><span class="sxs-lookup"><span data-stu-id="58e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="58e7c-110">範例1：為共用產生共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="58e7c-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="58e7c-111">這個命令會建立名為 ContosoShare 的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="58e7c-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="58e7c-112">範例2：使用管線產生多個共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="58e7c-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="58e7c-113">這個命令會取得符合前置詞測試的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="58e7c-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="58e7c-114">命令會使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58e7c-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="58e7c-115">目前的 Cmdlet 會為具有指定許可權的每個儲存空間共用建立共用存取權杖。</span><span class="sxs-lookup"><span data-stu-id="58e7c-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="58e7c-116">範例3：產生使用共用存取原則的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="58e7c-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="58e7c-117">這個命令會為擁有名為 ContosoPolicy03 原則之名為 ContosoShare 的儲存空間共用建立共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="58e7c-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="58e7c-118">參數</span><span class="sxs-lookup"><span data-stu-id="58e7c-118">PARAMETERS</span></span>

### <span data-ttu-id="58e7c-119">-內容</span><span class="sxs-lookup"><span data-stu-id="58e7c-119">-Context</span></span>
<span data-ttu-id="58e7c-120">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="58e7c-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="58e7c-121">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58e7c-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="58e7c-122">-ExpiryTime</span></span>
<span data-ttu-id="58e7c-123">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="58e7c-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="58e7c-124">-FullUri</span></span>
<span data-ttu-id="58e7c-125">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="58e7c-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="58e7c-126">-IPAddressOrRange</span></span>
<span data-ttu-id="58e7c-127">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="58e7c-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="58e7c-128">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="58e7c-128">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-129">-許可權</span><span class="sxs-lookup"><span data-stu-id="58e7c-129">-Permission</span></span>
<span data-ttu-id="58e7c-130">指定權杖中的許可權，以存取共用中的共用和檔案。</span><span class="sxs-lookup"><span data-stu-id="58e7c-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-131">-原則</span><span class="sxs-lookup"><span data-stu-id="58e7c-131">-Policy</span></span>
<span data-ttu-id="58e7c-132">指定共用的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="58e7c-132">Specifies the stored access policy for a share.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-133">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="58e7c-133">-Protocol</span></span>
<span data-ttu-id="58e7c-134">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="58e7c-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="58e7c-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="58e7c-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="58e7c-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="58e7c-136">HttpsOnly</span></span>
* <span data-ttu-id="58e7c-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="58e7c-137">HttpsOrHttp</span></span>

<span data-ttu-id="58e7c-138">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="58e7c-138">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-139">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="58e7c-139">-ShareName</span></span>
<span data-ttu-id="58e7c-140">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="58e7c-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="58e7c-141">-StartTime</span></span>
<span data-ttu-id="58e7c-142">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="58e7c-142">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e7c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e7c-143">CommonParameters</span></span>
<span data-ttu-id="58e7c-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58e7c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e7c-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58e7c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e7c-146">輸入</span><span class="sxs-lookup"><span data-stu-id="58e7c-146">INPUTS</span></span>

### <span data-ttu-id="58e7c-147">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="58e7c-147">IStorageContext</span></span>

<span data-ttu-id="58e7c-148">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="58e7c-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="58e7c-149">字串</span><span class="sxs-lookup"><span data-stu-id="58e7c-149">String</span></span>

<span data-ttu-id="58e7c-150">參數「共用名稱」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="58e7c-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="58e7c-151">輸出</span><span class="sxs-lookup"><span data-stu-id="58e7c-151">OUTPUTS</span></span>

### <span data-ttu-id="58e7c-152">System.object</span><span class="sxs-lookup"><span data-stu-id="58e7c-152">System.String</span></span>

## <span data-ttu-id="58e7c-153">筆記</span><span class="sxs-lookup"><span data-stu-id="58e7c-153">NOTES</span></span>
* <span data-ttu-id="58e7c-154">關鍵字：常見、azure、services、data、storage、blob、queue、table</span><span class="sxs-lookup"><span data-stu-id="58e7c-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="58e7c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="58e7c-155">RELATED LINKS</span></span>

[<span data-ttu-id="58e7c-156">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e7c-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="58e7c-157">新-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="58e7c-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
