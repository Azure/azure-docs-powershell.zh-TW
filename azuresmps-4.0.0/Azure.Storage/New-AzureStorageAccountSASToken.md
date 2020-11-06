---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443411"
---
# <span data-ttu-id="80430-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="80430-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80430-102">SYNOPSIS</span></span>
<span data-ttu-id="80430-103">建立 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="80430-103">Creates an SAS token.</span></span>

## <span data-ttu-id="80430-104">句法</span><span class="sxs-lookup"><span data-stu-id="80430-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="80430-105">說明</span><span class="sxs-lookup"><span data-stu-id="80430-105">DESCRIPTION</span></span>
<span data-ttu-id="80430-106">**新的-AzureStorageSASToken** Cmdlet 會針對 Azure 儲存空間帳戶 (SAS) 權杖建立帳戶層級的共用存取簽章。</span><span class="sxs-lookup"><span data-stu-id="80430-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="80430-107">您可以使用 SAS 權杖委派多個服務的許可權，或委派無法搭配物件層級 SAS 權杖使用之服務的許可權。</span><span class="sxs-lookup"><span data-stu-id="80430-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="80430-108">示例</span><span class="sxs-lookup"><span data-stu-id="80430-108">EXAMPLES</span></span>

### <span data-ttu-id="80430-109">範例1：建立 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="80430-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="80430-110">這個命令會建立具有完整許可權的帳戶層級 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="80430-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="80430-111">範例2：針對 IP 位址範圍建立 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="80430-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="80430-112">這個命令會針對來自指定 IP 位址範圍的 HTTPS 式要求建立 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="80430-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="80430-113">參數</span><span class="sxs-lookup"><span data-stu-id="80430-113">PARAMETERS</span></span>

### <span data-ttu-id="80430-114">-內容</span><span class="sxs-lookup"><span data-stu-id="80430-114">-Context</span></span>
<span data-ttu-id="80430-115">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="80430-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="80430-116">您可以使用 New-AzureStorageContext Cmdlet 來取得 **AzureStorageCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="80430-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="80430-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="80430-117">-ExpiryTime</span></span>
<span data-ttu-id="80430-118">指定共用存取簽名失效的時間。</span><span class="sxs-lookup"><span data-stu-id="80430-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="80430-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="80430-119">-IPAddressOrRange</span></span>
<span data-ttu-id="80430-120">指定要接受其要求的 ip 位址或 IP 位址範圍（例如168.1.5.65 或 168.1.5.60-168.1.5.70）。</span><span class="sxs-lookup"><span data-stu-id="80430-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="80430-121">範圍包括在內。</span><span class="sxs-lookup"><span data-stu-id="80430-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="80430-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="80430-122">-Permission</span></span>
<span data-ttu-id="80430-123">指定儲存空間帳戶的許可權。</span><span class="sxs-lookup"><span data-stu-id="80430-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="80430-124">許可權只有符合指定的資源類型時才是有效的。</span><span class="sxs-lookup"><span data-stu-id="80430-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="80430-125">如需可接受許可權值的詳細資訊，請參閱建立帳戶 SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="80430-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="80430-126">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="80430-126">-Protocol</span></span>
<span data-ttu-id="80430-127">指定以帳戶 SA 發出的要求所允許的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="80430-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="80430-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="80430-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80430-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="80430-129">HttpsOnly</span></span>
- <span data-ttu-id="80430-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="80430-130">HttpsOrHttp</span></span>

<span data-ttu-id="80430-131">預設值為 HttpsOrHttp。</span><span class="sxs-lookup"><span data-stu-id="80430-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="80430-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="80430-132">-ResourceType</span></span>
<span data-ttu-id="80430-133">指定可用於 SAS 權杖的資源類型。</span><span class="sxs-lookup"><span data-stu-id="80430-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="80430-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="80430-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80430-135">所有</span><span class="sxs-lookup"><span data-stu-id="80430-135">None</span></span>
- <span data-ttu-id="80430-136">Services</span><span class="sxs-lookup"><span data-stu-id="80430-136">Service</span></span>
- <span data-ttu-id="80430-137">包裝箱</span><span class="sxs-lookup"><span data-stu-id="80430-137">Container</span></span>
- <span data-ttu-id="80430-138">面向</span><span class="sxs-lookup"><span data-stu-id="80430-138">Object</span></span>

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

### <span data-ttu-id="80430-139">-服務</span><span class="sxs-lookup"><span data-stu-id="80430-139">-Service</span></span>
<span data-ttu-id="80430-140">指定服務。</span><span class="sxs-lookup"><span data-stu-id="80430-140">Specifies the service.</span></span>
<span data-ttu-id="80430-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="80430-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80430-142">所有</span><span class="sxs-lookup"><span data-stu-id="80430-142">None</span></span>
- <span data-ttu-id="80430-143">Blob</span><span class="sxs-lookup"><span data-stu-id="80430-143">Blob</span></span>
- <span data-ttu-id="80430-144">檔案</span><span class="sxs-lookup"><span data-stu-id="80430-144">File</span></span>
- <span data-ttu-id="80430-145">序列</span><span class="sxs-lookup"><span data-stu-id="80430-145">Queue</span></span>
- <span data-ttu-id="80430-146">張</span><span class="sxs-lookup"><span data-stu-id="80430-146">Table</span></span>

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

### <span data-ttu-id="80430-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="80430-147">-StartTime</span></span>
<span data-ttu-id="80430-148">指定時間（以 **DateTime** 物件表示），SAS 就會生效。</span><span class="sxs-lookup"><span data-stu-id="80430-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="80430-149">若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="80430-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="80430-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80430-150">CommonParameters</span></span>
<span data-ttu-id="80430-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80430-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80430-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80430-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80430-153">輸入</span><span class="sxs-lookup"><span data-stu-id="80430-153">INPUTS</span></span>

## <span data-ttu-id="80430-154">輸出</span><span class="sxs-lookup"><span data-stu-id="80430-154">OUTPUTS</span></span>

## <span data-ttu-id="80430-155">筆記</span><span class="sxs-lookup"><span data-stu-id="80430-155">NOTES</span></span>

## <span data-ttu-id="80430-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="80430-156">RELATED LINKS</span></span>

[<span data-ttu-id="80430-157">新-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="80430-158">新-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="80430-159">新-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="80430-160">新-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="80430-161">新-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="80430-162">新-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="80430-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


