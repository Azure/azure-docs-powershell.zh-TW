---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: e2d408e54aa4b4e2de766d4f4e058d2edd22cb22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906458"
---
# <span data-ttu-id="eab93-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eab93-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="eab93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="eab93-102">SYNOPSIS</span></span>
<span data-ttu-id="eab93-103">移除指定的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="eab93-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="eab93-104">語法</span><span class="sxs-lookup"><span data-stu-id="eab93-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eab93-105">描述</span><span class="sxs-lookup"><span data-stu-id="eab93-105">DESCRIPTION</span></span>
<span data-ttu-id="eab93-106">**Remove-AzStorageContainer Cmdlet** 會移除 Azure 中指定的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="eab93-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="eab93-107">例子</span><span class="sxs-lookup"><span data-stu-id="eab93-107">EXAMPLES</span></span>

### <span data-ttu-id="eab93-108">範例 1：移除容器</span><span class="sxs-lookup"><span data-stu-id="eab93-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="eab93-109">此範例會移除名為 MyTestContainer 的容器。</span><span class="sxs-lookup"><span data-stu-id="eab93-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="eab93-110">參數</span><span class="sxs-lookup"><span data-stu-id="eab93-110">PARAMETERS</span></span>

### <span data-ttu-id="eab93-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eab93-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eab93-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="eab93-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eab93-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="eab93-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eab93-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="eab93-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eab93-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eab93-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eab93-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="eab93-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eab93-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="eab93-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eab93-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="eab93-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eab93-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="eab93-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eab93-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="eab93-120">The default value is 10.</span></span>

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

### <span data-ttu-id="eab93-121">-內容</span><span class="sxs-lookup"><span data-stu-id="eab93-121">-Context</span></span>
<span data-ttu-id="eab93-122">指定要移除之容器的上下文。</span><span class="sxs-lookup"><span data-stu-id="eab93-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="eab93-123">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="eab93-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="eab93-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab93-124">-DefaultProfile</span></span>
<span data-ttu-id="eab93-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="eab93-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab93-126">-強制</span><span class="sxs-lookup"><span data-stu-id="eab93-126">-Force</span></span>
<span data-ttu-id="eab93-127">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="eab93-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eab93-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="eab93-128">-Name</span></span>
<span data-ttu-id="eab93-129">指定要移除的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="eab93-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="eab93-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eab93-130">-PassThru</span></span>
<span data-ttu-id="eab93-131">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="eab93-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eab93-132">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="eab93-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eab93-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eab93-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eab93-134">指定服務端要求的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="eab93-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="eab93-135">如果指定的時間間隔在服務處理要求之前已經過，儲存服務會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="eab93-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="eab93-136">-確認</span><span class="sxs-lookup"><span data-stu-id="eab93-136">-Confirm</span></span>
<span data-ttu-id="eab93-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="eab93-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eab93-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab93-138">-WhatIf</span></span>
<span data-ttu-id="eab93-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eab93-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eab93-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eab93-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eab93-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab93-141">CommonParameters</span></span>
<span data-ttu-id="eab93-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="eab93-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab93-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="eab93-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab93-144">輸入</span><span class="sxs-lookup"><span data-stu-id="eab93-144">INPUTS</span></span>

### <span data-ttu-id="eab93-145">System.String</span><span class="sxs-lookup"><span data-stu-id="eab93-145">System.String</span></span>

### <span data-ttu-id="eab93-146">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="eab93-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eab93-147">輸出</span><span class="sxs-lookup"><span data-stu-id="eab93-147">OUTPUTS</span></span>

### <span data-ttu-id="eab93-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eab93-148">System.Boolean</span></span>

## <span data-ttu-id="eab93-149">筆記</span><span class="sxs-lookup"><span data-stu-id="eab93-149">NOTES</span></span>

## <span data-ttu-id="eab93-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="eab93-150">RELATED LINKS</span></span>

[<span data-ttu-id="eab93-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eab93-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="eab93-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eab93-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
