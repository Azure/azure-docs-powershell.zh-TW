---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: d029a00a2ddba5974fb473e58b933820e2e14757
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970027"
---
# <span data-ttu-id="fa364-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="fa364-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="fa364-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa364-102">SYNOPSIS</span></span>
<span data-ttu-id="fa364-103">設定共用的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="fa364-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="fa364-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa364-104">SYNTAX</span></span>

### <span data-ttu-id="fa364-105">共用名稱 (預設) </span><span class="sxs-lookup"><span data-stu-id="fa364-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fa364-106">共用</span><span class="sxs-lookup"><span data-stu-id="fa364-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa364-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa364-107">DESCRIPTION</span></span>
<span data-ttu-id="fa364-108">**AzStorageShareQuota** Cmdlet 會設定指定共用的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="fa364-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="fa364-109">示例</span><span class="sxs-lookup"><span data-stu-id="fa364-109">EXAMPLES</span></span>

### <span data-ttu-id="fa364-110">範例1：設定共用的儲存空間</span><span class="sxs-lookup"><span data-stu-id="fa364-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="fa364-111">這個命令會將名為 ContosoShare01 的共用的儲存空間設定為 1024 GB。</span><span class="sxs-lookup"><span data-stu-id="fa364-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="fa364-112">參數</span><span class="sxs-lookup"><span data-stu-id="fa364-112">PARAMETERS</span></span>

### <span data-ttu-id="fa364-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa364-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fa364-114">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="fa364-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fa364-115">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="fa364-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fa364-116">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fa364-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fa364-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fa364-118">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="fa364-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fa364-119">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="fa364-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fa364-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="fa364-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fa364-121">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="fa364-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fa364-122">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="fa364-122">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-123">-內容</span><span class="sxs-lookup"><span data-stu-id="fa364-123">-Context</span></span>
<span data-ttu-id="fa364-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="fa364-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fa364-125">若要取得儲存內容，請使用 [AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa364-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa364-126">-DefaultProfile</span></span>
<span data-ttu-id="fa364-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa364-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa364-128">-配額</span><span class="sxs-lookup"><span data-stu-id="fa364-128">-Quota</span></span>
<span data-ttu-id="fa364-129">以 gb 為 (GB) 指定配額值。</span><span class="sxs-lookup"><span data-stu-id="fa364-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="fa364-130">請參閱中的配額限制 https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits 。</span><span class="sxs-lookup"><span data-stu-id="fa364-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fa364-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fa364-132">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="fa364-132">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-133">-共用</span><span class="sxs-lookup"><span data-stu-id="fa364-133">-Share</span></span>
<span data-ttu-id="fa364-134">指定 **CloudFileShare** 物件來代表這個 Cmdlet 設定配額的共用。</span><span class="sxs-lookup"><span data-stu-id="fa364-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="fa364-135">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa364-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-136">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="fa364-136">-ShareName</span></span>
<span data-ttu-id="fa364-137">指定要設定配額之檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa364-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa364-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa364-138">CommonParameters</span></span>
<span data-ttu-id="fa364-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa364-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa364-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa364-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa364-141">輸入</span><span class="sxs-lookup"><span data-stu-id="fa364-141">INPUTS</span></span>

### <span data-ttu-id="fa364-142">System.object</span><span class="sxs-lookup"><span data-stu-id="fa364-142">System.String</span></span>

### <span data-ttu-id="fa364-143">CloudFileShare （即 Azure）</span><span class="sxs-lookup"><span data-stu-id="fa364-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="fa364-144">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="fa364-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fa364-145">輸出</span><span class="sxs-lookup"><span data-stu-id="fa364-145">OUTPUTS</span></span>

### <span data-ttu-id="fa364-146">AzureStorageFileShare WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="fa364-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="fa364-147">筆記</span><span class="sxs-lookup"><span data-stu-id="fa364-147">NOTES</span></span>

## <span data-ttu-id="fa364-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa364-148">RELATED LINKS</span></span>

[<span data-ttu-id="fa364-149">AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fa364-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="fa364-150">AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="fa364-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="fa364-151">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="fa364-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)