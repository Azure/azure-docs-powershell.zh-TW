---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 4d2828351c4007e57fd8c7534e88aa3be5543199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911837"
---
# <span data-ttu-id="d0c9e-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c9e-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d0c9e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c9e-103">從 Azure 儲存容器移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="d0c9e-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0c9e-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c9e-105">描述</span><span class="sxs-lookup"><span data-stu-id="d0c9e-105">DESCRIPTION</span></span>
<span data-ttu-id="d0c9e-106">**Remove-AzStorageContainerStoredAccessPolicy** Cmdlet 會從 Azure 儲存容器移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="d0c9e-107">例子</span><span class="sxs-lookup"><span data-stu-id="d0c9e-107">EXAMPLES</span></span>

### <span data-ttu-id="d0c9e-108">範例 1：從儲存容器移除儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="d0c9e-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="d0c9e-109">此命令會從名為 MyContainer 的儲存容器移除名為 Policy03 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="d0c9e-110">參數</span><span class="sxs-lookup"><span data-stu-id="d0c9e-110">PARAMETERS</span></span>

### <span data-ttu-id="d0c9e-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0c9e-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d0c9e-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d0c9e-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d0c9e-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d0c9e-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d0c9e-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d0c9e-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d0c9e-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d0c9e-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d0c9e-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d0c9e-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d0c9e-121">-Container</span><span class="sxs-lookup"><span data-stu-id="d0c9e-121">-Container</span></span>
<span data-ttu-id="d0c9e-122">指定 Azure 儲存容器名稱。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="d0c9e-123">-內容</span><span class="sxs-lookup"><span data-stu-id="d0c9e-123">-Context</span></span>
<span data-ttu-id="d0c9e-124">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d0c9e-125">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0c9e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c9e-126">-DefaultProfile</span></span>
<span data-ttu-id="d0c9e-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c9e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0c9e-128">-PassThru</span></span>
<span data-ttu-id="d0c9e-129">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d0c9e-130">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d0c9e-131">-策略</span><span class="sxs-lookup"><span data-stu-id="d0c9e-131">-Policy</span></span>
<span data-ttu-id="d0c9e-132">指定此 Cmdlet 移除的已儲存存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0c9e-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0c9e-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d0c9e-134">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d0c9e-135">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d0c9e-136">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d0c9e-137">-確認</span><span class="sxs-lookup"><span data-stu-id="d0c9e-137">-Confirm</span></span>
<span data-ttu-id="d0c9e-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0c9e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0c9e-139">-WhatIf</span></span>
<span data-ttu-id="d0c9e-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0c9e-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0c9e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c9e-142">CommonParameters</span></span>
<span data-ttu-id="d0c9e-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c9e-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d0c9e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c9e-145">輸入</span><span class="sxs-lookup"><span data-stu-id="d0c9e-145">INPUTS</span></span>

### <span data-ttu-id="d0c9e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d0c9e-146">System.String</span></span>

### <span data-ttu-id="d0c9e-147">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="d0c9e-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0c9e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="d0c9e-148">OUTPUTS</span></span>

### <span data-ttu-id="d0c9e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0c9e-149">System.Boolean</span></span>

## <span data-ttu-id="d0c9e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="d0c9e-150">NOTES</span></span>

## <span data-ttu-id="d0c9e-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0c9e-151">RELATED LINKS</span></span>

[<span data-ttu-id="d0c9e-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c9e-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d0c9e-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c9e-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d0c9e-154">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="d0c9e-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d0c9e-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c9e-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
