---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443328"
---
# <span data-ttu-id="d9ced-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9ced-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d9ced-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9ced-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ced-103">從 Azure 儲存空間佇列移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="d9ced-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="d9ced-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9ced-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ced-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9ced-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ced-106">**AzureStorageQueueStoredAccessPolicy** Cmdlet 會從 Azure 儲存空間佇列中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="d9ced-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="d9ced-107">示例</span><span class="sxs-lookup"><span data-stu-id="d9ced-107">EXAMPLES</span></span>

### <span data-ttu-id="d9ced-108">範例1：從儲存佇列移除已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="d9ced-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="d9ced-109">這個命令會從名為 MyQueue 的儲存空間中移除名為 Policy04 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="d9ced-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="d9ced-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9ced-110">PARAMETERS</span></span>

### <span data-ttu-id="d9ced-111">-內容</span><span class="sxs-lookup"><span data-stu-id="d9ced-111">-Context</span></span>
<span data-ttu-id="d9ced-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="d9ced-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d9ced-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9ced-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d9ced-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9ced-114">-PassThru</span></span>
<span data-ttu-id="d9ced-115">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="d9ced-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d9ced-116">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d9ced-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d9ced-117">-原則</span><span class="sxs-lookup"><span data-stu-id="d9ced-117">-Policy</span></span>
<span data-ttu-id="d9ced-118">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="d9ced-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="d9ced-119">-佇列</span><span class="sxs-lookup"><span data-stu-id="d9ced-119">-Queue</span></span>
<span data-ttu-id="d9ced-120">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="d9ced-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d9ced-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d9ced-121">-Confirm</span></span>
<span data-ttu-id="d9ced-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9ced-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ced-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ced-123">-WhatIf</span></span>
<span data-ttu-id="d9ced-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9ced-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ced-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9ced-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ced-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ced-126">CommonParameters</span></span>
<span data-ttu-id="d9ced-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9ced-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ced-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d9ced-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ced-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d9ced-129">INPUTS</span></span>

## <span data-ttu-id="d9ced-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d9ced-130">OUTPUTS</span></span>

## <span data-ttu-id="d9ced-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d9ced-131">NOTES</span></span>

## <span data-ttu-id="d9ced-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9ced-132">RELATED LINKS</span></span>

[<span data-ttu-id="d9ced-133">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9ced-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d9ced-134">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="d9ced-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d9ced-135">新-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9ced-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d9ced-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d9ced-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
