---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 9a6702b59bbe2e0305966cd9a1323edc120e86c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904233"
---
# <span data-ttu-id="29e7b-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="29e7b-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="29e7b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="29e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="29e7b-103">從儲存空間共用移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="29e7b-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="29e7b-104">語法</span><span class="sxs-lookup"><span data-stu-id="29e7b-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29e7b-105">描述</span><span class="sxs-lookup"><span data-stu-id="29e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="29e7b-106">**Remove-AzStorageSharedAccessPolicy** Cmdlet 會從 Azure 儲存空間共用移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="29e7b-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="29e7b-107">例子</span><span class="sxs-lookup"><span data-stu-id="29e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="29e7b-108">範例 1：從 Azure 儲存空間共用移除儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="29e7b-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="29e7b-109">此命令會從 ContosoShare 移除名為 GeneralPolicy 的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="29e7b-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="29e7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="29e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="29e7b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29e7b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="29e7b-112">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="29e7b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="29e7b-113">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="29e7b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="29e7b-114">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="29e7b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="29e7b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="29e7b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="29e7b-116">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="29e7b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="29e7b-117">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="29e7b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="29e7b-118">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="29e7b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="29e7b-119">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="29e7b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="29e7b-120">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="29e7b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="29e7b-121">-內容</span><span class="sxs-lookup"><span data-stu-id="29e7b-121">-Context</span></span>
<span data-ttu-id="29e7b-122">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="29e7b-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="29e7b-123">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29e7b-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="29e7b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e7b-124">-DefaultProfile</span></span>
<span data-ttu-id="29e7b-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="29e7b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29e7b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29e7b-126">-PassThru</span></span>
<span data-ttu-id="29e7b-127">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="29e7b-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="29e7b-128">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="29e7b-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="29e7b-129">-策略</span><span class="sxs-lookup"><span data-stu-id="29e7b-129">-Policy</span></span>
<span data-ttu-id="29e7b-130">指定此 Cmdlet 移除的已儲存存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="29e7b-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="29e7b-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="29e7b-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="29e7b-132">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="29e7b-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="29e7b-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="29e7b-133">-ShareName</span></span>
<span data-ttu-id="29e7b-134">指定此 Cmdlet 會移除該策略的儲存空間共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="29e7b-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="29e7b-135">-確認</span><span class="sxs-lookup"><span data-stu-id="29e7b-135">-Confirm</span></span>
<span data-ttu-id="29e7b-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="29e7b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29e7b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e7b-137">-WhatIf</span></span>
<span data-ttu-id="29e7b-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29e7b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29e7b-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29e7b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29e7b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e7b-140">CommonParameters</span></span>
<span data-ttu-id="29e7b-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="29e7b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e7b-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="29e7b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e7b-143">輸入</span><span class="sxs-lookup"><span data-stu-id="29e7b-143">INPUTS</span></span>

### <span data-ttu-id="29e7b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="29e7b-144">System.String</span></span>

### <span data-ttu-id="29e7b-145">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="29e7b-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="29e7b-146">輸出</span><span class="sxs-lookup"><span data-stu-id="29e7b-146">OUTPUTS</span></span>

### <span data-ttu-id="29e7b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29e7b-147">System.Boolean</span></span>

## <span data-ttu-id="29e7b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="29e7b-148">NOTES</span></span>

## <span data-ttu-id="29e7b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="29e7b-149">RELATED LINKS</span></span>

[<span data-ttu-id="29e7b-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="29e7b-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="29e7b-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="29e7b-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="29e7b-152">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="29e7b-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="29e7b-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="29e7b-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
