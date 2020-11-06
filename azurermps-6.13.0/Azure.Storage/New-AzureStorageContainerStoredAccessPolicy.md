---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6dadd92955c325120b67d8faae99c7f8ae90dc5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450399"
---
# <span data-ttu-id="593df-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="593df-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="593df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="593df-102">SYNOPSIS</span></span>
<span data-ttu-id="593df-103">建立 Azure 儲存空間容器的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="593df-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="593df-104">句法</span><span class="sxs-lookup"><span data-stu-id="593df-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="593df-105">說明</span><span class="sxs-lookup"><span data-stu-id="593df-105">DESCRIPTION</span></span>
<span data-ttu-id="593df-106">**新的-AzureStorageContainerStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間容器建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="593df-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="593df-107">示例</span><span class="sxs-lookup"><span data-stu-id="593df-107">EXAMPLES</span></span>

### <span data-ttu-id="593df-108">範例1：在儲存空間容器中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="593df-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="593df-109">這個命令會在名為 MyContainer 的存儲容器中建立名為 Policy01 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="593df-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="593df-110">參數</span><span class="sxs-lookup"><span data-stu-id="593df-110">PARAMETERS</span></span>

### <span data-ttu-id="593df-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="593df-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="593df-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="593df-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="593df-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="593df-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="593df-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="593df-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="593df-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="593df-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="593df-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="593df-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="593df-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="593df-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="593df-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="593df-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="593df-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="593df-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="593df-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="593df-120">The default value is 10.</span></span>

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

### <span data-ttu-id="593df-121">-容器</span><span class="sxs-lookup"><span data-stu-id="593df-121">-Container</span></span>
<span data-ttu-id="593df-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="593df-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="593df-123">-內容</span><span class="sxs-lookup"><span data-stu-id="593df-123">-Context</span></span>
<span data-ttu-id="593df-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="593df-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="593df-125">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="593df-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="593df-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593df-126">-DefaultProfile</span></span>
<span data-ttu-id="593df-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="593df-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="593df-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="593df-128">-ExpiryTime</span></span>
<span data-ttu-id="593df-129">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="593df-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="593df-130">-許可權</span><span class="sxs-lookup"><span data-stu-id="593df-130">-Permission</span></span>
<span data-ttu-id="593df-131">指定儲存的存取原則中的許可權來存取容器。</span><span class="sxs-lookup"><span data-stu-id="593df-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="593df-132">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="593df-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="593df-133">-原則</span><span class="sxs-lookup"><span data-stu-id="593df-133">-Policy</span></span>
<span data-ttu-id="593df-134">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="593df-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="593df-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="593df-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="593df-136">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="593df-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="593df-137">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="593df-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="593df-138">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="593df-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="593df-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="593df-139">-StartTime</span></span>
<span data-ttu-id="593df-140">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="593df-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="593df-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593df-141">CommonParameters</span></span>
<span data-ttu-id="593df-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="593df-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593df-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="593df-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593df-144">輸入</span><span class="sxs-lookup"><span data-stu-id="593df-144">INPUTS</span></span>

### <span data-ttu-id="593df-145">System.object</span><span class="sxs-lookup"><span data-stu-id="593df-145">System.String</span></span>

### <span data-ttu-id="593df-146">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="593df-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="593df-147">輸出</span><span class="sxs-lookup"><span data-stu-id="593df-147">OUTPUTS</span></span>

### <span data-ttu-id="593df-148">System.object</span><span class="sxs-lookup"><span data-stu-id="593df-148">System.String</span></span>

## <span data-ttu-id="593df-149">筆記</span><span class="sxs-lookup"><span data-stu-id="593df-149">NOTES</span></span>

## <span data-ttu-id="593df-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="593df-150">RELATED LINKS</span></span>

[<span data-ttu-id="593df-151">AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="593df-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="593df-152">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="593df-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="593df-153">移除-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="593df-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="593df-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="593df-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


