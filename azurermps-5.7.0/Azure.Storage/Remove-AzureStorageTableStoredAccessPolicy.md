---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: a9e1290c5933d54481c57b051e170568653eee5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451552"
---
# <span data-ttu-id="8ec3a-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ec3a-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="8ec3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ec3a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec3a-103">從 Azure 儲存空間資料表移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ec3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ec3a-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ec3a-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec3a-106">**AzureStorageTableStoredAccessPolicy** Cmdlet 會從 Azure 儲存空間資料表中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="8ec3a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ec3a-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec3a-108">範例1：從儲存資料表移除儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="8ec3a-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="8ec3a-109">這個命令會從名為 MyTable 的存儲資料表中移除名為 Policy05 的原則。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="8ec3a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8ec3a-110">PARAMETERS</span></span>

### <span data-ttu-id="8ec3a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="8ec3a-111">-Context</span></span>
<span data-ttu-id="8ec3a-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8ec3a-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8ec3a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ec3a-114">-PassThru</span></span>
<span data-ttu-id="8ec3a-115">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8ec3a-116">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8ec3a-117">-原則</span><span class="sxs-lookup"><span data-stu-id="8ec3a-117">-Policy</span></span>
<span data-ttu-id="8ec3a-118">指定此 Cmdlet 移除之已儲存的訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec3a-119">-資料表</span><span class="sxs-lookup"><span data-stu-id="8ec3a-119">-Table</span></span>
<span data-ttu-id="8ec3a-120">指定 Azure 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec3a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8ec3a-121">-Confirm</span></span>
<span data-ttu-id="8ec3a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec3a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec3a-123">-WhatIf</span></span>
<span data-ttu-id="8ec3a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec3a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec3a-126">CommonParameters</span></span>
<span data-ttu-id="8ec3a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec3a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ec3a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec3a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8ec3a-129">INPUTS</span></span>

### <span data-ttu-id="8ec3a-130">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8ec3a-130">IStorageContext</span></span>

<span data-ttu-id="8ec3a-131">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8ec3a-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8ec3a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8ec3a-132">OUTPUTS</span></span>

### <span data-ttu-id="8ec3a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8ec3a-133">System.Boolean</span></span>

## <span data-ttu-id="8ec3a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8ec3a-134">NOTES</span></span>

## <span data-ttu-id="8ec3a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ec3a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8ec3a-136">AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ec3a-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8ec3a-137">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8ec3a-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8ec3a-138">新-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ec3a-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8ec3a-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8ec3a-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
