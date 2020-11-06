---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8d84b310a16a73456bcd519332fa76ad1a6566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443408"
---
# <span data-ttu-id="91507-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="91507-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="91507-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91507-102">SYNOPSIS</span></span>
<span data-ttu-id="91507-103">針對 Azure 儲存區 blob 產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="91507-103">Generates an SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="91507-104">句法</span><span class="sxs-lookup"><span data-stu-id="91507-104">SYNTAX</span></span>

### <span data-ttu-id="91507-105">BlobNameWithPermission (預設) </span><span class="sxs-lookup"><span data-stu-id="91507-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="91507-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="91507-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="91507-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="91507-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="91507-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="91507-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="91507-109">說明</span><span class="sxs-lookup"><span data-stu-id="91507-109">DESCRIPTION</span></span>
<span data-ttu-id="91507-110">**AzureStorageBlobSASToken** Cmdlet 會針對 Azure 儲存區 blob 產生 (SAS) 權杖的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="91507-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="91507-111">示例</span><span class="sxs-lookup"><span data-stu-id="91507-111">EXAMPLES</span></span>

### <span data-ttu-id="91507-112">範例1：使用完整 blob 許可權產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="91507-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="91507-113">這個範例會產生含完整 blob 許可權的 blob SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="91507-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="91507-114">範例2：使用生命時間產生 blob SAS 標記</span><span class="sxs-lookup"><span data-stu-id="91507-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="91507-115">這個範例會產生含生命時間的 blob SAS 標記。</span><span class="sxs-lookup"><span data-stu-id="91507-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="91507-116">參數</span><span class="sxs-lookup"><span data-stu-id="91507-116">PARAMETERS</span></span>

### <span data-ttu-id="91507-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="91507-117">-Blob</span></span>
<span data-ttu-id="91507-118">指定儲存區 blob 名稱。</span><span class="sxs-lookup"><span data-stu-id="91507-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="91507-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="91507-119">-CloudBlob</span></span>
<span data-ttu-id="91507-120">指定 **CloudBlob** 物件。</span><span class="sxs-lookup"><span data-stu-id="91507-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="91507-121">若要取得 **CloudBlob** 物件，請使用 [AzureStorageBlob](./Get-AzureStorageBlob.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91507-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="91507-122">-容器</span><span class="sxs-lookup"><span data-stu-id="91507-122">-Container</span></span>
<span data-ttu-id="91507-123">指定儲存容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="91507-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="91507-124">-內容</span><span class="sxs-lookup"><span data-stu-id="91507-124">-Context</span></span>
<span data-ttu-id="91507-125">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="91507-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="91507-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="91507-126">-ExpiryTime</span></span>
<span data-ttu-id="91507-127">指定共用存取簽章的到期時間。</span><span class="sxs-lookup"><span data-stu-id="91507-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="91507-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="91507-128">-FullUri</span></span>
<span data-ttu-id="91507-129">指示這個 Cmdlet 會傳回完整的 blob URI 和共用的存取簽章權杖。</span><span class="sxs-lookup"><span data-stu-id="91507-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="91507-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="91507-130">-IPAddressOrRange</span></span>
<span data-ttu-id="91507-131">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="91507-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="91507-132">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="91507-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="91507-133">-許可權</span><span class="sxs-lookup"><span data-stu-id="91507-133">-Permission</span></span>
<span data-ttu-id="91507-134">指定儲存 blob 的許可權。</span><span class="sxs-lookup"><span data-stu-id="91507-134">Specifies the permissions for a storage blob.</span></span>

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

### <span data-ttu-id="91507-135">-原則</span><span class="sxs-lookup"><span data-stu-id="91507-135">-Policy</span></span>
<span data-ttu-id="91507-136">指定 Azure 儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="91507-136">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="91507-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="91507-137">-Protocol</span></span>
<span data-ttu-id="91507-138">指定要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="91507-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="91507-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="91507-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="91507-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="91507-140">HttpsOnly</span></span>
* <span data-ttu-id="91507-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="91507-141">HttpsOrHttp</span></span>

<span data-ttu-id="91507-142">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="91507-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="91507-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="91507-143">-StartTime</span></span>
<span data-ttu-id="91507-144">指定共用存取簽章生效的時間。</span><span class="sxs-lookup"><span data-stu-id="91507-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="91507-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91507-145">CommonParameters</span></span>
<span data-ttu-id="91507-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91507-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91507-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91507-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91507-148">輸入</span><span class="sxs-lookup"><span data-stu-id="91507-148">INPUTS</span></span>

## <span data-ttu-id="91507-149">輸出</span><span class="sxs-lookup"><span data-stu-id="91507-149">OUTPUTS</span></span>

## <span data-ttu-id="91507-150">筆記</span><span class="sxs-lookup"><span data-stu-id="91507-150">NOTES</span></span>

## <span data-ttu-id="91507-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="91507-151">RELATED LINKS</span></span>

[<span data-ttu-id="91507-152">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="91507-152">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="91507-153">新-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="91507-153">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
