---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443335"
---
# <span data-ttu-id="ce087-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ce087-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="ce087-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce087-102">SYNOPSIS</span></span>
<span data-ttu-id="ce087-103">移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="ce087-103">Removes a storage queue.</span></span>

## <span data-ttu-id="ce087-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce087-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce087-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce087-105">DESCRIPTION</span></span>
<span data-ttu-id="ce087-106">**AzureStorageQueue** Cmdlet 會移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="ce087-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="ce087-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce087-107">EXAMPLES</span></span>

### <span data-ttu-id="ce087-108">範例1：依名稱移除儲存佇列</span><span class="sxs-lookup"><span data-stu-id="ce087-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="ce087-109">這個命令會移除名為 ContosoQueue01 的佇列。</span><span class="sxs-lookup"><span data-stu-id="ce087-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="ce087-110">範例2：移除多個儲存佇列</span><span class="sxs-lookup"><span data-stu-id="ce087-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="ce087-111">這個命令會移除名稱以 Contoso 為開頭的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="ce087-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="ce087-112">參數</span><span class="sxs-lookup"><span data-stu-id="ce087-112">PARAMETERS</span></span>

### <span data-ttu-id="ce087-113">-內容</span><span class="sxs-lookup"><span data-stu-id="ce087-113">-Context</span></span>
<span data-ttu-id="ce087-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ce087-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ce087-115">若要取得儲存內容，請 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce087-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ce087-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ce087-116">-Force</span></span>
<span data-ttu-id="ce087-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ce087-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce087-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce087-118">-Name</span></span>
<span data-ttu-id="ce087-119">指定要移除之佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce087-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="ce087-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce087-120">-PassThru</span></span>
<span data-ttu-id="ce087-121">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="ce087-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ce087-122">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ce087-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ce087-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ce087-123">-Confirm</span></span>
<span data-ttu-id="ce087-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce087-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce087-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce087-125">-WhatIf</span></span>
<span data-ttu-id="ce087-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce087-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce087-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce087-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce087-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce087-128">CommonParameters</span></span>
<span data-ttu-id="ce087-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce087-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce087-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce087-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce087-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ce087-131">INPUTS</span></span>

## <span data-ttu-id="ce087-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ce087-132">OUTPUTS</span></span>

## <span data-ttu-id="ce087-133">筆記</span><span class="sxs-lookup"><span data-stu-id="ce087-133">NOTES</span></span>

## <span data-ttu-id="ce087-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce087-134">RELATED LINKS</span></span>

[<span data-ttu-id="ce087-135">AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ce087-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="ce087-136">新-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ce087-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
