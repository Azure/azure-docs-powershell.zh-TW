---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragefilesastoken
schema: 2.0.0
ms.openlocfilehash: 7c1b29cdb420ed0af4be8ce8ff07c73db179cabe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800602"
---
# <span data-ttu-id="ba8f1-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="ba8f1-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="ba8f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8f1-103">產生儲存空間的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba8f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba8f1-104">SYNTAX</span></span>

### <span data-ttu-id="ba8f1-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="ba8f1-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba8f1-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="ba8f1-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba8f1-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="ba8f1-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8f1-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="ba8f1-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8f1-109">說明</span><span class="sxs-lookup"><span data-stu-id="ba8f1-109">DESCRIPTION</span></span>
<span data-ttu-id="ba8f1-110">**新的-AzureStorageFileSASToken** Cmdlet 會針對 Azure 儲存空間檔產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="ba8f1-111">示例</span><span class="sxs-lookup"><span data-stu-id="ba8f1-111">EXAMPLES</span></span>

### <span data-ttu-id="ba8f1-112">範例1：產生具有完整檔案許可權的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="ba8f1-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="ba8f1-113">這個命令會產生擁有名為 FilePath 之檔案之完整許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="ba8f1-114">範例2：產生具有時間限制的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="ba8f1-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="ba8f1-115">第一個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="ba8f1-116">該命令會將目前的時間儲存在 $StartTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="ba8f1-117">第二個命令會將兩個小時加到 $StartTime 中的物件，然後將結果儲存在 $EndTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="ba8f1-118">此物件是在未來兩個小時的時間。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="ba8f1-119">第三個命令會產生擁有指定許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="ba8f1-120">此權杖會在目前的時間生效。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="ba8f1-121">權杖在 $EndTime 中儲存的時間之前一直保持有效。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="ba8f1-122">參數</span><span class="sxs-lookup"><span data-stu-id="ba8f1-122">PARAMETERS</span></span>

### <span data-ttu-id="ba8f1-123">-內容</span><span class="sxs-lookup"><span data-stu-id="ba8f1-123">-Context</span></span>
<span data-ttu-id="ba8f1-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ba8f1-125">若要取得內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8f1-126">-DefaultProfile</span></span>
<span data-ttu-id="ba8f1-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba8f1-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ba8f1-128">-ExpiryTime</span></span>
<span data-ttu-id="ba8f1-129">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-130">檔案</span><span class="sxs-lookup"><span data-stu-id="ba8f1-130">-File</span></span>
<span data-ttu-id="ba8f1-131">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ba8f1-132">您可以使用 Get-AzureStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ba8f1-133">-FullUri</span></span>
<span data-ttu-id="ba8f1-134">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ba8f1-135">-IPAddressOrRange</span></span>
<span data-ttu-id="ba8f1-136">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ba8f1-137">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="ba8f1-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ba8f1-138">-Path</span></span>
<span data-ttu-id="ba8f1-139">指定檔案相對於儲存區共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-140">-許可權</span><span class="sxs-lookup"><span data-stu-id="ba8f1-140">-Permission</span></span>
<span data-ttu-id="ba8f1-141">指定儲存空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="ba8f1-142">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-143">-原則</span><span class="sxs-lookup"><span data-stu-id="ba8f1-143">-Policy</span></span>
<span data-ttu-id="ba8f1-144">指定檔案的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-145">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ba8f1-145">-Protocol</span></span>
<span data-ttu-id="ba8f1-146">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ba8f1-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ba8f1-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ba8f1-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ba8f1-148">HttpsOnly</span></span>
* <span data-ttu-id="ba8f1-149">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-150">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="ba8f1-150">-ShareName</span></span>
<span data-ttu-id="ba8f1-151">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ba8f1-152">-StartTime</span></span>
<span data-ttu-id="ba8f1-153">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-153">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8f1-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8f1-154">CommonParameters</span></span>
<span data-ttu-id="ba8f1-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8f1-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba8f1-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8f1-157">輸入</span><span class="sxs-lookup"><span data-stu-id="ba8f1-157">INPUTS</span></span>

### <span data-ttu-id="ba8f1-158">System.object</span><span class="sxs-lookup"><span data-stu-id="ba8f1-158">System.String</span></span>

### <span data-ttu-id="ba8f1-159">[WindowsAzure] CloudFile</span><span class="sxs-lookup"><span data-stu-id="ba8f1-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ba8f1-160">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ba8f1-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>
<span data-ttu-id="ba8f1-161">參數：內容 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ba8f1-161">Parameters: Context (ByValue)</span></span>

## <span data-ttu-id="ba8f1-162">輸出</span><span class="sxs-lookup"><span data-stu-id="ba8f1-162">OUTPUTS</span></span>

### <span data-ttu-id="ba8f1-163">System.object</span><span class="sxs-lookup"><span data-stu-id="ba8f1-163">System.String</span></span>

## <span data-ttu-id="ba8f1-164">筆記</span><span class="sxs-lookup"><span data-stu-id="ba8f1-164">NOTES</span></span>

## <span data-ttu-id="ba8f1-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba8f1-165">RELATED LINKS</span></span>

[<span data-ttu-id="ba8f1-166">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ba8f1-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ba8f1-167">新-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="ba8f1-167">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
