---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454992"
---
# <span data-ttu-id="53d0f-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53d0f-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="53d0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="53d0f-103">針對 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="53d0f-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53d0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="53d0f-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53d0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="53d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="53d0f-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="53d0f-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="53d0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="53d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="53d0f-108">範例1：以完整許可權在佇列中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="53d0f-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="53d0f-109">這個命令會為名為 MyQueue 的儲存佇列設定一個名為 Policy07 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="53d0f-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="53d0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="53d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="53d0f-111">-內容</span><span class="sxs-lookup"><span data-stu-id="53d0f-111">-Context</span></span>
<span data-ttu-id="53d0f-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="53d0f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="53d0f-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53d0f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="53d0f-114">-ExpiryTime</span></span>
<span data-ttu-id="53d0f-115">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="53d0f-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="53d0f-116">-NoExpiryTime</span></span>
<span data-ttu-id="53d0f-117">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="53d0f-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="53d0f-118">-NoStartTime</span></span>
<span data-ttu-id="53d0f-119">表示此 Cmdlet 會將開始時間設定為 $Null。</span><span class="sxs-lookup"><span data-stu-id="53d0f-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-120">-許可權</span><span class="sxs-lookup"><span data-stu-id="53d0f-120">-Permission</span></span>
<span data-ttu-id="53d0f-121">指定儲存的存取原則中的許可權，以存取儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="53d0f-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-122">-原則</span><span class="sxs-lookup"><span data-stu-id="53d0f-122">-Policy</span></span>
<span data-ttu-id="53d0f-123">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="53d0f-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="53d0f-124">-Queue</span></span>
<span data-ttu-id="53d0f-125">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="53d0f-125">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="53d0f-126">-StartTime</span></span>
<span data-ttu-id="53d0f-127">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="53d0f-127">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="53d0f-128">-Confirm</span></span>
<span data-ttu-id="53d0f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53d0f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53d0f-130">-WhatIf</span></span>
<span data-ttu-id="53d0f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53d0f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53d0f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53d0f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53d0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d0f-133">CommonParameters</span></span>
<span data-ttu-id="53d0f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53d0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d0f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53d0f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d0f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="53d0f-136">INPUTS</span></span>

### <span data-ttu-id="53d0f-137">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="53d0f-137">IStorageContext</span></span>

<span data-ttu-id="53d0f-138">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53d0f-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="53d0f-139">字串</span><span class="sxs-lookup"><span data-stu-id="53d0f-139">String</span></span>

<span data-ttu-id="53d0f-140">形參 "Queue" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53d0f-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="53d0f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="53d0f-141">OUTPUTS</span></span>

### <span data-ttu-id="53d0f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="53d0f-142">System.String</span></span>

## <span data-ttu-id="53d0f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="53d0f-143">NOTES</span></span>

## <span data-ttu-id="53d0f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="53d0f-144">RELATED LINKS</span></span>

[<span data-ttu-id="53d0f-145">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53d0f-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="53d0f-146">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53d0f-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="53d0f-147">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53d0f-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
