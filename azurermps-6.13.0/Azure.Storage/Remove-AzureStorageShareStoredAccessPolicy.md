---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 64eb11604d1b75682b95851f87ff8aa9d2b26466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450385"
---
# <span data-ttu-id="dcd01-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd01-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="dcd01-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcd01-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd01-103">從儲存空間共用移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="dcd01-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd01-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcd01-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcd01-105">說明</span><span class="sxs-lookup"><span data-stu-id="dcd01-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd01-106">**AzureStorageShareStoredAccessPolicy** Cmdlet 會從 Azure 儲存空間共用中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="dcd01-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="dcd01-107">示例</span><span class="sxs-lookup"><span data-stu-id="dcd01-107">EXAMPLES</span></span>

### <span data-ttu-id="dcd01-108">範例1：從 Azure 儲存空間共用移除已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="dcd01-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="dcd01-109">這個命令會從 ContosoShare 中移除名為 GeneralPolicy 的儲存訪問原則。</span><span class="sxs-lookup"><span data-stu-id="dcd01-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="dcd01-110">參數</span><span class="sxs-lookup"><span data-stu-id="dcd01-110">PARAMETERS</span></span>

### <span data-ttu-id="dcd01-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd01-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dcd01-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="dcd01-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dcd01-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="dcd01-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dcd01-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="dcd01-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dcd01-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dcd01-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dcd01-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="dcd01-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dcd01-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="dcd01-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dcd01-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="dcd01-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dcd01-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="dcd01-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dcd01-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="dcd01-120">The default value is 10.</span></span>

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

### <span data-ttu-id="dcd01-121">-內容</span><span class="sxs-lookup"><span data-stu-id="dcd01-121">-Context</span></span>
<span data-ttu-id="dcd01-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="dcd01-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dcd01-123">若要取得儲存內容，請使用 [AzureStorageCoNtext](./New-AzureStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcd01-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dcd01-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd01-124">-DefaultProfile</span></span>
<span data-ttu-id="dcd01-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcd01-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd01-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcd01-126">-PassThru</span></span>
<span data-ttu-id="dcd01-127">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="dcd01-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dcd01-128">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dcd01-128">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd01-129">-原則</span><span class="sxs-lookup"><span data-stu-id="dcd01-129">-Policy</span></span>
<span data-ttu-id="dcd01-130">指定此 Cmdlet 移除之已儲存的訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="dcd01-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd01-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd01-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dcd01-132">指定要求中伺服器部分的超時時間長度。</span><span class="sxs-lookup"><span data-stu-id="dcd01-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dcd01-133">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="dcd01-133">-ShareName</span></span>
<span data-ttu-id="dcd01-134">指定此 Cmdlet 移除原則的儲存空間份額名稱。</span><span class="sxs-lookup"><span data-stu-id="dcd01-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd01-135">-確認</span><span class="sxs-lookup"><span data-stu-id="dcd01-135">-Confirm</span></span>
<span data-ttu-id="dcd01-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcd01-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd01-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd01-137">-WhatIf</span></span>
<span data-ttu-id="dcd01-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcd01-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd01-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcd01-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd01-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd01-140">CommonParameters</span></span>
<span data-ttu-id="dcd01-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcd01-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd01-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dcd01-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd01-143">輸入</span><span class="sxs-lookup"><span data-stu-id="dcd01-143">INPUTS</span></span>

### <span data-ttu-id="dcd01-144">System.object</span><span class="sxs-lookup"><span data-stu-id="dcd01-144">System.String</span></span>

### <span data-ttu-id="dcd01-145">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="dcd01-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dcd01-146">輸出</span><span class="sxs-lookup"><span data-stu-id="dcd01-146">OUTPUTS</span></span>

### <span data-ttu-id="dcd01-147">System.object</span><span class="sxs-lookup"><span data-stu-id="dcd01-147">System.Boolean</span></span>

## <span data-ttu-id="dcd01-148">筆記</span><span class="sxs-lookup"><span data-stu-id="dcd01-148">NOTES</span></span>

## <span data-ttu-id="dcd01-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcd01-149">RELATED LINKS</span></span>

[<span data-ttu-id="dcd01-150">AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd01-150">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="dcd01-151">新-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd01-151">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="dcd01-152">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="dcd01-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dcd01-153">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd01-153">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
