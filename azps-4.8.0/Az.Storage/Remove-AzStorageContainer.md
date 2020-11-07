---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: a6ea7a2686d084b241e1ba3ff5c513c0d03128c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93968955"
---
# <span data-ttu-id="3a06b-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a06b-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="3a06b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a06b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a06b-103">移除指定的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="3a06b-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="3a06b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a06b-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a06b-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a06b-105">DESCRIPTION</span></span>
<span data-ttu-id="3a06b-106">**AzStorageContainer** Cmdlet 會在 Azure 中移除指定的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="3a06b-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="3a06b-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a06b-107">EXAMPLES</span></span>

### <span data-ttu-id="3a06b-108">範例1：移除容器</span><span class="sxs-lookup"><span data-stu-id="3a06b-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="3a06b-109">這個範例會移除名為 MyTestContainer 的容器。</span><span class="sxs-lookup"><span data-stu-id="3a06b-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="3a06b-110">參數</span><span class="sxs-lookup"><span data-stu-id="3a06b-110">PARAMETERS</span></span>

### <span data-ttu-id="3a06b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a06b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3a06b-112">指定一個服務要求的用戶端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a06b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3a06b-113">如果上一個呼叫在指定的時間間隔中失敗，這個 Cmdlet 會將要求重試。</span><span class="sxs-lookup"><span data-stu-id="3a06b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3a06b-114">如果這個 Cmdlet 在間隔到期前沒有收到成功的回應，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a06b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3a06b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3a06b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3a06b-116">指定最大併發網路通話數。</span><span class="sxs-lookup"><span data-stu-id="3a06b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3a06b-117">您可以使用這個參數，透過指定併發網路呼叫的最大數量來限制併發 CPU 和頻寬使用量。</span><span class="sxs-lookup"><span data-stu-id="3a06b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3a06b-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="3a06b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3a06b-119">這個參數可協助減少低頻寬環境中的網路連線問題，例如 100 kb/秒。</span><span class="sxs-lookup"><span data-stu-id="3a06b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3a06b-120">預設值為10。</span><span class="sxs-lookup"><span data-stu-id="3a06b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3a06b-121">-內容</span><span class="sxs-lookup"><span data-stu-id="3a06b-121">-Context</span></span>
<span data-ttu-id="3a06b-122">指定您要移除之容器的內容。</span><span class="sxs-lookup"><span data-stu-id="3a06b-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="3a06b-123">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="3a06b-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="3a06b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a06b-124">-DefaultProfile</span></span>
<span data-ttu-id="3a06b-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a06b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a06b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3a06b-126">-Force</span></span>
<span data-ttu-id="3a06b-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3a06b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a06b-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a06b-128">-Name</span></span>
<span data-ttu-id="3a06b-129">指定要移除之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a06b-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a06b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a06b-130">-PassThru</span></span>
<span data-ttu-id="3a06b-131">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="3a06b-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3a06b-132">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3a06b-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3a06b-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3a06b-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3a06b-134">指定要求的服務端超時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a06b-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3a06b-135">如果所指定的間隔在服務處理要求之前就已到期，儲存服務就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a06b-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3a06b-136">-確認</span><span class="sxs-lookup"><span data-stu-id="3a06b-136">-Confirm</span></span>
<span data-ttu-id="3a06b-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a06b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a06b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a06b-138">-WhatIf</span></span>
<span data-ttu-id="3a06b-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a06b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a06b-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a06b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a06b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a06b-141">CommonParameters</span></span>
<span data-ttu-id="3a06b-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a06b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a06b-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a06b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a06b-144">輸入</span><span class="sxs-lookup"><span data-stu-id="3a06b-144">INPUTS</span></span>

### <span data-ttu-id="3a06b-145">System.object</span><span class="sxs-lookup"><span data-stu-id="3a06b-145">System.String</span></span>

### <span data-ttu-id="3a06b-146">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="3a06b-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3a06b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="3a06b-147">OUTPUTS</span></span>

### <span data-ttu-id="3a06b-148">System.object</span><span class="sxs-lookup"><span data-stu-id="3a06b-148">System.Boolean</span></span>

## <span data-ttu-id="3a06b-149">筆記</span><span class="sxs-lookup"><span data-stu-id="3a06b-149">NOTES</span></span>

## <span data-ttu-id="3a06b-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a06b-150">RELATED LINKS</span></span>

[<span data-ttu-id="3a06b-151">AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a06b-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="3a06b-152">新-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a06b-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
