---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e2e88cc676fddd6da7ce460fbe0d9d770756c4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907458"
---
# <span data-ttu-id="66835-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66835-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="66835-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66835-102">SYNOPSIS</span></span>
<span data-ttu-id="66835-103">設定 Azure 儲存佇列的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="66835-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="66835-104">語法</span><span class="sxs-lookup"><span data-stu-id="66835-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66835-105">描述</span><span class="sxs-lookup"><span data-stu-id="66835-105">DESCRIPTION</span></span>
<span data-ttu-id="66835-106">**Set-AzStorageQueueStoredAccessPolicy** Cmdlet 會設定 Azure 儲存佇列的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="66835-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="66835-107">例子</span><span class="sxs-lookup"><span data-stu-id="66835-107">EXAMPLES</span></span>

### <span data-ttu-id="66835-108">範例 1：在具有完整許可權的佇列中設定儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="66835-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="66835-109">此命令會針對名為 MyQueue 的儲存佇列設定名為 Policy07 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="66835-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="66835-110">參數</span><span class="sxs-lookup"><span data-stu-id="66835-110">PARAMETERS</span></span>

### <span data-ttu-id="66835-111">-內容</span><span class="sxs-lookup"><span data-stu-id="66835-111">-Context</span></span>
<span data-ttu-id="66835-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="66835-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="66835-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66835-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="66835-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66835-114">-DefaultProfile</span></span>
<span data-ttu-id="66835-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66835-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66835-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="66835-116">-ExpiryTime</span></span>
<span data-ttu-id="66835-117">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="66835-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="66835-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="66835-118">-NoExpiryTime</span></span>
<span data-ttu-id="66835-119">表示存取策略沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="66835-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="66835-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="66835-120">-NoStartTime</span></span>
<span data-ttu-id="66835-121">表示此 Cmdlet 會設定要$Null。</span><span class="sxs-lookup"><span data-stu-id="66835-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="66835-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="66835-122">-Permission</span></span>
<span data-ttu-id="66835-123">指定儲存存取策略中存取儲存佇列的許可權。</span><span class="sxs-lookup"><span data-stu-id="66835-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="66835-124">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="66835-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="66835-125">-策略</span><span class="sxs-lookup"><span data-stu-id="66835-125">-Policy</span></span>
<span data-ttu-id="66835-126">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="66835-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="66835-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="66835-127">-Queue</span></span>
<span data-ttu-id="66835-128">指定 Azure 儲存佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="66835-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="66835-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="66835-129">-StartTime</span></span>
<span data-ttu-id="66835-130">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="66835-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="66835-131">-確認</span><span class="sxs-lookup"><span data-stu-id="66835-131">-Confirm</span></span>
<span data-ttu-id="66835-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66835-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66835-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66835-133">-WhatIf</span></span>
<span data-ttu-id="66835-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66835-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66835-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66835-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66835-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66835-136">CommonParameters</span></span>
<span data-ttu-id="66835-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66835-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66835-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="66835-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66835-139">輸入</span><span class="sxs-lookup"><span data-stu-id="66835-139">INPUTS</span></span>

### <span data-ttu-id="66835-140">System.String</span><span class="sxs-lookup"><span data-stu-id="66835-140">System.String</span></span>

### <span data-ttu-id="66835-141">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="66835-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66835-142">輸出</span><span class="sxs-lookup"><span data-stu-id="66835-142">OUTPUTS</span></span>

### <span data-ttu-id="66835-143">System.String</span><span class="sxs-lookup"><span data-stu-id="66835-143">System.String</span></span>

## <span data-ttu-id="66835-144">筆記</span><span class="sxs-lookup"><span data-stu-id="66835-144">NOTES</span></span>

## <span data-ttu-id="66835-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="66835-145">RELATED LINKS</span></span>

[<span data-ttu-id="66835-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66835-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="66835-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66835-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="66835-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="66835-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
