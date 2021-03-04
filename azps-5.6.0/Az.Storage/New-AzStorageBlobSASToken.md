---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 1dbe66bd8c34cb653fe17d01b19a2eca1b23c479
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915094"
---
# <span data-ttu-id="2806d-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2806d-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="2806d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2806d-102">SYNOPSIS</span></span>
<span data-ttu-id="2806d-103">產生 Azure 儲存 Blob 的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="2806d-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="2806d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2806d-104">SYNTAX</span></span>

### <span data-ttu-id="2806d-105">BlobNameWithPermission (預設) </span><span class="sxs-lookup"><span data-stu-id="2806d-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2806d-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="2806d-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2806d-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="2806d-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2806d-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="2806d-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2806d-109">描述</span><span class="sxs-lookup"><span data-stu-id="2806d-109">DESCRIPTION</span></span>
<span data-ttu-id="2806d-110">**New-AzStorageBlobSAsToken Cmdlet** 會為 Azure 儲存 blob 產生共用存取簽名 (SAS) 權杖。</span><span class="sxs-lookup"><span data-stu-id="2806d-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="2806d-111">例子</span><span class="sxs-lookup"><span data-stu-id="2806d-111">EXAMPLES</span></span>

### <span data-ttu-id="2806d-112">範例 1：產生具有完整 Blob 許可權的 Blob SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="2806d-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="2806d-113">此範例會產生具有完整 Blob 許可權的 Blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="2806d-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="2806d-114">範例 2：使用生命週期時間產生 Blob SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="2806d-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="2806d-115">此範例會產生具有生命週期的 Blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="2806d-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="2806d-116">範例 3：根據 OAuth 驗證產生具有儲存內容的使用者身分識別 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="2806d-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="2806d-117">此範例會根據 OAuth 驗證產生具有儲存內容的使用者身分識別 Blob SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="2806d-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="2806d-118">參數</span><span class="sxs-lookup"><span data-stu-id="2806d-118">PARAMETERS</span></span>

### <span data-ttu-id="2806d-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="2806d-119">-Blob</span></span>
<span data-ttu-id="2806d-120">指定儲存 Blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="2806d-120">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="2806d-121">-BlobBaseClient</span></span>
<span data-ttu-id="2806d-122">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="2806d-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2806d-123">-CloudBlob</span></span>
<span data-ttu-id="2806d-124">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="2806d-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="2806d-125">若要取得 **CloudBlob 物件** ，請使用 [Get-AzStorageBlob](./Get-AzStorageBlob.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2806d-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-126">-Container</span><span class="sxs-lookup"><span data-stu-id="2806d-126">-Container</span></span>
<span data-ttu-id="2806d-127">指定儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="2806d-127">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-128">-內容</span><span class="sxs-lookup"><span data-stu-id="2806d-128">-Context</span></span>
<span data-ttu-id="2806d-129">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2806d-129">Specifies the storage context.</span></span>
<span data-ttu-id="2806d-130">當儲存內容是以 OAuth 驗證為基礎時，會產生使用者身分識別 Blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="2806d-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="2806d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2806d-131">-DefaultProfile</span></span>
<span data-ttu-id="2806d-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2806d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2806d-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2806d-133">-ExpiryTime</span></span>
<span data-ttu-id="2806d-134">指定共用存取簽章到期的時間。</span><span class="sxs-lookup"><span data-stu-id="2806d-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="2806d-135">當儲存內容是以 OAuth 驗證為基礎時，過期時間必須在目前時間之後 7 天內，而且不能早于目前時間。</span><span class="sxs-lookup"><span data-stu-id="2806d-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="2806d-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2806d-136">-FullUri</span></span>
<span data-ttu-id="2806d-137">表示此 Cmdlet 會返回完整的 Blob URI 和共用存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="2806d-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="2806d-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2806d-138">-IPAddressOrRange</span></span>
<span data-ttu-id="2806d-139">指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。</span><span class="sxs-lookup"><span data-stu-id="2806d-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2806d-140">此範圍包含。</span><span class="sxs-lookup"><span data-stu-id="2806d-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="2806d-141">-許可權</span><span class="sxs-lookup"><span data-stu-id="2806d-141">-Permission</span></span>
<span data-ttu-id="2806d-142">指定儲存 Blob 的許可權。</span><span class="sxs-lookup"><span data-stu-id="2806d-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="2806d-143">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="2806d-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-144">-策略</span><span class="sxs-lookup"><span data-stu-id="2806d-144">-Policy</span></span>
<span data-ttu-id="2806d-145">指定 Azure 儲存的 Access 策略。</span><span class="sxs-lookup"><span data-stu-id="2806d-145">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-146">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="2806d-146">-Protocol</span></span>
<span data-ttu-id="2806d-147">指定要求允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="2806d-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2806d-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2806d-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2806d-149">HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="2806d-149">HttpsOnly</span></span>
* <span data-ttu-id="2806d-150">HTTPsOrHttp 預設值為 HTTPsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="2806d-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="2806d-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2806d-151">-StartTime</span></span>
<span data-ttu-id="2806d-152">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="2806d-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="2806d-153">-確認</span><span class="sxs-lookup"><span data-stu-id="2806d-153">-Confirm</span></span>
<span data-ttu-id="2806d-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2806d-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2806d-155">-WhatIf</span></span>
<span data-ttu-id="2806d-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2806d-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2806d-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2806d-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2806d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2806d-158">CommonParameters</span></span>
<span data-ttu-id="2806d-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2806d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2806d-160">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2806d-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2806d-161">輸入</span><span class="sxs-lookup"><span data-stu-id="2806d-161">INPUTS</span></span>

### <span data-ttu-id="2806d-162">Microsoft.Azure.storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2806d-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2806d-163">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2806d-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2806d-164">輸出</span><span class="sxs-lookup"><span data-stu-id="2806d-164">OUTPUTS</span></span>

### <span data-ttu-id="2806d-165">System.String</span><span class="sxs-lookup"><span data-stu-id="2806d-165">System.String</span></span>

## <span data-ttu-id="2806d-166">筆記</span><span class="sxs-lookup"><span data-stu-id="2806d-166">NOTES</span></span>

## <span data-ttu-id="2806d-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="2806d-167">RELATED LINKS</span></span>

[<span data-ttu-id="2806d-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2806d-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2806d-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2806d-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
