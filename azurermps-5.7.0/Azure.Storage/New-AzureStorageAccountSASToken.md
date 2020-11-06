---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
ms.openlocfilehash: fb0565232410e840ef3e8adbad48e7f622a51d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452319"
---
# <span data-ttu-id="0ceb7-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="0ceb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ceb7-102">SYNOPSIS</span></span>
<span data-ttu-id="0ceb7-103">建立帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ceb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ceb7-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ceb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ceb7-105">DESCRIPTION</span></span>
<span data-ttu-id="0ceb7-106">**新的-AzureStorageSASToken** Cmdlet 會針對 Azure 儲存空間帳戶 (SAS) 權杖建立帳戶層級的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="0ceb7-107">您可以使用 SAS 權杖委派多個服務的許可權，或委派無法搭配物件層級 SAS 權杖使用之服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="0ceb7-108">示例</span><span class="sxs-lookup"><span data-stu-id="0ceb7-108">EXAMPLES</span></span>

### <span data-ttu-id="0ceb7-109">範例1：使用完整許可權建立帳戶層級 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="0ceb7-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="0ceb7-110">這個命令會建立具有完整許可權的帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="0ceb7-111">範例2：針對 IP 位址範圍建立帳戶層級 SAS 標記</span><span class="sxs-lookup"><span data-stu-id="0ceb7-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="0ceb7-112">這個命令會針對來自指定 IP 位址範圍的 HTTPS 式要求建立帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="0ceb7-113">參數</span><span class="sxs-lookup"><span data-stu-id="0ceb7-113">PARAMETERS</span></span>

### <span data-ttu-id="0ceb7-114">-內容</span><span class="sxs-lookup"><span data-stu-id="0ceb7-114">-Context</span></span>
<span data-ttu-id="0ceb7-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="0ceb7-116">您可以使用 New-AzureStorageContext Cmdlet 來取得 **AzureStorageCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="0ceb7-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0ceb7-117">-ExpiryTime</span></span>
<span data-ttu-id="0ceb7-118">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="0ceb7-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="0ceb7-119">-IPAddressOrRange</span></span>
<span data-ttu-id="0ceb7-120">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="0ceb7-121">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="0ceb7-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="0ceb7-122">-Permission</span></span>
<span data-ttu-id="0ceb7-123">指定儲存空間帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="0ceb7-124">許可權只有符合指定的資源類型時才是有效的。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="0ceb7-125">如需可接受許可權值的詳細資訊，請參閱建立帳戶 SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="0ceb7-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="0ceb7-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="0ceb7-126">-Protocol</span></span>
<span data-ttu-id="0ceb7-127">指定以帳戶 SA 發出的要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="0ceb7-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0ceb7-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ceb7-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0ceb7-129">HttpsOnly</span></span>
- <span data-ttu-id="0ceb7-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="0ceb7-130">HttpsOrHttp</span></span>

<span data-ttu-id="0ceb7-131">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="0ceb7-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0ceb7-132">-ResourceType</span></span>
<span data-ttu-id="0ceb7-133">指定可用於 SAS 權杖的資源類型。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="0ceb7-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0ceb7-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ceb7-135">所有</span><span class="sxs-lookup"><span data-stu-id="0ceb7-135">None</span></span>
- <span data-ttu-id="0ceb7-136">Services</span><span class="sxs-lookup"><span data-stu-id="0ceb7-136">Service</span></span>
- <span data-ttu-id="0ceb7-137">包裝箱</span><span class="sxs-lookup"><span data-stu-id="0ceb7-137">Container</span></span>
- <span data-ttu-id="0ceb7-138">面向</span><span class="sxs-lookup"><span data-stu-id="0ceb7-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ceb7-139">-服務</span><span class="sxs-lookup"><span data-stu-id="0ceb7-139">-Service</span></span>
<span data-ttu-id="0ceb7-140">指定服務。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-140">Specifies the service.</span></span>
<span data-ttu-id="0ceb7-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0ceb7-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ceb7-142">所有</span><span class="sxs-lookup"><span data-stu-id="0ceb7-142">None</span></span>
- <span data-ttu-id="0ceb7-143">Blob</span><span class="sxs-lookup"><span data-stu-id="0ceb7-143">Blob</span></span>
- <span data-ttu-id="0ceb7-144">檔案</span><span class="sxs-lookup"><span data-stu-id="0ceb7-144">File</span></span>
- <span data-ttu-id="0ceb7-145">序列</span><span class="sxs-lookup"><span data-stu-id="0ceb7-145">Queue</span></span>
- <span data-ttu-id="0ceb7-146">張</span><span class="sxs-lookup"><span data-stu-id="0ceb7-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ceb7-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0ceb7-147">-StartTime</span></span>
<span data-ttu-id="0ceb7-148">指定時間（以 **DateTime** 物件表示），SAS 就會生效。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="0ceb7-149">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="0ceb7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ceb7-150">CommonParameters</span></span>
<span data-ttu-id="0ceb7-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ceb7-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ceb7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ceb7-153">輸入</span><span class="sxs-lookup"><span data-stu-id="0ceb7-153">INPUTS</span></span>

### <span data-ttu-id="0ceb7-154">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0ceb7-154">IStorageContext</span></span>

<span data-ttu-id="0ceb7-155">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0ceb7-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="0ceb7-156">輸出</span><span class="sxs-lookup"><span data-stu-id="0ceb7-156">OUTPUTS</span></span>

### <span data-ttu-id="0ceb7-157">System.object</span><span class="sxs-lookup"><span data-stu-id="0ceb7-157">System.String</span></span>

## <span data-ttu-id="0ceb7-158">筆記</span><span class="sxs-lookup"><span data-stu-id="0ceb7-158">NOTES</span></span>

## <span data-ttu-id="0ceb7-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ceb7-159">RELATED LINKS</span></span>

[<span data-ttu-id="0ceb7-160">新-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="0ceb7-161">新-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="0ceb7-162">新-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="0ceb7-163">新-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="0ceb7-164">新-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="0ceb7-165">新-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="0ceb7-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


