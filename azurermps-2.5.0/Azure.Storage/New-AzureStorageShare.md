---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 55ee72941f49954bcc56f9558bc7ffb444ae9e6b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801458"
---
# <span data-ttu-id="b1365-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b1365-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="b1365-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1365-102">SYNOPSIS</span></span>
<span data-ttu-id="b1365-103">建立檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b1365-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1365-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1365-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1365-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1365-105">DESCRIPTION</span></span>
<span data-ttu-id="b1365-106">**新的-AzureStorageShare** Cmdlet 會建立檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b1365-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="b1365-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1365-107">EXAMPLES</span></span>

### <span data-ttu-id="b1365-108">範例1：建立檔案共用</span><span class="sxs-lookup"><span data-stu-id="b1365-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="b1365-109">這個命令會建立名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b1365-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="b1365-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1365-110">PARAMETERS</span></span>

### <span data-ttu-id="b1365-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b1365-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b1365-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b1365-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b1365-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="b1365-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b1365-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b1365-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b1365-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b1365-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b1365-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="b1365-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b1365-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="b1365-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b1365-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="b1365-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b1365-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="b1365-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b1365-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="b1365-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b1365-121">-內容</span><span class="sxs-lookup"><span data-stu-id="b1365-121">-Context</span></span>
<span data-ttu-id="b1365-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b1365-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b1365-123">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1365-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b1365-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1365-124">-DefaultProfile</span></span>
<span data-ttu-id="b1365-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1365-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1365-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1365-126">-Name</span></span>
<span data-ttu-id="b1365-127">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1365-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="b1365-128">這個 Cmdlet 會建立具有此參數指定之名稱的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="b1365-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1365-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b1365-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b1365-130">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="b1365-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b1365-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1365-131">CommonParameters</span></span>
<span data-ttu-id="b1365-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1365-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1365-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1365-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1365-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b1365-134">INPUTS</span></span>

### <span data-ttu-id="b1365-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b1365-135">System.String</span></span>

### <span data-ttu-id="b1365-136">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b1365-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b1365-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b1365-137">OUTPUTS</span></span>

### <span data-ttu-id="b1365-138">[WindowsAzure] CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b1365-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="b1365-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b1365-139">NOTES</span></span>

## <span data-ttu-id="b1365-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1365-140">RELATED LINKS</span></span>

[<span data-ttu-id="b1365-141">AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b1365-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b1365-142">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b1365-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b1365-143">移除-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b1365-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
