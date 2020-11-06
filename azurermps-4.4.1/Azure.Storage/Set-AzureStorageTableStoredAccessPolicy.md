---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450971"
---
# <span data-ttu-id="ee66e-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee66e-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ee66e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee66e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee66e-103">設定 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ee66e-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee66e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee66e-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee66e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee66e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee66e-106">**AzureStorageTableStoredAccessPolicy** Cmdlet 設定 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="ee66e-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="ee66e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ee66e-107">EXAMPLES</span></span>

### <span data-ttu-id="ee66e-108">範例1：以完整許可權在資料表中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="ee66e-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="ee66e-109">這個命令會為名為 MyTable 的儲存空間資料表設定一個名為 Policy08 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="ee66e-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="ee66e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ee66e-110">PARAMETERS</span></span>

### <span data-ttu-id="ee66e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ee66e-111">-Context</span></span>
<span data-ttu-id="ee66e-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ee66e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ee66e-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee66e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee66e-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee66e-114">-ExpiryTime</span></span>
<span data-ttu-id="ee66e-115">指定儲存的存取原則到期的時間。</span><span class="sxs-lookup"><span data-stu-id="ee66e-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="ee66e-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ee66e-116">-NoExpiryTime</span></span>
<span data-ttu-id="ee66e-117">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="ee66e-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="ee66e-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="ee66e-118">-NoStartTime</span></span>
<span data-ttu-id="ee66e-119">表示 [開始時間] 設定為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="ee66e-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="ee66e-120">-許可權</span><span class="sxs-lookup"><span data-stu-id="ee66e-120">-Permission</span></span>
<span data-ttu-id="ee66e-121">指定儲存的存取原則中的許可權來存取儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="ee66e-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="ee66e-122">-原則</span><span class="sxs-lookup"><span data-stu-id="ee66e-122">-Policy</span></span>
<span data-ttu-id="ee66e-123">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="ee66e-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="ee66e-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ee66e-124">-StartTime</span></span>
<span data-ttu-id="ee66e-125">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="ee66e-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ee66e-126">-資料表</span><span class="sxs-lookup"><span data-stu-id="ee66e-126">-Table</span></span>
<span data-ttu-id="ee66e-127">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ee66e-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="ee66e-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ee66e-128">-Confirm</span></span>
<span data-ttu-id="ee66e-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee66e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee66e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee66e-130">-WhatIf</span></span>
<span data-ttu-id="ee66e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee66e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee66e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee66e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee66e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee66e-133">CommonParameters</span></span>
<span data-ttu-id="ee66e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee66e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee66e-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee66e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee66e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ee66e-136">INPUTS</span></span>

### <span data-ttu-id="ee66e-137">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ee66e-137">IStorageContext</span></span>

<span data-ttu-id="ee66e-138">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ee66e-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ee66e-139">字串</span><span class="sxs-lookup"><span data-stu-id="ee66e-139">String</span></span>

<span data-ttu-id="ee66e-140">形參 "Table" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ee66e-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ee66e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ee66e-141">OUTPUTS</span></span>

### <span data-ttu-id="ee66e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ee66e-142">System.String</span></span>

## <span data-ttu-id="ee66e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ee66e-143">NOTES</span></span>

## <span data-ttu-id="ee66e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee66e-144">RELATED LINKS</span></span>

[<span data-ttu-id="ee66e-145">AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee66e-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ee66e-146">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ee66e-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ee66e-147">新-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee66e-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ee66e-148">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ee66e-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
