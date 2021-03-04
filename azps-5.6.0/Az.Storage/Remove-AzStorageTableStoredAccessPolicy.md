---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 7674b21e72d375665662272cb2ac1a585d266324
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904226"
---
# <span data-ttu-id="ac14a-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac14a-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="ac14a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ac14a-102">SYNOPSIS</span></span>
<span data-ttu-id="ac14a-103">從 Azure 儲存資料表移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="ac14a-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="ac14a-104">語法</span><span class="sxs-lookup"><span data-stu-id="ac14a-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac14a-105">描述</span><span class="sxs-lookup"><span data-stu-id="ac14a-105">DESCRIPTION</span></span>
<span data-ttu-id="ac14a-106">**Remove-AzStorageTableStoredAccessPolicy** Cmdlet 會從 Azure 儲存資料表移除儲存的存取策略。</span><span class="sxs-lookup"><span data-stu-id="ac14a-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="ac14a-107">例子</span><span class="sxs-lookup"><span data-stu-id="ac14a-107">EXAMPLES</span></span>

### <span data-ttu-id="ac14a-108">範例 1：從儲存資料表移除儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="ac14a-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="ac14a-109">此命令會從名為 MyTable 的儲存資料表移除名為 Policy05 的策略。</span><span class="sxs-lookup"><span data-stu-id="ac14a-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="ac14a-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac14a-110">PARAMETERS</span></span>

### <span data-ttu-id="ac14a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ac14a-111">-Context</span></span>
<span data-ttu-id="ac14a-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="ac14a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ac14a-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac14a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ac14a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac14a-114">-DefaultProfile</span></span>
<span data-ttu-id="ac14a-115">與 Azure 的通訊。</span><span class="sxs-lookup"><span data-stu-id="ac14a-115">communication with Azure.</span></span>

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

### <span data-ttu-id="ac14a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac14a-116">-PassThru</span></span>
<span data-ttu-id="ac14a-117">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="ac14a-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ac14a-118">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ac14a-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ac14a-119">-策略</span><span class="sxs-lookup"><span data-stu-id="ac14a-119">-Policy</span></span>
<span data-ttu-id="ac14a-120">指定此 Cmdlet 移除的已儲存存取策略名稱。</span><span class="sxs-lookup"><span data-stu-id="ac14a-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ac14a-121">-表格</span><span class="sxs-lookup"><span data-stu-id="ac14a-121">-Table</span></span>
<span data-ttu-id="ac14a-122">指定 Azure 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ac14a-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="ac14a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ac14a-123">-Confirm</span></span>
<span data-ttu-id="ac14a-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ac14a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac14a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac14a-125">-WhatIf</span></span>
<span data-ttu-id="ac14a-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac14a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac14a-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac14a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac14a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac14a-128">CommonParameters</span></span>
<span data-ttu-id="ac14a-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ac14a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac14a-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ac14a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac14a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ac14a-131">INPUTS</span></span>

### <span data-ttu-id="ac14a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ac14a-132">System.String</span></span>

### <span data-ttu-id="ac14a-133">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac14a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac14a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ac14a-134">OUTPUTS</span></span>

### <span data-ttu-id="ac14a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac14a-135">System.Boolean</span></span>

## <span data-ttu-id="ac14a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ac14a-136">NOTES</span></span>

## <span data-ttu-id="ac14a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac14a-137">RELATED LINKS</span></span>

[<span data-ttu-id="ac14a-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac14a-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ac14a-139">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ac14a-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ac14a-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac14a-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="ac14a-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac14a-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
