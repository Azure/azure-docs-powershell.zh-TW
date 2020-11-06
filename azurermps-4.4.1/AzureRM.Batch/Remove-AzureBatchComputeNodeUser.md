---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453596"
---
# <span data-ttu-id="e814f-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e814f-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="e814f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e814f-102">SYNOPSIS</span></span>
<span data-ttu-id="e814f-103">從批次計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="e814f-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e814f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e814f-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e814f-105">說明</span><span class="sxs-lookup"><span data-stu-id="e814f-105">DESCRIPTION</span></span>
<span data-ttu-id="e814f-106">**AzureBatchComputeNodeUser** Cmdlet 會從 Azure Batch 計算節點刪除使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="e814f-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="e814f-107">示例</span><span class="sxs-lookup"><span data-stu-id="e814f-107">EXAMPLES</span></span>

### <span data-ttu-id="e814f-108">範例1：不需確認就能從計算節點刪除使用者</span><span class="sxs-lookup"><span data-stu-id="e814f-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="e814f-109">這個命令會從名為 ComputeNode01 的計算節點中刪除名為 User14 的使用者。</span><span class="sxs-lookup"><span data-stu-id="e814f-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="e814f-110">Compute 節點位於名為 Pool01 的 pool 中。</span><span class="sxs-lookup"><span data-stu-id="e814f-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="e814f-111">這個命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e814f-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e814f-112">因此，命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e814f-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e814f-113">參數</span><span class="sxs-lookup"><span data-stu-id="e814f-113">PARAMETERS</span></span>

### <span data-ttu-id="e814f-114">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="e814f-114">-BatchContext</span></span>
<span data-ttu-id="e814f-115">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="e814f-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e814f-116">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e814f-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e814f-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e814f-117">-ComputeNodeId</span></span>
<span data-ttu-id="e814f-118">指定此 Cmdlet 刪除使用者帳戶的計算節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="e814f-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e814f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e814f-119">-Name</span></span>
<span data-ttu-id="e814f-120">指定要刪除的使用者帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e814f-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="e814f-121">您無法指定通配字元。</span><span class="sxs-lookup"><span data-stu-id="e814f-121">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e814f-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e814f-122">-PoolId</span></span>
<span data-ttu-id="e814f-123">指定包含要刪除其使用者帳戶之計算節點的池 ID。</span><span class="sxs-lookup"><span data-stu-id="e814f-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e814f-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e814f-124">-Confirm</span></span>
<span data-ttu-id="e814f-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e814f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e814f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e814f-126">-WhatIf</span></span>
<span data-ttu-id="e814f-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e814f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e814f-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e814f-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e814f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e814f-129">-DefaultProfile</span></span>
<span data-ttu-id="e814f-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e814f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e814f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e814f-131">CommonParameters</span></span>
<span data-ttu-id="e814f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e814f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e814f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e814f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e814f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e814f-134">INPUTS</span></span>

### <span data-ttu-id="e814f-135">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="e814f-135">BatchAccountContext</span></span>
<span data-ttu-id="e814f-136">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e814f-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="e814f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e814f-137">OUTPUTS</span></span>

## <span data-ttu-id="e814f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e814f-138">NOTES</span></span>

## <span data-ttu-id="e814f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e814f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e814f-140">新-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e814f-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="e814f-141">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e814f-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e814f-142">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e814f-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


