---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4e1b58e2ca2586ada574b55a03287d1cc5915b6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802629"
---
# <span data-ttu-id="b3199-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3199-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="b3199-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3199-102">SYNOPSIS</span></span>
<span data-ttu-id="b3199-103">針對 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b3199-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3199-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3199-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3199-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3199-105">DESCRIPTION</span></span>
<span data-ttu-id="b3199-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b3199-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="b3199-107">示例</span><span class="sxs-lookup"><span data-stu-id="b3199-107">EXAMPLES</span></span>

### <span data-ttu-id="b3199-108">範例1：以完整許可權在佇列中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="b3199-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="b3199-109">這個命令會為名為 MyQueue 的儲存佇列設定一個名為 Policy07 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="b3199-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="b3199-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3199-110">PARAMETERS</span></span>

### <span data-ttu-id="b3199-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b3199-111">-Context</span></span>
<span data-ttu-id="b3199-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b3199-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b3199-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3199-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b3199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3199-114">-DefaultProfile</span></span>
<span data-ttu-id="b3199-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3199-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3199-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b3199-116">-ExpiryTime</span></span>
<span data-ttu-id="b3199-117">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="b3199-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="b3199-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b3199-118">-NoExpiryTime</span></span>
<span data-ttu-id="b3199-119">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="b3199-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="b3199-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="b3199-120">-NoStartTime</span></span>
<span data-ttu-id="b3199-121">表示此 Cmdlet 會將開始時間設定為 $Null。</span><span class="sxs-lookup"><span data-stu-id="b3199-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="b3199-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="b3199-122">-Permission</span></span>
<span data-ttu-id="b3199-123">指定儲存的存取原則中的許可權，以存取儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="b3199-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="b3199-124">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="b3199-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b3199-125">-原則</span><span class="sxs-lookup"><span data-stu-id="b3199-125">-Policy</span></span>
<span data-ttu-id="b3199-126">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3199-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="b3199-127">-佇列</span><span class="sxs-lookup"><span data-stu-id="b3199-127">-Queue</span></span>
<span data-ttu-id="b3199-128">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="b3199-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="b3199-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b3199-129">-StartTime</span></span>
<span data-ttu-id="b3199-130">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="b3199-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="b3199-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b3199-131">-Confirm</span></span>
<span data-ttu-id="b3199-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3199-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3199-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3199-133">-WhatIf</span></span>
<span data-ttu-id="b3199-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3199-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3199-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3199-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3199-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3199-136">CommonParameters</span></span>
<span data-ttu-id="b3199-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3199-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3199-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3199-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3199-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b3199-139">INPUTS</span></span>

### <span data-ttu-id="b3199-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b3199-140">System.String</span></span>

### <span data-ttu-id="b3199-141">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b3199-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b3199-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b3199-142">OUTPUTS</span></span>

### <span data-ttu-id="b3199-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b3199-143">System.String</span></span>

## <span data-ttu-id="b3199-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b3199-144">NOTES</span></span>

## <span data-ttu-id="b3199-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3199-145">RELATED LINKS</span></span>

[<span data-ttu-id="b3199-146">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3199-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b3199-147">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3199-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b3199-148">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3199-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
