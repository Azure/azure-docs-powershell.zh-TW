---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d1db19d4b49815f5c4e9c6a413008e55707c291b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454980"
---
# <span data-ttu-id="9a8c1-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="9a8c1-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="9a8c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a8c1-103">設定共用的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a8c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a8c1-104">SYNTAX</span></span>

### <span data-ttu-id="9a8c1-105">名</span><span class="sxs-lookup"><span data-stu-id="9a8c1-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a8c1-106">共用</span><span class="sxs-lookup"><span data-stu-id="9a8c1-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9a8c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a8c1-107">DESCRIPTION</span></span>
<span data-ttu-id="9a8c1-108">**AzureStorageShareQuota** Cmdlet 會設定指定共用的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="9a8c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a8c1-109">EXAMPLES</span></span>

### <span data-ttu-id="9a8c1-110">範例1：設定共用的儲存空間</span><span class="sxs-lookup"><span data-stu-id="9a8c1-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="9a8c1-111">這個命令會將名為 ContosoShare01 的共用的儲存空間設定為 1024 GB。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="9a8c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a8c1-112">PARAMETERS</span></span>

### <span data-ttu-id="9a8c1-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a8c1-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9a8c1-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9a8c1-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9a8c1-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9a8c1-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9a8c1-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9a8c1-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9a8c1-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9a8c1-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9a8c1-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-122">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-123">-內容</span><span class="sxs-lookup"><span data-stu-id="9a8c1-123">-Context</span></span>
<span data-ttu-id="9a8c1-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9a8c1-125">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-126">-配額</span><span class="sxs-lookup"><span data-stu-id="9a8c1-126">-Quota</span></span>
<span data-ttu-id="9a8c1-127">以 gb 為 (GB) 指定配額值。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9a8c1-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9a8c1-129">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-129">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-130">-共用</span><span class="sxs-lookup"><span data-stu-id="9a8c1-130">-Share</span></span>
<span data-ttu-id="9a8c1-131">指定 **CloudFileShare** 物件來代表這個 Cmdlet 設定配額的共用。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="9a8c1-132">若要取得 **CloudFileShare** 物件，請使用 Get-AzureStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-133">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="9a8c1-133">-ShareName</span></span>
<span data-ttu-id="9a8c1-134">指定要設定配額之檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a8c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a8c1-135">CommonParameters</span></span>
<span data-ttu-id="9a8c1-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a8c1-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a8c1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a8c1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="9a8c1-138">INPUTS</span></span>

### <span data-ttu-id="9a8c1-139">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="9a8c1-139">IStorageContext</span></span>

<span data-ttu-id="9a8c1-140">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9a8c1-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="9a8c1-141">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9a8c1-141">CloudFileShare</span></span>

<span data-ttu-id="9a8c1-142">形參 "Share" 接受管線中 "CloudFileShare" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9a8c1-142">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

### <span data-ttu-id="9a8c1-143">字串</span><span class="sxs-lookup"><span data-stu-id="9a8c1-143">String</span></span>

<span data-ttu-id="9a8c1-144">參數「共用名稱」接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9a8c1-144">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9a8c1-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9a8c1-145">OUTPUTS</span></span>

### <span data-ttu-id="9a8c1-146">[WindowsAzure] FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="9a8c1-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="9a8c1-147">筆記</span><span class="sxs-lookup"><span data-stu-id="9a8c1-147">NOTES</span></span>

## <span data-ttu-id="9a8c1-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a8c1-148">RELATED LINKS</span></span>

[<span data-ttu-id="9a8c1-149">AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9a8c1-149">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="9a8c1-150">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="9a8c1-150">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="9a8c1-151">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="9a8c1-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
