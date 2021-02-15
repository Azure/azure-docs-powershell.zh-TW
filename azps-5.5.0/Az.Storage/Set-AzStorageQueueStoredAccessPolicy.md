---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142412"
---
# <span data-ttu-id="cdb9b-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdb9b-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="cdb9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdb9b-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb9b-103">針對 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="cdb9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cdb9b-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="cdb9b-105">DESCRIPTION</span></span>
<span data-ttu-id="cdb9b-106">**AzStorageQueueStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="cdb9b-107">示例</span><span class="sxs-lookup"><span data-stu-id="cdb9b-107">EXAMPLES</span></span>

### <span data-ttu-id="cdb9b-108">範例1：以完整許可權在佇列中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="cdb9b-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="cdb9b-109">這個命令會為名為 MyQueue 的儲存佇列設定一個名為 Policy07 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="cdb9b-110">參數</span><span class="sxs-lookup"><span data-stu-id="cdb9b-110">PARAMETERS</span></span>

### <span data-ttu-id="cdb9b-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cdb9b-111">-Context</span></span>
<span data-ttu-id="cdb9b-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cdb9b-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cdb9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb9b-114">-DefaultProfile</span></span>
<span data-ttu-id="cdb9b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb9b-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cdb9b-116">-ExpiryTime</span></span>
<span data-ttu-id="cdb9b-117">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="cdb9b-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cdb9b-118">-NoExpiryTime</span></span>
<span data-ttu-id="cdb9b-119">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="cdb9b-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="cdb9b-120">-NoStartTime</span></span>
<span data-ttu-id="cdb9b-121">表示此 Cmdlet 會將開始時間設定為 $Null。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="cdb9b-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="cdb9b-122">-Permission</span></span>
<span data-ttu-id="cdb9b-123">指定儲存的存取原則中的許可權，以存取儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="cdb9b-124">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="cdb9b-125">-原則</span><span class="sxs-lookup"><span data-stu-id="cdb9b-125">-Policy</span></span>
<span data-ttu-id="cdb9b-126">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="cdb9b-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="cdb9b-127">-Queue</span></span>
<span data-ttu-id="cdb9b-128">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="cdb9b-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cdb9b-129">-StartTime</span></span>
<span data-ttu-id="cdb9b-130">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="cdb9b-131">-確認</span><span class="sxs-lookup"><span data-stu-id="cdb9b-131">-Confirm</span></span>
<span data-ttu-id="cdb9b-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb9b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb9b-133">-WhatIf</span></span>
<span data-ttu-id="cdb9b-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdb9b-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb9b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb9b-136">CommonParameters</span></span>
<span data-ttu-id="cdb9b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb9b-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cdb9b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb9b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="cdb9b-139">INPUTS</span></span>

### <span data-ttu-id="cdb9b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="cdb9b-140">System.String</span></span>

### <span data-ttu-id="cdb9b-141">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="cdb9b-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cdb9b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="cdb9b-142">OUTPUTS</span></span>

### <span data-ttu-id="cdb9b-143">System.object</span><span class="sxs-lookup"><span data-stu-id="cdb9b-143">System.String</span></span>

## <span data-ttu-id="cdb9b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="cdb9b-144">NOTES</span></span>

## <span data-ttu-id="cdb9b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdb9b-145">RELATED LINKS</span></span>

[<span data-ttu-id="cdb9b-146">AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdb9b-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="cdb9b-147">新-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdb9b-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="cdb9b-148">移除-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cdb9b-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
