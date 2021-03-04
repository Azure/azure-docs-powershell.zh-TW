---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 132ad47cd52f258b78ac944342d86979a69abbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916341"
---
# <span data-ttu-id="78507-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="78507-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="78507-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78507-102">SYNOPSIS</span></span>
<span data-ttu-id="78507-103">設定共用儲存空間容量。</span><span class="sxs-lookup"><span data-stu-id="78507-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="78507-104">語法</span><span class="sxs-lookup"><span data-stu-id="78507-104">SYNTAX</span></span>

### <span data-ttu-id="78507-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="78507-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="78507-106">共用</span><span class="sxs-lookup"><span data-stu-id="78507-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="78507-107">描述</span><span class="sxs-lookup"><span data-stu-id="78507-107">DESCRIPTION</span></span>
<span data-ttu-id="78507-108">**Set-AzStorageShareQuota** Cmdlet 會設定指定共用的儲存容量。</span><span class="sxs-lookup"><span data-stu-id="78507-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="78507-109">例子</span><span class="sxs-lookup"><span data-stu-id="78507-109">EXAMPLES</span></span>

### <span data-ttu-id="78507-110">範例 1：設定共用儲存容量</span><span class="sxs-lookup"><span data-stu-id="78507-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="78507-111">此命令將名為 ContosoShare01 的共用儲存空間設為 1024 GB。</span><span class="sxs-lookup"><span data-stu-id="78507-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="78507-112">參數</span><span class="sxs-lookup"><span data-stu-id="78507-112">PARAMETERS</span></span>

### <span data-ttu-id="78507-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78507-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="78507-114">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="78507-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="78507-115">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="78507-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="78507-116">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="78507-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="78507-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="78507-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="78507-118">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="78507-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="78507-119">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="78507-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="78507-120">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="78507-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="78507-121">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="78507-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="78507-122">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="78507-122">The default value is 10.</span></span>

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

### <span data-ttu-id="78507-123">-內容</span><span class="sxs-lookup"><span data-stu-id="78507-123">-Context</span></span>
<span data-ttu-id="78507-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="78507-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="78507-125">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78507-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="78507-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78507-126">-DefaultProfile</span></span>
<span data-ttu-id="78507-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78507-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78507-128">-配額</span><span class="sxs-lookup"><span data-stu-id="78507-128">-Quota</span></span>
<span data-ttu-id="78507-129">指定配額值 ，以 GB (GB) 。</span><span class="sxs-lookup"><span data-stu-id="78507-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="78507-130">請參閱 中的配額限制 https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits 。</span><span class="sxs-lookup"><span data-stu-id="78507-130">See the quota limitation in https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="78507-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="78507-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="78507-132">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="78507-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="78507-133">-共用</span><span class="sxs-lookup"><span data-stu-id="78507-133">-Share</span></span>
<span data-ttu-id="78507-134">指定 **CloudFileShare** 物件來代表此 Cmdlet 設定配額的共用。</span><span class="sxs-lookup"><span data-stu-id="78507-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="78507-135">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78507-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="78507-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="78507-136">-ShareName</span></span>
<span data-ttu-id="78507-137">指定要設定配額的檔案共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="78507-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="78507-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78507-138">CommonParameters</span></span>
<span data-ttu-id="78507-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78507-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78507-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="78507-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78507-141">輸入</span><span class="sxs-lookup"><span data-stu-id="78507-141">INPUTS</span></span>

### <span data-ttu-id="78507-142">System.String</span><span class="sxs-lookup"><span data-stu-id="78507-142">System.String</span></span>

### <span data-ttu-id="78507-143">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="78507-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="78507-144">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="78507-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="78507-145">輸出</span><span class="sxs-lookup"><span data-stu-id="78507-145">OUTPUTS</span></span>

### <span data-ttu-id="78507-146">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="78507-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="78507-147">筆記</span><span class="sxs-lookup"><span data-stu-id="78507-147">NOTES</span></span>

## <span data-ttu-id="78507-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="78507-148">RELATED LINKS</span></span>

[<span data-ttu-id="78507-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="78507-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="78507-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="78507-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="78507-151">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="78507-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
