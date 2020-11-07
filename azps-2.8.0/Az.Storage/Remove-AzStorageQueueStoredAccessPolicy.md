---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32bf76e80dbd088b133d4401dc51bb1f49b2593b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792896"
---
# <span data-ttu-id="c081e-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c081e-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c081e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c081e-102">SYNOPSIS</span></span>
<span data-ttu-id="c081e-103">從 Azure 儲存空間佇列移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="c081e-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="c081e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c081e-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c081e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c081e-105">DESCRIPTION</span></span>
<span data-ttu-id="c081e-106">**AzStorageQueueStoredAccessPolicy** Cmdlet 會從 Azure 儲存空間佇列中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="c081e-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="c081e-107">示例</span><span class="sxs-lookup"><span data-stu-id="c081e-107">EXAMPLES</span></span>

### <span data-ttu-id="c081e-108">範例1：從儲存佇列移除已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="c081e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="c081e-109">這個命令會從名為 MyQueue 的儲存空間中移除名為 Policy04 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="c081e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="c081e-110">參數</span><span class="sxs-lookup"><span data-stu-id="c081e-110">PARAMETERS</span></span>

### <span data-ttu-id="c081e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c081e-111">-Context</span></span>
<span data-ttu-id="c081e-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="c081e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c081e-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c081e-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c081e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c081e-114">-DefaultProfile</span></span>
<span data-ttu-id="c081e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c081e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c081e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c081e-116">-PassThru</span></span>
<span data-ttu-id="c081e-117">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="c081e-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c081e-118">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c081e-118">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c081e-119">-原則</span><span class="sxs-lookup"><span data-stu-id="c081e-119">-Policy</span></span>
<span data-ttu-id="c081e-120">指定此 Cmdlet 移除之已儲存的訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="c081e-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c081e-121">-佇列</span><span class="sxs-lookup"><span data-stu-id="c081e-121">-Queue</span></span>
<span data-ttu-id="c081e-122">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="c081e-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c081e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c081e-123">-Confirm</span></span>
<span data-ttu-id="c081e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c081e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c081e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c081e-125">-WhatIf</span></span>
<span data-ttu-id="c081e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c081e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c081e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c081e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c081e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c081e-128">CommonParameters</span></span>
<span data-ttu-id="c081e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c081e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c081e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c081e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c081e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c081e-131">INPUTS</span></span>

### <span data-ttu-id="c081e-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c081e-132">System.String</span></span>

### <span data-ttu-id="c081e-133">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="c081e-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c081e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c081e-134">OUTPUTS</span></span>

### <span data-ttu-id="c081e-135">System.object</span><span class="sxs-lookup"><span data-stu-id="c081e-135">System.Boolean</span></span>

## <span data-ttu-id="c081e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c081e-136">NOTES</span></span>

## <span data-ttu-id="c081e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c081e-137">RELATED LINKS</span></span>

[<span data-ttu-id="c081e-138">AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c081e-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c081e-139">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c081e-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c081e-140">新-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c081e-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c081e-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c081e-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
