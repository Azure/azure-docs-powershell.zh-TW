---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443092"
---
# <span data-ttu-id="c334b-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c334b-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="c334b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c334b-102">SYNOPSIS</span></span>
<span data-ttu-id="c334b-103">產生儲存空間的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c334b-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="c334b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c334b-104">SYNTAX</span></span>

### <span data-ttu-id="c334b-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="c334b-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c334b-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="c334b-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c334b-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="c334b-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="c334b-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="c334b-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="c334b-109">說明</span><span class="sxs-lookup"><span data-stu-id="c334b-109">DESCRIPTION</span></span>
<span data-ttu-id="c334b-110">**新的-AzureStorageFileSASToken** Cmdlet 會針對 Azure 儲存空間檔產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c334b-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="c334b-111">示例</span><span class="sxs-lookup"><span data-stu-id="c334b-111">EXAMPLES</span></span>

### <span data-ttu-id="c334b-112">範例1：產生具有完整檔案許可權的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="c334b-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="c334b-113">這個命令會產生擁有名為 FilePath 之檔案之完整許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c334b-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="c334b-114">範例2：產生具有時間限制的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="c334b-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="c334b-115">第一個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="c334b-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="c334b-116">該命令會將目前的時間儲存在 $StartTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="c334b-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="c334b-117">第二個命令會將兩個小時加到 $StartTime 中的物件，然後將結果儲存在 $EndTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="c334b-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="c334b-118">此物件是在未來兩個小時的時間。</span><span class="sxs-lookup"><span data-stu-id="c334b-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="c334b-119">第三個命令會產生擁有指定許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="c334b-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="c334b-120">此權杖會在目前的時間生效。</span><span class="sxs-lookup"><span data-stu-id="c334b-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="c334b-121">權杖在 $EndTime 中儲存的時間之前一直保持有效。</span><span class="sxs-lookup"><span data-stu-id="c334b-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="c334b-122">參數</span><span class="sxs-lookup"><span data-stu-id="c334b-122">PARAMETERS</span></span>

### <span data-ttu-id="c334b-123">-內容</span><span class="sxs-lookup"><span data-stu-id="c334b-123">-Context</span></span>
<span data-ttu-id="c334b-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c334b-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c334b-125">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c334b-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c334b-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c334b-126">-ExpiryTime</span></span>
<span data-ttu-id="c334b-127">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="c334b-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c334b-128">檔案</span><span class="sxs-lookup"><span data-stu-id="c334b-128">-File</span></span>
<span data-ttu-id="c334b-129">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="c334b-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c334b-130">您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="c334b-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="c334b-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c334b-131">-FullUri</span></span>
<span data-ttu-id="c334b-132">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="c334b-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c334b-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c334b-133">-IPAddressOrRange</span></span>
<span data-ttu-id="c334b-134">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="c334b-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c334b-135">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="c334b-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="c334b-136">-Path</span><span class="sxs-lookup"><span data-stu-id="c334b-136">-Path</span></span>
<span data-ttu-id="c334b-137">指定檔案相對於儲存區共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="c334b-137">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="c334b-138">-許可權</span><span class="sxs-lookup"><span data-stu-id="c334b-138">-Permission</span></span>
<span data-ttu-id="c334b-139">指定儲存空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="c334b-139">Specifies the permissions for a Storage file.</span></span>

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

### <span data-ttu-id="c334b-140">-原則</span><span class="sxs-lookup"><span data-stu-id="c334b-140">-Policy</span></span>
<span data-ttu-id="c334b-141">指定檔案的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="c334b-141">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="c334b-142">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="c334b-142">-Protocol</span></span>
<span data-ttu-id="c334b-143">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="c334b-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c334b-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c334b-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c334b-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c334b-145">HttpsOnly</span></span>
* <span data-ttu-id="c334b-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="c334b-146">HttpsOrHttp</span></span>

<span data-ttu-id="c334b-147">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="c334b-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c334b-148">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="c334b-148">-ShareName</span></span>
<span data-ttu-id="c334b-149">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="c334b-149">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="c334b-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c334b-150">-StartTime</span></span>
<span data-ttu-id="c334b-151">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="c334b-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c334b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c334b-152">CommonParameters</span></span>
<span data-ttu-id="c334b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c334b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c334b-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c334b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c334b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="c334b-155">INPUTS</span></span>

## <span data-ttu-id="c334b-156">輸出</span><span class="sxs-lookup"><span data-stu-id="c334b-156">OUTPUTS</span></span>

## <span data-ttu-id="c334b-157">筆記</span><span class="sxs-lookup"><span data-stu-id="c334b-157">NOTES</span></span>

## <span data-ttu-id="c334b-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="c334b-158">RELATED LINKS</span></span>

[<span data-ttu-id="c334b-159">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c334b-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c334b-160">新-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c334b-160">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
