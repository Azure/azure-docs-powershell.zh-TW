---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: b55ab1d87fa63523b35077243d8b9b4f00ba5d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915042"
---
# <span data-ttu-id="bbcba-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="bbcba-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="bbcba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bbcba-102">SYNOPSIS</span></span>
<span data-ttu-id="bbcba-103">產生 Azure 儲存空間共用的共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="bbcba-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="bbcba-104">語法</span><span class="sxs-lookup"><span data-stu-id="bbcba-104">SYNTAX</span></span>

### <span data-ttu-id="bbcba-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="bbcba-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbcba-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="bbcba-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbcba-107">描述</span><span class="sxs-lookup"><span data-stu-id="bbcba-107">DESCRIPTION</span></span>
<span data-ttu-id="bbcba-108">**New-AzStorageShareSASToken Cmdlet** 會為 Azure 儲存空間共用產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="bbcba-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="bbcba-109">例子</span><span class="sxs-lookup"><span data-stu-id="bbcba-109">EXAMPLES</span></span>

### <span data-ttu-id="bbcba-110">範例 1：產生共用共用的共用存取簽章權杖</span><span class="sxs-lookup"><span data-stu-id="bbcba-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="bbcba-111">此命令會為名為 ContosoShare 的共用建立共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="bbcba-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="bbcba-112">範例 2：使用管線產生多個共用存取簽章權杖</span><span class="sxs-lookup"><span data-stu-id="bbcba-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="bbcba-113">此命令會獲得符合首碼測試的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="bbcba-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="bbcba-114">該命令會使用管線運算子，將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbcba-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bbcba-115">目前的 Cmdlet 會為每個具有指定許可權的儲存空間共用建立共用存取權杖。</span><span class="sxs-lookup"><span data-stu-id="bbcba-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="bbcba-116">範例 3：產生使用共用存取策略的共用存取簽章權杖</span><span class="sxs-lookup"><span data-stu-id="bbcba-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="bbcba-117">此命令會為名為 ContosoShare 的儲存空間共用建立共用存取簽章權杖，該共用共用具有名為 ContosoPolicy03 的策略。</span><span class="sxs-lookup"><span data-stu-id="bbcba-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="bbcba-118">參數</span><span class="sxs-lookup"><span data-stu-id="bbcba-118">PARAMETERS</span></span>

### <span data-ttu-id="bbcba-119">-內容</span><span class="sxs-lookup"><span data-stu-id="bbcba-119">-Context</span></span>
<span data-ttu-id="bbcba-120">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="bbcba-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="bbcba-121">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbcba-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbcba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbcba-122">-DefaultProfile</span></span>
<span data-ttu-id="bbcba-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbcba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbcba-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bbcba-124">-ExpiryTime</span></span>
<span data-ttu-id="bbcba-125">指定共用存取簽章變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="bbcba-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="bbcba-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="bbcba-126">-FullUri</span></span>
<span data-ttu-id="bbcba-127">表示此 Cmdlet 會返回完整的 Blob URI 和共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="bbcba-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="bbcba-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bbcba-128">-IPAddressOrRange</span></span>
<span data-ttu-id="bbcba-129">指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。</span><span class="sxs-lookup"><span data-stu-id="bbcba-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="bbcba-130">此範圍包含。</span><span class="sxs-lookup"><span data-stu-id="bbcba-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="bbcba-131">-許可權</span><span class="sxs-lookup"><span data-stu-id="bbcba-131">-Permission</span></span>
<span data-ttu-id="bbcba-132">指定權杖中存取共用和共用下檔案的許可權。</span><span class="sxs-lookup"><span data-stu-id="bbcba-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="bbcba-133">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="bbcba-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbcba-134">-策略</span><span class="sxs-lookup"><span data-stu-id="bbcba-134">-Policy</span></span>
<span data-ttu-id="bbcba-135">指定共用儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="bbcba-135">Specifies the stored access policy for a share.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbcba-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="bbcba-136">-Protocol</span></span>
<span data-ttu-id="bbcba-137">指定要求允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bbcba-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="bbcba-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bbcba-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="bbcba-139">HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="bbcba-139">HttpsOnly</span></span>
* <span data-ttu-id="bbcba-140">HTTPsOrHttp 預設值為 HTTPsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="bbcba-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="bbcba-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bbcba-141">-ShareName</span></span>
<span data-ttu-id="bbcba-142">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbcba-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbcba-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bbcba-143">-StartTime</span></span>
<span data-ttu-id="bbcba-144">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="bbcba-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="bbcba-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbcba-145">CommonParameters</span></span>
<span data-ttu-id="bbcba-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bbcba-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbcba-147">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bbcba-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbcba-148">輸入</span><span class="sxs-lookup"><span data-stu-id="bbcba-148">INPUTS</span></span>

### <span data-ttu-id="bbcba-149">System.String</span><span class="sxs-lookup"><span data-stu-id="bbcba-149">System.String</span></span>

### <span data-ttu-id="bbcba-150">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="bbcba-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bbcba-151">輸出</span><span class="sxs-lookup"><span data-stu-id="bbcba-151">OUTPUTS</span></span>

### <span data-ttu-id="bbcba-152">System.String</span><span class="sxs-lookup"><span data-stu-id="bbcba-152">System.String</span></span>

## <span data-ttu-id="bbcba-153">筆記</span><span class="sxs-lookup"><span data-stu-id="bbcba-153">NOTES</span></span>
* <span data-ttu-id="bbcba-154">關鍵字：常見、azure、服務、資料、儲存、Blob、佇列、表格</span><span class="sxs-lookup"><span data-stu-id="bbcba-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="bbcba-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbcba-155">RELATED LINKS</span></span>

[<span data-ttu-id="bbcba-156">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="bbcba-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="bbcba-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="bbcba-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
