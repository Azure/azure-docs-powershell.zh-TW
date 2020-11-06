---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 94c5bc28ae381227366b5461b51a2da7fd6feccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450139"
---
# <span data-ttu-id="8e42a-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e42a-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8e42a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e42a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e42a-103">從 Azure 儲存空間佇列移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8e42a-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e42a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e42a-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e42a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e42a-105">DESCRIPTION</span></span>
<span data-ttu-id="8e42a-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會從 Azure 儲存空間佇列中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="8e42a-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="8e42a-107">示例</span><span class="sxs-lookup"><span data-stu-id="8e42a-107">EXAMPLES</span></span>

### <span data-ttu-id="8e42a-108">範例1：從儲存佇列移除已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="8e42a-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="8e42a-109">這個命令會從名為 MyQueue 的儲存空間中移除名為 Policy04 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="8e42a-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="8e42a-110">參數</span><span class="sxs-lookup"><span data-stu-id="8e42a-110">PARAMETERS</span></span>

### <span data-ttu-id="8e42a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="8e42a-111">-Context</span></span>
<span data-ttu-id="8e42a-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8e42a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8e42a-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e42a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8e42a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e42a-114">-PassThru</span></span>
<span data-ttu-id="8e42a-115">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="8e42a-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="8e42a-116">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8e42a-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8e42a-117">-原則</span><span class="sxs-lookup"><span data-stu-id="8e42a-117">-Policy</span></span>
<span data-ttu-id="8e42a-118">指定此 Cmdlet 移除之已儲存的訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="8e42a-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8e42a-119">-佇列</span><span class="sxs-lookup"><span data-stu-id="8e42a-119">-Queue</span></span>
<span data-ttu-id="8e42a-120">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="8e42a-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="8e42a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="8e42a-121">-Confirm</span></span>
<span data-ttu-id="8e42a-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e42a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e42a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e42a-123">-WhatIf</span></span>
<span data-ttu-id="8e42a-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e42a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e42a-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e42a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e42a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e42a-126">CommonParameters</span></span>
<span data-ttu-id="8e42a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e42a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e42a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e42a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e42a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8e42a-129">INPUTS</span></span>

### <span data-ttu-id="8e42a-130">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8e42a-130">IStorageContext</span></span>

<span data-ttu-id="8e42a-131">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8e42a-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8e42a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8e42a-132">OUTPUTS</span></span>

### <span data-ttu-id="8e42a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8e42a-133">System.Boolean</span></span>

## <span data-ttu-id="8e42a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8e42a-134">NOTES</span></span>

## <span data-ttu-id="8e42a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e42a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8e42a-136">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e42a-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8e42a-137">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8e42a-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8e42a-138">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e42a-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8e42a-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e42a-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
