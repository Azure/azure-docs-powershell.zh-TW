---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 492ad3713bafa692d0ddf969540b8cab89fc05a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915045"
---
# <span data-ttu-id="60b5c-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="60b5c-101">New-AzStorageShare</span></span>

## <span data-ttu-id="60b5c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="60b5c-103">建立檔案共用。</span><span class="sxs-lookup"><span data-stu-id="60b5c-103">Creates a file share.</span></span>

## <span data-ttu-id="60b5c-104">語法</span><span class="sxs-lookup"><span data-stu-id="60b5c-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="60b5c-105">描述</span><span class="sxs-lookup"><span data-stu-id="60b5c-105">DESCRIPTION</span></span>
<span data-ttu-id="60b5c-106">**New-AzStorageShare** Cmdlet 會建立檔案共用。</span><span class="sxs-lookup"><span data-stu-id="60b5c-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="60b5c-107">例子</span><span class="sxs-lookup"><span data-stu-id="60b5c-107">EXAMPLES</span></span>

### <span data-ttu-id="60b5c-108">範例 1：建立檔案共用</span><span class="sxs-lookup"><span data-stu-id="60b5c-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="60b5c-109">此命令會建立名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="60b5c-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="60b5c-110">參數</span><span class="sxs-lookup"><span data-stu-id="60b5c-110">PARAMETERS</span></span>

### <span data-ttu-id="60b5c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60b5c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="60b5c-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="60b5c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="60b5c-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="60b5c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="60b5c-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="60b5c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="60b5c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="60b5c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="60b5c-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="60b5c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="60b5c-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="60b5c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="60b5c-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="60b5c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="60b5c-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="60b5c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="60b5c-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="60b5c-120">The default value is 10.</span></span>

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

### <span data-ttu-id="60b5c-121">-內容</span><span class="sxs-lookup"><span data-stu-id="60b5c-121">-Context</span></span>
<span data-ttu-id="60b5c-122">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="60b5c-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="60b5c-123">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60b5c-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="60b5c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b5c-124">-DefaultProfile</span></span>
<span data-ttu-id="60b5c-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60b5c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60b5c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="60b5c-126">-Name</span></span>
<span data-ttu-id="60b5c-127">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="60b5c-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="60b5c-128">此 Cmdlet 會建立具有此參數指定名稱的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="60b5c-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="60b5c-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60b5c-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="60b5c-130">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="60b5c-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="60b5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b5c-131">CommonParameters</span></span>
<span data-ttu-id="60b5c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60b5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b5c-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="60b5c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b5c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="60b5c-134">INPUTS</span></span>

### <span data-ttu-id="60b5c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="60b5c-135">System.String</span></span>

### <span data-ttu-id="60b5c-136">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="60b5c-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="60b5c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="60b5c-137">OUTPUTS</span></span>

### <span data-ttu-id="60b5c-138">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="60b5c-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="60b5c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="60b5c-139">NOTES</span></span>

## <span data-ttu-id="60b5c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="60b5c-140">RELATED LINKS</span></span>

[<span data-ttu-id="60b5c-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="60b5c-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="60b5c-142">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="60b5c-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="60b5c-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="60b5c-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
