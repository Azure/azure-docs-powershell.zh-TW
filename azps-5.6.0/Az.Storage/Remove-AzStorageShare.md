---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: 5e2021277792bbaf52b6fcf6ffba88d71c854c7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904234"
---
# <span data-ttu-id="1a870-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1a870-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="1a870-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1a870-102">SYNOPSIS</span></span>
<span data-ttu-id="1a870-103">刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="1a870-103">Deletes a file share.</span></span>

## <span data-ttu-id="1a870-104">語法</span><span class="sxs-lookup"><span data-stu-id="1a870-104">SYNTAX</span></span>

### <span data-ttu-id="1a870-105">ShareName (預設) </span><span class="sxs-lookup"><span data-stu-id="1a870-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a870-106">共用</span><span class="sxs-lookup"><span data-stu-id="1a870-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a870-107">描述</span><span class="sxs-lookup"><span data-stu-id="1a870-107">DESCRIPTION</span></span>
<span data-ttu-id="1a870-108">**Remove-AzStorageShare** Cmdlet 會刪除檔案共用。</span><span class="sxs-lookup"><span data-stu-id="1a870-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="1a870-109">例子</span><span class="sxs-lookup"><span data-stu-id="1a870-109">EXAMPLES</span></span>

### <span data-ttu-id="1a870-110">範例 1：移除檔案共用</span><span class="sxs-lookup"><span data-stu-id="1a870-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="1a870-111">此命令會移除名為 ContosoShare06 的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="1a870-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="1a870-112">範例 2：移除檔案共用及其所有快照</span><span class="sxs-lookup"><span data-stu-id="1a870-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="1a870-113">此命令會移除名為 ContosoShare06 的檔案共用及其所有快照。</span><span class="sxs-lookup"><span data-stu-id="1a870-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="1a870-114">參數</span><span class="sxs-lookup"><span data-stu-id="1a870-114">PARAMETERS</span></span>

### <span data-ttu-id="1a870-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a870-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="1a870-116">指定一個服務要求用戶端的時間間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="1a870-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="1a870-117">如果前一個通話在指定的時間間隔內失敗，此 Cmdlet 會重新重試要求。</span><span class="sxs-lookup"><span data-stu-id="1a870-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="1a870-118">如果此 Cmdlet 在間隔經過之前未收到成功回應，此 Cmdlet 會返回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a870-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="1a870-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="1a870-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="1a870-120">指定同時進行的最大網路通話數。</span><span class="sxs-lookup"><span data-stu-id="1a870-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="1a870-121">您可以使用此參數來限制並行，以節流本地 CPU 和頻寬使用量，方法為指定並行網路通話的數量上限。</span><span class="sxs-lookup"><span data-stu-id="1a870-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="1a870-122">指定的值是絕對計數，不會乘以核心計數。</span><span class="sxs-lookup"><span data-stu-id="1a870-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="1a870-123">此參數有助於減少低頻寬環境的網路連接問題，例如每秒 100 KB。</span><span class="sxs-lookup"><span data-stu-id="1a870-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="1a870-124">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="1a870-124">The default value is 10.</span></span>

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

### <span data-ttu-id="1a870-125">-內容</span><span class="sxs-lookup"><span data-stu-id="1a870-125">-Context</span></span>
<span data-ttu-id="1a870-126">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="1a870-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1a870-127">若要取得儲存內容，請使用 [New-AzStorageCoNtext](./New-AzStorageContext.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a870-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a870-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a870-128">-DefaultProfile</span></span>
<span data-ttu-id="1a870-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a870-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a870-130">-強制</span><span class="sxs-lookup"><span data-stu-id="1a870-130">-Force</span></span>
<span data-ttu-id="1a870-131">強制移除共用及其所有快照及所有內容。</span><span class="sxs-lookup"><span data-stu-id="1a870-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="1a870-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="1a870-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="1a870-133">移除檔案共用及其所有快照</span><span class="sxs-lookup"><span data-stu-id="1a870-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="1a870-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a870-134">-Name</span></span>
<span data-ttu-id="1a870-135">指定檔案共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a870-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="1a870-136">此 Cmdlet 會刪除此參數指定的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="1a870-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a870-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a870-137">-PassThru</span></span>
<span data-ttu-id="1a870-138">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="1a870-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1a870-139">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1a870-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1a870-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="1a870-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="1a870-141">指定要求的伺服器部分之時間長度。</span><span class="sxs-lookup"><span data-stu-id="1a870-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="1a870-142">-共用</span><span class="sxs-lookup"><span data-stu-id="1a870-142">-Share</span></span>
<span data-ttu-id="1a870-143">指定 **CloudFileShare** 物件。</span><span class="sxs-lookup"><span data-stu-id="1a870-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="1a870-144">此 Cmdlet 會移除此參數指定的物件。</span><span class="sxs-lookup"><span data-stu-id="1a870-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="1a870-145">若要取得 **CloudFileShare** 物件，請使用 Get-AzStorageShare Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a870-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="1a870-146">此物件包含儲存內容。</span><span class="sxs-lookup"><span data-stu-id="1a870-146">This object contains the storage context.</span></span>
<span data-ttu-id="1a870-147">如果您指定此參數，請勿指定 *CoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="1a870-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a870-148">-確認</span><span class="sxs-lookup"><span data-stu-id="1a870-148">-Confirm</span></span>
<span data-ttu-id="1a870-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1a870-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a870-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a870-150">-WhatIf</span></span>
<span data-ttu-id="1a870-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a870-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a870-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a870-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a870-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a870-153">CommonParameters</span></span>
<span data-ttu-id="1a870-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1a870-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a870-155">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1a870-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a870-156">輸入</span><span class="sxs-lookup"><span data-stu-id="1a870-156">INPUTS</span></span>

### <span data-ttu-id="1a870-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1a870-157">System.String</span></span>

### <span data-ttu-id="1a870-158">Microsoft.Azure.storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="1a870-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="1a870-159">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="1a870-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1a870-160">輸出</span><span class="sxs-lookup"><span data-stu-id="1a870-160">OUTPUTS</span></span>

### <span data-ttu-id="1a870-161">Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="1a870-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="1a870-162">筆記</span><span class="sxs-lookup"><span data-stu-id="1a870-162">NOTES</span></span>

## <span data-ttu-id="1a870-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a870-163">RELATED LINKS</span></span>

[<span data-ttu-id="1a870-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1a870-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="1a870-165">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="1a870-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1a870-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="1a870-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
