---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138619"
---
# <span data-ttu-id="ca7b7-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ca7b7-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="ca7b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7b7-103">針對 Azure 儲存區 blob 產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="ca7b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca7b7-104">SYNTAX</span></span>

### <span data-ttu-id="ca7b7-105">BlobNameWithPermission (預設) </span><span class="sxs-lookup"><span data-stu-id="ca7b7-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7b7-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="ca7b7-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7b7-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="ca7b7-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7b7-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="ca7b7-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca7b7-109">說明</span><span class="sxs-lookup"><span data-stu-id="ca7b7-109">DESCRIPTION</span></span>
<span data-ttu-id="ca7b7-110">**AzStorageBlobSASToken** Cmdlet 會針對 Azure 儲存區 blob 產生 (SAS) 權杖的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="ca7b7-111">示例</span><span class="sxs-lookup"><span data-stu-id="ca7b7-111">EXAMPLES</span></span>

### <span data-ttu-id="ca7b7-112">範例1：使用完整 blob 許可權產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="ca7b7-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="ca7b7-113">這個範例會產生含完整 blob 許可權的 blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="ca7b7-114">範例2：使用生命時間產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="ca7b7-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="ca7b7-115">這個範例會產生含生命時間的 blob SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="ca7b7-116">範例3：根據 OAuth 驗證產生含儲存內容的使用者身分識別 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="ca7b7-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="ca7b7-117">這個範例會根據 OAuth 驗證產生一個含儲存內容的使用者身分識別 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="ca7b7-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="ca7b7-118">參數</span><span class="sxs-lookup"><span data-stu-id="ca7b7-118">PARAMETERS</span></span>

### <span data-ttu-id="ca7b7-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="ca7b7-119">-Blob</span></span>
<span data-ttu-id="ca7b7-120">指定儲存區 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="ca7b7-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ca7b7-121">-BlobBaseClient</span></span>
<span data-ttu-id="ca7b7-122">BlobBaseClient 物件</span><span class="sxs-lookup"><span data-stu-id="ca7b7-122">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="ca7b7-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ca7b7-123">-CloudBlob</span></span>
<span data-ttu-id="ca7b7-124">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="ca7b7-125">若要取得 **CloudBlob** 物件，請使用 [AzStorageBlob](./Get-AzStorageBlob.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="ca7b7-126">-容器</span><span class="sxs-lookup"><span data-stu-id="ca7b7-126">-Container</span></span>
<span data-ttu-id="ca7b7-127">指定儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="ca7b7-128">-內容</span><span class="sxs-lookup"><span data-stu-id="ca7b7-128">-Context</span></span>
<span data-ttu-id="ca7b7-129">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-129">Specifies the storage context.</span></span>
<span data-ttu-id="ca7b7-130">當儲存內容是以 OAuth 驗證為基礎時，會產生使用者身分識別 blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="ca7b7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7b7-131">-DefaultProfile</span></span>
<span data-ttu-id="ca7b7-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca7b7-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca7b7-133">-ExpiryTime</span></span>
<span data-ttu-id="ca7b7-134">指定共用存取簽章的到期時間。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="ca7b7-135">當儲存內容是以 OAuth 驗證為基礎時，到期時間必須是與目前時間的7天，且不得早于目前時間。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="ca7b7-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ca7b7-136">-FullUri</span></span>
<span data-ttu-id="ca7b7-137">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ca7b7-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ca7b7-138">-IPAddressOrRange</span></span>
<span data-ttu-id="ca7b7-139">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ca7b7-140">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="ca7b7-141">-許可權</span><span class="sxs-lookup"><span data-stu-id="ca7b7-141">-Permission</span></span>
<span data-ttu-id="ca7b7-142">指定儲存 blob 的許可權。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="ca7b7-143">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="ca7b7-144">-原則</span><span class="sxs-lookup"><span data-stu-id="ca7b7-144">-Policy</span></span>
<span data-ttu-id="ca7b7-145">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="ca7b7-146">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ca7b7-146">-Protocol</span></span>
<span data-ttu-id="ca7b7-147">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ca7b7-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ca7b7-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ca7b7-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ca7b7-149">HttpsOnly</span></span>
* <span data-ttu-id="ca7b7-150">HttpsOrHttp 預設值是 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ca7b7-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ca7b7-151">-StartTime</span></span>
<span data-ttu-id="ca7b7-152">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ca7b7-153">-確認</span><span class="sxs-lookup"><span data-stu-id="ca7b7-153">-Confirm</span></span>
<span data-ttu-id="ca7b7-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca7b7-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca7b7-155">-WhatIf</span></span>
<span data-ttu-id="ca7b7-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca7b7-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca7b7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7b7-158">CommonParameters</span></span>
<span data-ttu-id="ca7b7-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7b7-160">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7b7-161">輸入</span><span class="sxs-lookup"><span data-stu-id="ca7b7-161">INPUTS</span></span>

### <span data-ttu-id="ca7b7-162">[CloudBlob]。</span><span class="sxs-lookup"><span data-stu-id="ca7b7-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ca7b7-163">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ca7b7-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca7b7-164">輸出</span><span class="sxs-lookup"><span data-stu-id="ca7b7-164">OUTPUTS</span></span>

### <span data-ttu-id="ca7b7-165">System.object</span><span class="sxs-lookup"><span data-stu-id="ca7b7-165">System.String</span></span>

## <span data-ttu-id="ca7b7-166">筆記</span><span class="sxs-lookup"><span data-stu-id="ca7b7-166">NOTES</span></span>

## <span data-ttu-id="ca7b7-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca7b7-167">RELATED LINKS</span></span>

[<span data-ttu-id="ca7b7-168">AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ca7b7-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ca7b7-169">新-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ca7b7-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
