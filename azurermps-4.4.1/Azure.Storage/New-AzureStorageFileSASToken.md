---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 052eae9a995aafe9d5d966ae5a17aae31a0fc0fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626523"
---
# <span data-ttu-id="7de35-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="7de35-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="7de35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7de35-102">SYNOPSIS</span></span>
<span data-ttu-id="7de35-103">產生儲存空間的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="7de35-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de35-104">句法</span><span class="sxs-lookup"><span data-stu-id="7de35-104">SYNTAX</span></span>

### <span data-ttu-id="7de35-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="7de35-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="7de35-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="7de35-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="7de35-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="7de35-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="7de35-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="7de35-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="7de35-109">說明</span><span class="sxs-lookup"><span data-stu-id="7de35-109">DESCRIPTION</span></span>
<span data-ttu-id="7de35-110">**新的-AzureStorageFileSASToken** Cmdlet 會針對 Azure 儲存空間檔產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="7de35-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="7de35-111">示例</span><span class="sxs-lookup"><span data-stu-id="7de35-111">EXAMPLES</span></span>

### <span data-ttu-id="7de35-112">範例1：產生具有完整檔案許可權的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="7de35-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="7de35-113">這個命令會產生擁有名為 FilePath 之檔案之完整許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="7de35-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="7de35-114">範例2：產生具有時間限制的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="7de35-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="7de35-115">第一個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de35-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="7de35-116">該命令會將目前的時間儲存在 $StartTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="7de35-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="7de35-117">第二個命令會將兩個小時加到 $StartTime 中的物件，然後將結果儲存在 $EndTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="7de35-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="7de35-118">此物件是在未來兩個小時的時間。</span><span class="sxs-lookup"><span data-stu-id="7de35-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="7de35-119">第三個命令會產生擁有指定許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="7de35-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="7de35-120">此權杖會在目前的時間生效。</span><span class="sxs-lookup"><span data-stu-id="7de35-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="7de35-121">權杖在 $EndTime 中儲存的時間之前一直保持有效。</span><span class="sxs-lookup"><span data-stu-id="7de35-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="7de35-122">參數</span><span class="sxs-lookup"><span data-stu-id="7de35-122">PARAMETERS</span></span>

### <span data-ttu-id="7de35-123">-內容</span><span class="sxs-lookup"><span data-stu-id="7de35-123">-Context</span></span>
<span data-ttu-id="7de35-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="7de35-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7de35-125">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7de35-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de35-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7de35-126">-ExpiryTime</span></span>
<span data-ttu-id="7de35-127">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="7de35-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="7de35-128">檔案</span><span class="sxs-lookup"><span data-stu-id="7de35-128">-File</span></span>
<span data-ttu-id="7de35-129">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="7de35-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="7de35-130">您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="7de35-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de35-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="7de35-131">-FullUri</span></span>
<span data-ttu-id="7de35-132">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="7de35-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="7de35-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="7de35-133">-IPAddressOrRange</span></span>
<span data-ttu-id="7de35-134">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="7de35-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="7de35-135">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="7de35-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="7de35-136">-Path</span><span class="sxs-lookup"><span data-stu-id="7de35-136">-Path</span></span>
<span data-ttu-id="7de35-137">指定檔案相對於儲存區共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="7de35-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de35-138">-許可權</span><span class="sxs-lookup"><span data-stu-id="7de35-138">-Permission</span></span>
<span data-ttu-id="7de35-139">指定儲存空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="7de35-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de35-140">-原則</span><span class="sxs-lookup"><span data-stu-id="7de35-140">-Policy</span></span>
<span data-ttu-id="7de35-141">指定檔案的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="7de35-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de35-142">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="7de35-142">-Protocol</span></span>
<span data-ttu-id="7de35-143">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="7de35-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="7de35-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7de35-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="7de35-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7de35-145">HttpsOnly</span></span>
* <span data-ttu-id="7de35-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="7de35-146">HttpsOrHttp</span></span>

<span data-ttu-id="7de35-147">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="7de35-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="7de35-148">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="7de35-148">-ShareName</span></span>
<span data-ttu-id="7de35-149">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="7de35-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de35-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7de35-150">-StartTime</span></span>
<span data-ttu-id="7de35-151">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="7de35-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="7de35-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de35-152">CommonParameters</span></span>
<span data-ttu-id="7de35-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7de35-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de35-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7de35-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de35-155">輸入</span><span class="sxs-lookup"><span data-stu-id="7de35-155">INPUTS</span></span>

### <span data-ttu-id="7de35-156">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="7de35-156">IStorageContext</span></span>

<span data-ttu-id="7de35-157">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7de35-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7de35-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="7de35-158">CloudFile</span></span>

<span data-ttu-id="7de35-159">形參 "File" 接受管線中 "CloudFile" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7de35-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="7de35-160">字串</span><span class="sxs-lookup"><span data-stu-id="7de35-160">String</span></span>

<span data-ttu-id="7de35-161">形參 "Path" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7de35-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="7de35-162">字串</span><span class="sxs-lookup"><span data-stu-id="7de35-162">String</span></span>

<span data-ttu-id="7de35-163">參數「共用名稱」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7de35-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7de35-164">輸出</span><span class="sxs-lookup"><span data-stu-id="7de35-164">OUTPUTS</span></span>

### <span data-ttu-id="7de35-165">System.object</span><span class="sxs-lookup"><span data-stu-id="7de35-165">System.String</span></span>

## <span data-ttu-id="7de35-166">筆記</span><span class="sxs-lookup"><span data-stu-id="7de35-166">NOTES</span></span>

## <span data-ttu-id="7de35-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="7de35-167">RELATED LINKS</span></span>

[<span data-ttu-id="7de35-168">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="7de35-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7de35-169">新-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="7de35-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
