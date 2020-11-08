---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: eb51b8c4e33f45d637354f85be049295626afdd6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128012"
---
# <span data-ttu-id="0c463-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c463-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="0c463-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c463-102">SYNOPSIS</span></span>
<span data-ttu-id="0c463-103">建立 Azure 儲存空間容器的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="0c463-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="0c463-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c463-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0c463-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c463-105">DESCRIPTION</span></span>
<span data-ttu-id="0c463-106">**新的-AzStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="0c463-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="0c463-107">示例</span><span class="sxs-lookup"><span data-stu-id="0c463-107">EXAMPLES</span></span>

### <span data-ttu-id="0c463-108">範例1：在儲存空間容器中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="0c463-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="0c463-109">這個命令會在名為 MyContainer 的存儲容器中建立名為 Policy01 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="0c463-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="0c463-110">參數</span><span class="sxs-lookup"><span data-stu-id="0c463-110">PARAMETERS</span></span>

### <span data-ttu-id="0c463-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c463-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0c463-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c463-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c463-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="0c463-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c463-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c463-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c463-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0c463-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0c463-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="0c463-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0c463-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="0c463-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0c463-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="0c463-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0c463-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="0c463-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0c463-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="0c463-120">The default value is 10.</span></span>

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

### <span data-ttu-id="0c463-121">-容器</span><span class="sxs-lookup"><span data-stu-id="0c463-121">-Container</span></span>
<span data-ttu-id="0c463-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="0c463-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c463-123">-內容</span><span class="sxs-lookup"><span data-stu-id="0c463-123">-Context</span></span>
<span data-ttu-id="0c463-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="0c463-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0c463-125">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c463-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0c463-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c463-126">-DefaultProfile</span></span>
<span data-ttu-id="0c463-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c463-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c463-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0c463-128">-ExpiryTime</span></span>
<span data-ttu-id="0c463-129">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="0c463-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="0c463-130">-許可權</span><span class="sxs-lookup"><span data-stu-id="0c463-130">-Permission</span></span>
<span data-ttu-id="0c463-131">指定儲存的存取原則中的許可權來存取容器。</span><span class="sxs-lookup"><span data-stu-id="0c463-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="0c463-132">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="0c463-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0c463-133">-原則</span><span class="sxs-lookup"><span data-stu-id="0c463-133">-Policy</span></span>
<span data-ttu-id="0c463-134">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="0c463-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c463-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0c463-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0c463-136">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0c463-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0c463-137">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="0c463-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0c463-138">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c463-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0c463-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0c463-139">-StartTime</span></span>
<span data-ttu-id="0c463-140">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="0c463-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="0c463-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c463-141">CommonParameters</span></span>
<span data-ttu-id="0c463-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c463-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c463-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c463-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c463-144">輸入</span><span class="sxs-lookup"><span data-stu-id="0c463-144">INPUTS</span></span>

### <span data-ttu-id="0c463-145">System.object</span><span class="sxs-lookup"><span data-stu-id="0c463-145">System.String</span></span>

### <span data-ttu-id="0c463-146">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="0c463-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0c463-147">輸出</span><span class="sxs-lookup"><span data-stu-id="0c463-147">OUTPUTS</span></span>

### <span data-ttu-id="0c463-148">System.object</span><span class="sxs-lookup"><span data-stu-id="0c463-148">System.String</span></span>

## <span data-ttu-id="0c463-149">筆記</span><span class="sxs-lookup"><span data-stu-id="0c463-149">NOTES</span></span>

## <span data-ttu-id="0c463-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c463-150">RELATED LINKS</span></span>

[<span data-ttu-id="0c463-151">AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c463-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="0c463-152">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="0c463-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0c463-153">移除-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c463-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="0c463-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c463-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


