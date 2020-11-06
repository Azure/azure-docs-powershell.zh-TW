---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: 7bb5f376953a378eadc2dee6b061ba3f876cfdf4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614550"
---
# <span data-ttu-id="8529d-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="8529d-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="8529d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8529d-102">SYNOPSIS</span></span>
<span data-ttu-id="8529d-103">產生儲存空間的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="8529d-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="8529d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8529d-104">SYNTAX</span></span>

### <span data-ttu-id="8529d-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="8529d-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8529d-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="8529d-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8529d-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="8529d-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8529d-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="8529d-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8529d-109">說明</span><span class="sxs-lookup"><span data-stu-id="8529d-109">DESCRIPTION</span></span>
<span data-ttu-id="8529d-110">**新的-AzStorageFileSASToken** Cmdlet 會針對 Azure 儲存空間檔產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="8529d-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="8529d-111">示例</span><span class="sxs-lookup"><span data-stu-id="8529d-111">EXAMPLES</span></span>

### <span data-ttu-id="8529d-112">範例1：產生具有完整檔案許可權的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="8529d-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="8529d-113">這個命令會產生擁有名為 FilePath 之檔案之完整許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="8529d-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="8529d-114">範例2：產生具有時間限制的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="8529d-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="8529d-115">第一個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="8529d-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="8529d-116">該命令會將目前的時間儲存在 $StartTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="8529d-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="8529d-117">第二個命令會將兩個小時加到 $StartTime 中的物件，然後將結果儲存在 $EndTime 變數中。</span><span class="sxs-lookup"><span data-stu-id="8529d-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="8529d-118">此物件是在未來兩個小時的時間。</span><span class="sxs-lookup"><span data-stu-id="8529d-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="8529d-119">第三個命令會產生擁有指定許可權的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="8529d-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="8529d-120">此權杖會在目前的時間生效。</span><span class="sxs-lookup"><span data-stu-id="8529d-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="8529d-121">權杖在 $EndTime 中儲存的時間之前一直保持有效。</span><span class="sxs-lookup"><span data-stu-id="8529d-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="8529d-122">參數</span><span class="sxs-lookup"><span data-stu-id="8529d-122">PARAMETERS</span></span>

### <span data-ttu-id="8529d-123">-內容</span><span class="sxs-lookup"><span data-stu-id="8529d-123">-Context</span></span>
<span data-ttu-id="8529d-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8529d-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="8529d-125">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8529d-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8529d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8529d-126">-DefaultProfile</span></span>
<span data-ttu-id="8529d-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8529d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8529d-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8529d-128">-ExpiryTime</span></span>
<span data-ttu-id="8529d-129">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="8529d-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="8529d-130">檔案</span><span class="sxs-lookup"><span data-stu-id="8529d-130">-File</span></span>
<span data-ttu-id="8529d-131">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="8529d-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="8529d-132">您可以使用 Get-AzStorageFile Cmdlet 來建立雲端檔案或取得一個雲端檔案。</span><span class="sxs-lookup"><span data-stu-id="8529d-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="8529d-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8529d-133">-FullUri</span></span>
<span data-ttu-id="8529d-134">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="8529d-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="8529d-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8529d-135">-IPAddressOrRange</span></span>
<span data-ttu-id="8529d-136">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="8529d-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8529d-137">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="8529d-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="8529d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="8529d-138">-Path</span></span>
<span data-ttu-id="8529d-139">指定檔案相對於儲存區共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="8529d-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="8529d-140">-許可權</span><span class="sxs-lookup"><span data-stu-id="8529d-140">-Permission</span></span>
<span data-ttu-id="8529d-141">指定儲存空間的許可權。</span><span class="sxs-lookup"><span data-stu-id="8529d-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="8529d-142">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="8529d-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8529d-143">-原則</span><span class="sxs-lookup"><span data-stu-id="8529d-143">-Policy</span></span>
<span data-ttu-id="8529d-144">指定檔案的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="8529d-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="8529d-145">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="8529d-145">-Protocol</span></span>
<span data-ttu-id="8529d-146">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="8529d-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8529d-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8529d-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8529d-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8529d-148">HttpsOnly</span></span>
* <span data-ttu-id="8529d-149">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="8529d-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="8529d-150">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="8529d-150">-ShareName</span></span>
<span data-ttu-id="8529d-151">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="8529d-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="8529d-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8529d-152">-StartTime</span></span>
<span data-ttu-id="8529d-153">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="8529d-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="8529d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8529d-154">CommonParameters</span></span>
<span data-ttu-id="8529d-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8529d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8529d-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8529d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8529d-157">輸入</span><span class="sxs-lookup"><span data-stu-id="8529d-157">INPUTS</span></span>

### <span data-ttu-id="8529d-158">System.object</span><span class="sxs-lookup"><span data-stu-id="8529d-158">System.String</span></span>

### <span data-ttu-id="8529d-159">[WindowsAzure] CloudFile</span><span class="sxs-lookup"><span data-stu-id="8529d-159">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="8529d-160">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="8529d-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8529d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="8529d-161">OUTPUTS</span></span>

### <span data-ttu-id="8529d-162">System.object</span><span class="sxs-lookup"><span data-stu-id="8529d-162">System.String</span></span>

## <span data-ttu-id="8529d-163">筆記</span><span class="sxs-lookup"><span data-stu-id="8529d-163">NOTES</span></span>

## <span data-ttu-id="8529d-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="8529d-164">RELATED LINKS</span></span>

[<span data-ttu-id="8529d-165">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8529d-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="8529d-166">新-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="8529d-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
