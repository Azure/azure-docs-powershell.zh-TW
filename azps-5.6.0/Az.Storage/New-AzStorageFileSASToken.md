---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: ec5f290a6c45725dfed369058d5e00bbee016f9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915066"
---
# <span data-ttu-id="00228-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="00228-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="00228-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00228-102">SYNOPSIS</span></span>
<span data-ttu-id="00228-103">產生儲存檔案的共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="00228-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="00228-104">語法</span><span class="sxs-lookup"><span data-stu-id="00228-104">SYNTAX</span></span>

### <span data-ttu-id="00228-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="00228-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00228-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="00228-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00228-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="00228-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00228-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="00228-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00228-109">描述</span><span class="sxs-lookup"><span data-stu-id="00228-109">DESCRIPTION</span></span>
<span data-ttu-id="00228-110">**New-AzStorageFileSASToken** Cmdlet 會產生 Azure 儲存體檔案的共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="00228-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="00228-111">例子</span><span class="sxs-lookup"><span data-stu-id="00228-111">EXAMPLES</span></span>

### <span data-ttu-id="00228-112">範例 1：產生具有完整檔案許可權的共用存取簽章權杖</span><span class="sxs-lookup"><span data-stu-id="00228-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="00228-113">此命令會產生具有 FilePath 檔案完整許可權的共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="00228-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="00228-114">範例 2：產生具有時間限制的共用存取簽章權杖</span><span class="sxs-lookup"><span data-stu-id="00228-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="00228-115">第一個命令會使用 Cmdlet 建立 **DateTime** Get-Date物件。</span><span class="sxs-lookup"><span data-stu-id="00228-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="00228-116">命令會儲存目前的時間$StartTime變數。</span><span class="sxs-lookup"><span data-stu-id="00228-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="00228-117">第二個命令會將兩小時加到 $StartTime 中的物件，然後將結果儲存在$EndTime變數中。</span><span class="sxs-lookup"><span data-stu-id="00228-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="00228-118">此物件在未來兩小時的時間。</span><span class="sxs-lookup"><span data-stu-id="00228-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="00228-119">第三個命令會產生具有指定許可權的共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="00228-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="00228-120">此權杖目前生效。</span><span class="sxs-lookup"><span data-stu-id="00228-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="00228-121">權杖在儲存于 $EndTime 之前$EndTime。</span><span class="sxs-lookup"><span data-stu-id="00228-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="00228-122">參數</span><span class="sxs-lookup"><span data-stu-id="00228-122">PARAMETERS</span></span>

### <span data-ttu-id="00228-123">-內容</span><span class="sxs-lookup"><span data-stu-id="00228-123">-Context</span></span>
<span data-ttu-id="00228-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="00228-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="00228-125">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00228-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="00228-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00228-126">-DefaultProfile</span></span>
<span data-ttu-id="00228-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00228-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00228-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="00228-128">-ExpiryTime</span></span>
<span data-ttu-id="00228-129">指定共用存取簽章變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="00228-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="00228-130">-檔案</span><span class="sxs-lookup"><span data-stu-id="00228-130">-File</span></span>
<span data-ttu-id="00228-131">指定 **CloudFile** 物件。</span><span class="sxs-lookup"><span data-stu-id="00228-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="00228-132">您可以使用 Cmdlet 建立雲端檔案，或取得Get-AzStorageFile檔案。</span><span class="sxs-lookup"><span data-stu-id="00228-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00228-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="00228-133">-FullUri</span></span>
<span data-ttu-id="00228-134">表示此 Cmdlet 會返回完整的 Blob URI 和共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="00228-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="00228-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="00228-135">-IPAddressOrRange</span></span>
<span data-ttu-id="00228-136">指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。</span><span class="sxs-lookup"><span data-stu-id="00228-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="00228-137">此範圍包含。</span><span class="sxs-lookup"><span data-stu-id="00228-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="00228-138">-路徑</span><span class="sxs-lookup"><span data-stu-id="00228-138">-Path</span></span>
<span data-ttu-id="00228-139">指定檔案相對於儲存空間共用的路徑。</span><span class="sxs-lookup"><span data-stu-id="00228-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="00228-140">-許可權</span><span class="sxs-lookup"><span data-stu-id="00228-140">-Permission</span></span>
<span data-ttu-id="00228-141">指定儲存空間檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="00228-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="00228-142">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="00228-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="00228-143">-策略</span><span class="sxs-lookup"><span data-stu-id="00228-143">-Policy</span></span>
<span data-ttu-id="00228-144">指定檔案的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="00228-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="00228-145">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="00228-145">-Protocol</span></span>
<span data-ttu-id="00228-146">指定要求允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="00228-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="00228-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="00228-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="00228-148">HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="00228-148">HttpsOnly</span></span>
* <span data-ttu-id="00228-149">HTTPsOrHttp 預設值為 HTTPsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="00228-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00228-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="00228-150">-ShareName</span></span>
<span data-ttu-id="00228-151">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="00228-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="00228-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="00228-152">-StartTime</span></span>
<span data-ttu-id="00228-153">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="00228-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="00228-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00228-154">CommonParameters</span></span>
<span data-ttu-id="00228-155">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00228-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00228-156">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00228-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00228-157">輸入</span><span class="sxs-lookup"><span data-stu-id="00228-157">INPUTS</span></span>

### <span data-ttu-id="00228-158">System.String</span><span class="sxs-lookup"><span data-stu-id="00228-158">System.String</span></span>

### <span data-ttu-id="00228-159">Microsoft.Azure.storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="00228-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="00228-160">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="00228-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="00228-161">輸出</span><span class="sxs-lookup"><span data-stu-id="00228-161">OUTPUTS</span></span>

### <span data-ttu-id="00228-162">System.String</span><span class="sxs-lookup"><span data-stu-id="00228-162">System.String</span></span>

## <span data-ttu-id="00228-163">筆記</span><span class="sxs-lookup"><span data-stu-id="00228-163">NOTES</span></span>

## <span data-ttu-id="00228-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="00228-164">RELATED LINKS</span></span>

[<span data-ttu-id="00228-165">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="00228-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="00228-166">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="00228-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
