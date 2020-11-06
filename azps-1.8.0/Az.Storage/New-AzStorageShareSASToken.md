---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 0fc159773b54e8eba39fc3fe5ca45a2559c1521c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614542"
---
# <span data-ttu-id="39a40-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="39a40-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="39a40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39a40-102">SYNOPSIS</span></span>
<span data-ttu-id="39a40-103">產生 Azure 儲存空間共用的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="39a40-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="39a40-104">句法</span><span class="sxs-lookup"><span data-stu-id="39a40-104">SYNTAX</span></span>

### <span data-ttu-id="39a40-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="39a40-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39a40-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="39a40-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39a40-107">說明</span><span class="sxs-lookup"><span data-stu-id="39a40-107">DESCRIPTION</span></span>
<span data-ttu-id="39a40-108">**新的-AzStorageShareSASToken** Cmdlet 會針對 Azure 儲存空間共用產生共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="39a40-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="39a40-109">示例</span><span class="sxs-lookup"><span data-stu-id="39a40-109">EXAMPLES</span></span>

### <span data-ttu-id="39a40-110">範例1：為共用產生共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="39a40-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="39a40-111">這個命令會建立名為 ContosoShare 的共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="39a40-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="39a40-112">範例2：使用管線產生多個共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="39a40-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="39a40-113">這個命令會取得符合前置詞測試的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="39a40-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="39a40-114">命令會使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39a40-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="39a40-115">目前的 Cmdlet 會為具有指定許可權的每個儲存空間共用建立共用存取權杖。</span><span class="sxs-lookup"><span data-stu-id="39a40-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="39a40-116">範例3：產生使用共用存取原則的共用存取簽名權杖</span><span class="sxs-lookup"><span data-stu-id="39a40-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="39a40-117">這個命令會為擁有名為 ContosoPolicy03 原則之名為 ContosoShare 的儲存空間共用建立共用存取簽名權杖。</span><span class="sxs-lookup"><span data-stu-id="39a40-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="39a40-118">參數</span><span class="sxs-lookup"><span data-stu-id="39a40-118">PARAMETERS</span></span>

### <span data-ttu-id="39a40-119">-內容</span><span class="sxs-lookup"><span data-stu-id="39a40-119">-Context</span></span>
<span data-ttu-id="39a40-120">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="39a40-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="39a40-121">若要取得內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39a40-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="39a40-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a40-122">-DefaultProfile</span></span>
<span data-ttu-id="39a40-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39a40-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a40-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="39a40-124">-ExpiryTime</span></span>
<span data-ttu-id="39a40-125">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="39a40-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="39a40-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="39a40-126">-FullUri</span></span>
<span data-ttu-id="39a40-127">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="39a40-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="39a40-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="39a40-128">-IPAddressOrRange</span></span>
<span data-ttu-id="39a40-129">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="39a40-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="39a40-130">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="39a40-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="39a40-131">-許可權</span><span class="sxs-lookup"><span data-stu-id="39a40-131">-Permission</span></span>
<span data-ttu-id="39a40-132">指定權杖中的許可權，以存取共用中的共用和檔案。</span><span class="sxs-lookup"><span data-stu-id="39a40-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="39a40-133">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="39a40-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="39a40-134">-原則</span><span class="sxs-lookup"><span data-stu-id="39a40-134">-Policy</span></span>
<span data-ttu-id="39a40-135">指定共用的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="39a40-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="39a40-136">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="39a40-136">-Protocol</span></span>
<span data-ttu-id="39a40-137">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="39a40-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="39a40-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="39a40-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="39a40-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="39a40-139">HttpsOnly</span></span>
* <span data-ttu-id="39a40-140">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="39a40-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="39a40-141">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="39a40-141">-ShareName</span></span>
<span data-ttu-id="39a40-142">指定儲存空間共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="39a40-142">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="39a40-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="39a40-143">-StartTime</span></span>
<span data-ttu-id="39a40-144">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="39a40-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="39a40-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a40-145">CommonParameters</span></span>
<span data-ttu-id="39a40-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39a40-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a40-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39a40-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a40-148">輸入</span><span class="sxs-lookup"><span data-stu-id="39a40-148">INPUTS</span></span>

### <span data-ttu-id="39a40-149">System.object</span><span class="sxs-lookup"><span data-stu-id="39a40-149">System.String</span></span>

### <span data-ttu-id="39a40-150">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="39a40-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="39a40-151">輸出</span><span class="sxs-lookup"><span data-stu-id="39a40-151">OUTPUTS</span></span>

### <span data-ttu-id="39a40-152">System.object</span><span class="sxs-lookup"><span data-stu-id="39a40-152">System.String</span></span>

## <span data-ttu-id="39a40-153">筆記</span><span class="sxs-lookup"><span data-stu-id="39a40-153">NOTES</span></span>
* <span data-ttu-id="39a40-154">關鍵字：常見、azure、services、data、storage、blob、queue、table</span><span class="sxs-lookup"><span data-stu-id="39a40-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="39a40-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="39a40-155">RELATED LINKS</span></span>

[<span data-ttu-id="39a40-156">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="39a40-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="39a40-157">新-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="39a40-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
