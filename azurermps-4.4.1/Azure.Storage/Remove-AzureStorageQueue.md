---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 51ea3111b5010b0e29f7bfd69ed5a8e66e596113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447209"
---
# <span data-ttu-id="62985-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="62985-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="62985-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62985-102">SYNOPSIS</span></span>
<span data-ttu-id="62985-103">移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="62985-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62985-104">句法</span><span class="sxs-lookup"><span data-stu-id="62985-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62985-105">說明</span><span class="sxs-lookup"><span data-stu-id="62985-105">DESCRIPTION</span></span>
<span data-ttu-id="62985-106">**AzureStorageQueue** Cmdlet 會移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="62985-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="62985-107">示例</span><span class="sxs-lookup"><span data-stu-id="62985-107">EXAMPLES</span></span>

### <span data-ttu-id="62985-108">範例1：依名稱移除儲存佇列</span><span class="sxs-lookup"><span data-stu-id="62985-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="62985-109">這個命令會移除名為 ContosoQueue01 的佇列。</span><span class="sxs-lookup"><span data-stu-id="62985-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="62985-110">範例2：移除多個儲存佇列</span><span class="sxs-lookup"><span data-stu-id="62985-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="62985-111">這個命令會移除名稱以 Contoso 為開頭的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="62985-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="62985-112">參數</span><span class="sxs-lookup"><span data-stu-id="62985-112">PARAMETERS</span></span>

### <span data-ttu-id="62985-113">-內容</span><span class="sxs-lookup"><span data-stu-id="62985-113">-Context</span></span>
<span data-ttu-id="62985-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="62985-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="62985-115">若要取得儲存內容，請 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62985-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="62985-116">-Force</span><span class="sxs-lookup"><span data-stu-id="62985-116">-Force</span></span>
<span data-ttu-id="62985-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="62985-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62985-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="62985-118">-Name</span></span>
<span data-ttu-id="62985-119">指定要移除之佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="62985-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62985-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62985-120">-PassThru</span></span>
<span data-ttu-id="62985-121">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="62985-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="62985-122">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="62985-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="62985-123">-確認</span><span class="sxs-lookup"><span data-stu-id="62985-123">-Confirm</span></span>
<span data-ttu-id="62985-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62985-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62985-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62985-125">-WhatIf</span></span>
<span data-ttu-id="62985-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62985-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62985-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62985-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62985-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62985-128">CommonParameters</span></span>
<span data-ttu-id="62985-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62985-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62985-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62985-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62985-131">輸入</span><span class="sxs-lookup"><span data-stu-id="62985-131">INPUTS</span></span>

### <span data-ttu-id="62985-132">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="62985-132">IStorageContext</span></span>

<span data-ttu-id="62985-133">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="62985-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="62985-134">字串</span><span class="sxs-lookup"><span data-stu-id="62985-134">String</span></span>

<span data-ttu-id="62985-135">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="62985-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="62985-136">輸出</span><span class="sxs-lookup"><span data-stu-id="62985-136">OUTPUTS</span></span>

### <span data-ttu-id="62985-137">System.object</span><span class="sxs-lookup"><span data-stu-id="62985-137">System.Boolean</span></span>

## <span data-ttu-id="62985-138">筆記</span><span class="sxs-lookup"><span data-stu-id="62985-138">NOTES</span></span>

## <span data-ttu-id="62985-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="62985-139">RELATED LINKS</span></span>

[<span data-ttu-id="62985-140">AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="62985-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="62985-141">新-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="62985-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
