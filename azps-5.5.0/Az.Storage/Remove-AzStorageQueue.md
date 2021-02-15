---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138222"
---
# <span data-ttu-id="75256-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="75256-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="75256-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75256-102">SYNOPSIS</span></span>
<span data-ttu-id="75256-103">移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="75256-103">Removes a storage queue.</span></span>

## <span data-ttu-id="75256-104">句法</span><span class="sxs-lookup"><span data-stu-id="75256-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75256-105">說明</span><span class="sxs-lookup"><span data-stu-id="75256-105">DESCRIPTION</span></span>
<span data-ttu-id="75256-106">**AzStorageQueue** Cmdlet 會移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="75256-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="75256-107">示例</span><span class="sxs-lookup"><span data-stu-id="75256-107">EXAMPLES</span></span>

### <span data-ttu-id="75256-108">範例1：依名稱移除儲存佇列</span><span class="sxs-lookup"><span data-stu-id="75256-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="75256-109">這個命令會移除名為 ContosoQueue01 的佇列。</span><span class="sxs-lookup"><span data-stu-id="75256-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="75256-110">範例2：移除多個儲存佇列</span><span class="sxs-lookup"><span data-stu-id="75256-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="75256-111">這個命令會移除名稱以 Contoso 為開頭的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="75256-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="75256-112">參數</span><span class="sxs-lookup"><span data-stu-id="75256-112">PARAMETERS</span></span>

### <span data-ttu-id="75256-113">-內容</span><span class="sxs-lookup"><span data-stu-id="75256-113">-Context</span></span>
<span data-ttu-id="75256-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="75256-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="75256-115">若要取得儲存內容，請 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75256-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="75256-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75256-116">-DefaultProfile</span></span>
<span data-ttu-id="75256-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75256-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75256-118">-Force</span><span class="sxs-lookup"><span data-stu-id="75256-118">-Force</span></span>
<span data-ttu-id="75256-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="75256-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75256-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="75256-120">-Name</span></span>
<span data-ttu-id="75256-121">指定要移除之佇列的名稱。</span><span class="sxs-lookup"><span data-stu-id="75256-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75256-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75256-122">-PassThru</span></span>
<span data-ttu-id="75256-123">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="75256-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="75256-124">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="75256-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="75256-125">-確認</span><span class="sxs-lookup"><span data-stu-id="75256-125">-Confirm</span></span>
<span data-ttu-id="75256-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="75256-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75256-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75256-127">-WhatIf</span></span>
<span data-ttu-id="75256-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="75256-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75256-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="75256-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75256-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75256-130">CommonParameters</span></span>
<span data-ttu-id="75256-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75256-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75256-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75256-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75256-133">輸入</span><span class="sxs-lookup"><span data-stu-id="75256-133">INPUTS</span></span>

### <span data-ttu-id="75256-134">System.object</span><span class="sxs-lookup"><span data-stu-id="75256-134">System.String</span></span>

### <span data-ttu-id="75256-135">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="75256-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="75256-136">輸出</span><span class="sxs-lookup"><span data-stu-id="75256-136">OUTPUTS</span></span>

### <span data-ttu-id="75256-137">System.object</span><span class="sxs-lookup"><span data-stu-id="75256-137">System.Boolean</span></span>

## <span data-ttu-id="75256-138">筆記</span><span class="sxs-lookup"><span data-stu-id="75256-138">NOTES</span></span>

## <span data-ttu-id="75256-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="75256-139">RELATED LINKS</span></span>

[<span data-ttu-id="75256-140">AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="75256-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="75256-141">新-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="75256-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
