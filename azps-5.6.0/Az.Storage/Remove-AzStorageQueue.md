---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: d66203d712de76004d009b98fdc14a18cc69e461
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904245"
---
# <span data-ttu-id="a960a-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a960a-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="a960a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a960a-102">SYNOPSIS</span></span>
<span data-ttu-id="a960a-103">移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="a960a-103">Removes a storage queue.</span></span>

## <span data-ttu-id="a960a-104">語法</span><span class="sxs-lookup"><span data-stu-id="a960a-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a960a-105">描述</span><span class="sxs-lookup"><span data-stu-id="a960a-105">DESCRIPTION</span></span>
<span data-ttu-id="a960a-106">**Remove-AzStorageQueue** Cmdlet 會移除儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="a960a-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="a960a-107">例子</span><span class="sxs-lookup"><span data-stu-id="a960a-107">EXAMPLES</span></span>

### <span data-ttu-id="a960a-108">範例 1：根據名稱移除儲存佇列</span><span class="sxs-lookup"><span data-stu-id="a960a-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="a960a-109">此命令會移除名為 ContosoQueue01 的佇列。</span><span class="sxs-lookup"><span data-stu-id="a960a-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="a960a-110">範例 2：移除多個儲存佇列</span><span class="sxs-lookup"><span data-stu-id="a960a-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="a960a-111">此命令會移除名稱以 Contoso 為開始的所有佇列。</span><span class="sxs-lookup"><span data-stu-id="a960a-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="a960a-112">參數</span><span class="sxs-lookup"><span data-stu-id="a960a-112">PARAMETERS</span></span>

### <span data-ttu-id="a960a-113">-內容</span><span class="sxs-lookup"><span data-stu-id="a960a-113">-Context</span></span>
<span data-ttu-id="a960a-114">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="a960a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a960a-115">若要取得儲存內容，New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a960a-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a960a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a960a-116">-DefaultProfile</span></span>
<span data-ttu-id="a960a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a960a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a960a-118">-強制</span><span class="sxs-lookup"><span data-stu-id="a960a-118">-Force</span></span>
<span data-ttu-id="a960a-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a960a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a960a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a960a-120">-Name</span></span>
<span data-ttu-id="a960a-121">指定要移除的佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="a960a-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="a960a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a960a-122">-PassThru</span></span>
<span data-ttu-id="a960a-123">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="a960a-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a960a-124">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a960a-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a960a-125">-確認</span><span class="sxs-lookup"><span data-stu-id="a960a-125">-Confirm</span></span>
<span data-ttu-id="a960a-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a960a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a960a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a960a-127">-WhatIf</span></span>
<span data-ttu-id="a960a-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a960a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a960a-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a960a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a960a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a960a-130">CommonParameters</span></span>
<span data-ttu-id="a960a-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a960a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a960a-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a960a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a960a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a960a-133">INPUTS</span></span>

### <span data-ttu-id="a960a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a960a-134">System.String</span></span>

### <span data-ttu-id="a960a-135">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a960a-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a960a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="a960a-136">OUTPUTS</span></span>

### <span data-ttu-id="a960a-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a960a-137">System.Boolean</span></span>

## <span data-ttu-id="a960a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a960a-138">NOTES</span></span>

## <span data-ttu-id="a960a-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="a960a-139">RELATED LINKS</span></span>

[<span data-ttu-id="a960a-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a960a-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="a960a-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a960a-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
