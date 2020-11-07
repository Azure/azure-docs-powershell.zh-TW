---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 17efee05b4d10ce87d327d8b7de26063bfc0cac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623526"
---
# <span data-ttu-id="ff376-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ff376-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="ff376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff376-102">SYNOPSIS</span></span>
<span data-ttu-id="ff376-103">針對 Azure 儲存區 blob 產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="ff376-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff376-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff376-104">SYNTAX</span></span>

### <span data-ttu-id="ff376-105">BlobNameWithPermission (預設) </span><span class="sxs-lookup"><span data-stu-id="ff376-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ff376-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="ff376-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ff376-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="ff376-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ff376-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="ff376-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ff376-109">說明</span><span class="sxs-lookup"><span data-stu-id="ff376-109">DESCRIPTION</span></span>
<span data-ttu-id="ff376-110">**AzureStorageBlobSASToken** Cmdlet 會針對 Azure 儲存區 blob 產生 (SAS) 權杖的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="ff376-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="ff376-111">示例</span><span class="sxs-lookup"><span data-stu-id="ff376-111">EXAMPLES</span></span>

### <span data-ttu-id="ff376-112">範例1：使用完整 blob 許可權產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="ff376-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="ff376-113">這個範例會產生含完整 blob 許可權的 blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="ff376-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="ff376-114">範例2：使用生命時間產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="ff376-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="ff376-115">這個範例會產生含生命時間的 blob SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="ff376-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="ff376-116">參數</span><span class="sxs-lookup"><span data-stu-id="ff376-116">PARAMETERS</span></span>

### <span data-ttu-id="ff376-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="ff376-117">-Blob</span></span>
<span data-ttu-id="ff376-118">指定儲存區 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="ff376-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff376-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ff376-119">-CloudBlob</span></span>
<span data-ttu-id="ff376-120">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="ff376-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="ff376-121">若要取得 **CloudBlob** 物件，請使用 [AzureStorageBlob](./Get-AzureStorageBlob.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff376-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff376-122">-容器</span><span class="sxs-lookup"><span data-stu-id="ff376-122">-Container</span></span>
<span data-ttu-id="ff376-123">指定儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ff376-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff376-124">-內容</span><span class="sxs-lookup"><span data-stu-id="ff376-124">-Context</span></span>
<span data-ttu-id="ff376-125">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="ff376-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="ff376-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ff376-126">-ExpiryTime</span></span>
<span data-ttu-id="ff376-127">指定共用存取簽章的到期時間。</span><span class="sxs-lookup"><span data-stu-id="ff376-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="ff376-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="ff376-128">-FullUri</span></span>
<span data-ttu-id="ff376-129">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="ff376-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="ff376-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="ff376-130">-IPAddressOrRange</span></span>
<span data-ttu-id="ff376-131">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="ff376-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="ff376-132">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="ff376-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="ff376-133">-許可權</span><span class="sxs-lookup"><span data-stu-id="ff376-133">-Permission</span></span>
<span data-ttu-id="ff376-134">指定儲存 blob 的許可權。</span><span class="sxs-lookup"><span data-stu-id="ff376-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff376-135">-原則</span><span class="sxs-lookup"><span data-stu-id="ff376-135">-Policy</span></span>
<span data-ttu-id="ff376-136">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ff376-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff376-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ff376-137">-Protocol</span></span>
<span data-ttu-id="ff376-138">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ff376-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="ff376-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ff376-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="ff376-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ff376-140">HttpsOnly</span></span>
* <span data-ttu-id="ff376-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="ff376-141">HttpsOrHttp</span></span>

<span data-ttu-id="ff376-142">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="ff376-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="ff376-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ff376-143">-StartTime</span></span>
<span data-ttu-id="ff376-144">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="ff376-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="ff376-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff376-145">CommonParameters</span></span>
<span data-ttu-id="ff376-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff376-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff376-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff376-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff376-148">輸入</span><span class="sxs-lookup"><span data-stu-id="ff376-148">INPUTS</span></span>

### <span data-ttu-id="ff376-149">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ff376-149">IStorageContext</span></span>

<span data-ttu-id="ff376-150">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ff376-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ff376-151">輸出</span><span class="sxs-lookup"><span data-stu-id="ff376-151">OUTPUTS</span></span>

### <span data-ttu-id="ff376-152">System.object</span><span class="sxs-lookup"><span data-stu-id="ff376-152">System.String</span></span>

## <span data-ttu-id="ff376-153">筆記</span><span class="sxs-lookup"><span data-stu-id="ff376-153">NOTES</span></span>

## <span data-ttu-id="ff376-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff376-154">RELATED LINKS</span></span>

[<span data-ttu-id="ff376-155">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ff376-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="ff376-156">新-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="ff376-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
