---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443540"
---
# <span data-ttu-id="27be5-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27be5-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="27be5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27be5-102">SYNOPSIS</span></span>
<span data-ttu-id="27be5-103">設定 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="27be5-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="27be5-104">句法</span><span class="sxs-lookup"><span data-stu-id="27be5-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27be5-105">說明</span><span class="sxs-lookup"><span data-stu-id="27be5-105">DESCRIPTION</span></span>
<span data-ttu-id="27be5-106">**AzureStorageTableStoredAccessPolicy** Cmdlet 設定 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="27be5-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="27be5-107">示例</span><span class="sxs-lookup"><span data-stu-id="27be5-107">EXAMPLES</span></span>

### <span data-ttu-id="27be5-108">範例1：以完整許可權在資料表中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="27be5-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="27be5-109">這個命令會為名為 MyTable 的儲存空間資料表設定一個名為 Policy08 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="27be5-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="27be5-110">參數</span><span class="sxs-lookup"><span data-stu-id="27be5-110">PARAMETERS</span></span>

### <span data-ttu-id="27be5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="27be5-111">-Context</span></span>
<span data-ttu-id="27be5-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="27be5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="27be5-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27be5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="27be5-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="27be5-114">-ExpiryTime</span></span>
<span data-ttu-id="27be5-115">指定儲存的存取原則到期的時間。</span><span class="sxs-lookup"><span data-stu-id="27be5-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="27be5-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="27be5-116">-NoExpiryTime</span></span>
<span data-ttu-id="27be5-117">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="27be5-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="27be5-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="27be5-118">-NoStartTime</span></span>
<span data-ttu-id="27be5-119">表示 [開始時間] 設定為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="27be5-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="27be5-120">-許可權</span><span class="sxs-lookup"><span data-stu-id="27be5-120">-Permission</span></span>
<span data-ttu-id="27be5-121">指定此儲存空間表格的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="27be5-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="27be5-122">-原則</span><span class="sxs-lookup"><span data-stu-id="27be5-122">-Policy</span></span>
<span data-ttu-id="27be5-123">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="27be5-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="27be5-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="27be5-124">-StartTime</span></span>
<span data-ttu-id="27be5-125">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="27be5-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="27be5-126">-資料表</span><span class="sxs-lookup"><span data-stu-id="27be5-126">-Table</span></span>
<span data-ttu-id="27be5-127">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="27be5-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="27be5-128">-確認</span><span class="sxs-lookup"><span data-stu-id="27be5-128">-Confirm</span></span>
<span data-ttu-id="27be5-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="27be5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27be5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27be5-130">-WhatIf</span></span>
<span data-ttu-id="27be5-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27be5-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27be5-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27be5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27be5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27be5-133">CommonParameters</span></span>
<span data-ttu-id="27be5-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27be5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27be5-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27be5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27be5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="27be5-136">INPUTS</span></span>

## <span data-ttu-id="27be5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="27be5-137">OUTPUTS</span></span>

## <span data-ttu-id="27be5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="27be5-138">NOTES</span></span>

## <span data-ttu-id="27be5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="27be5-139">RELATED LINKS</span></span>

[<span data-ttu-id="27be5-140">AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27be5-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="27be5-141">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="27be5-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="27be5-142">新-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27be5-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="27be5-143">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27be5-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
