---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443551"
---
# <span data-ttu-id="d9e62-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9e62-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d9e62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9e62-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e62-103">針對 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="d9e62-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="d9e62-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9e62-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9e62-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9e62-105">DESCRIPTION</span></span>
<span data-ttu-id="d9e62-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間佇列設定儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="d9e62-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="d9e62-107">示例</span><span class="sxs-lookup"><span data-stu-id="d9e62-107">EXAMPLES</span></span>

### <span data-ttu-id="d9e62-108">範例1：在佇列中設定已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="d9e62-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="d9e62-109">這個命令會為名為 MyQueue 的儲存佇列設定一個名為 Policy07 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="d9e62-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="d9e62-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9e62-110">PARAMETERS</span></span>

### <span data-ttu-id="d9e62-111">-內容</span><span class="sxs-lookup"><span data-stu-id="d9e62-111">-Context</span></span>
<span data-ttu-id="d9e62-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="d9e62-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d9e62-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9e62-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d9e62-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d9e62-114">-ExpiryTime</span></span>
<span data-ttu-id="d9e62-115">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="d9e62-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="d9e62-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d9e62-116">-NoExpiryTime</span></span>
<span data-ttu-id="d9e62-117">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="d9e62-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d9e62-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d9e62-118">-NoStartTime</span></span>
<span data-ttu-id="d9e62-119">表示此 Cmdlet 會將開始時間設定為 $Null。</span><span class="sxs-lookup"><span data-stu-id="d9e62-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="d9e62-120">-許可權</span><span class="sxs-lookup"><span data-stu-id="d9e62-120">-Permission</span></span>
<span data-ttu-id="d9e62-121">指定此儲存佇列的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="d9e62-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="d9e62-122">-原則</span><span class="sxs-lookup"><span data-stu-id="d9e62-122">-Policy</span></span>
<span data-ttu-id="d9e62-123">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="d9e62-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="d9e62-124">-佇列</span><span class="sxs-lookup"><span data-stu-id="d9e62-124">-Queue</span></span>
<span data-ttu-id="d9e62-125">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="d9e62-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d9e62-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d9e62-126">-StartTime</span></span>
<span data-ttu-id="d9e62-127">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="d9e62-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d9e62-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d9e62-128">-Confirm</span></span>
<span data-ttu-id="d9e62-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9e62-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9e62-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9e62-130">-WhatIf</span></span>
<span data-ttu-id="d9e62-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9e62-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9e62-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9e62-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9e62-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e62-133">CommonParameters</span></span>
<span data-ttu-id="d9e62-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9e62-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e62-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9e62-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e62-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d9e62-136">INPUTS</span></span>

## <span data-ttu-id="d9e62-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d9e62-137">OUTPUTS</span></span>

## <span data-ttu-id="d9e62-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d9e62-138">NOTES</span></span>

## <span data-ttu-id="d9e62-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9e62-139">RELATED LINKS</span></span>

[<span data-ttu-id="d9e62-140">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9e62-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d9e62-141">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9e62-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d9e62-142">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9e62-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
