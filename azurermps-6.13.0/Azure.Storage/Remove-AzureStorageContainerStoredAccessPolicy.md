---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: b0a0ffcc1d4742da62c983ed9429df46569f85be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452931"
---
# <span data-ttu-id="e9068-101">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9068-101">Remove-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="e9068-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9068-102">SYNOPSIS</span></span>
<span data-ttu-id="e9068-103">從 Azure 儲存體容器移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="e9068-103">Removes a stored access policy from an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9068-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9068-104">SYNTAX</span></span>

```
Remove-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9068-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9068-105">DESCRIPTION</span></span>
<span data-ttu-id="e9068-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet 會從 Azure 儲存體容器中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="e9068-106">The **Remove-AzureStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="e9068-107">示例</span><span class="sxs-lookup"><span data-stu-id="e9068-107">EXAMPLES</span></span>

### <span data-ttu-id="e9068-108">範例1：從儲存空間容器移除已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="e9068-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="e9068-109">這個命令會從儲存的容器（名為 MyContainer）移除一個名為 Policy03 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="e9068-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="e9068-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9068-110">PARAMETERS</span></span>

### <span data-ttu-id="e9068-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9068-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e9068-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e9068-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e9068-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="e9068-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e9068-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9068-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e9068-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e9068-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e9068-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="e9068-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e9068-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="e9068-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e9068-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="e9068-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e9068-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="e9068-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e9068-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="e9068-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e9068-121">-容器</span><span class="sxs-lookup"><span data-stu-id="e9068-121">-Container</span></span>
<span data-ttu-id="e9068-122">指定 Azure 儲存空間容器名稱。</span><span class="sxs-lookup"><span data-stu-id="e9068-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="e9068-123">-內容</span><span class="sxs-lookup"><span data-stu-id="e9068-123">-Context</span></span>
<span data-ttu-id="e9068-124">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="e9068-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e9068-125">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9068-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e9068-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9068-126">-DefaultProfile</span></span>
<span data-ttu-id="e9068-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9068-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9068-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9068-128">-PassThru</span></span>
<span data-ttu-id="e9068-129">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="e9068-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e9068-130">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e9068-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e9068-131">-原則</span><span class="sxs-lookup"><span data-stu-id="e9068-131">-Policy</span></span>
<span data-ttu-id="e9068-132">指定此 Cmdlet 移除之已儲存的訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="e9068-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9068-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9068-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e9068-134">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e9068-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e9068-135">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="e9068-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e9068-136">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9068-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e9068-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e9068-137">-Confirm</span></span>
<span data-ttu-id="e9068-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9068-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9068-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9068-139">-WhatIf</span></span>
<span data-ttu-id="e9068-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9068-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9068-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9068-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9068-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9068-142">CommonParameters</span></span>
<span data-ttu-id="e9068-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9068-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9068-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9068-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9068-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e9068-145">INPUTS</span></span>

### <span data-ttu-id="e9068-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e9068-146">System.String</span></span>

### <span data-ttu-id="e9068-147">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="e9068-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9068-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e9068-148">OUTPUTS</span></span>

### <span data-ttu-id="e9068-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e9068-149">System.Boolean</span></span>

## <span data-ttu-id="e9068-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e9068-150">NOTES</span></span>

## <span data-ttu-id="e9068-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9068-151">RELATED LINKS</span></span>

[<span data-ttu-id="e9068-152">AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9068-152">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e9068-153">新-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9068-153">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="e9068-154">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="e9068-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e9068-155">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9068-155">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)