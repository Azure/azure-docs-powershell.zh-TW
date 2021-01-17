---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435892"
---
# <span data-ttu-id="87bfc-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87bfc-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="87bfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="87bfc-103">從 Azure 儲存空間資料表移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="87bfc-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="87bfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="87bfc-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87bfc-105">說明</span><span class="sxs-lookup"><span data-stu-id="87bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="87bfc-106">**AzStorageTableStoredAccessPolicy** Cmdlet 會從 Azure 儲存空間資料表中移除已儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="87bfc-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="87bfc-107">示例</span><span class="sxs-lookup"><span data-stu-id="87bfc-107">EXAMPLES</span></span>

### <span data-ttu-id="87bfc-108">範例1：從儲存資料表移除儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="87bfc-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="87bfc-109">這個命令會從名為 MyTable 的存儲資料表中移除名為 Policy05 的原則。</span><span class="sxs-lookup"><span data-stu-id="87bfc-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="87bfc-110">參數</span><span class="sxs-lookup"><span data-stu-id="87bfc-110">PARAMETERS</span></span>

### <span data-ttu-id="87bfc-111">-內容</span><span class="sxs-lookup"><span data-stu-id="87bfc-111">-Context</span></span>
<span data-ttu-id="87bfc-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="87bfc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="87bfc-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87bfc-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="87bfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87bfc-114">-DefaultProfile</span></span>
<span data-ttu-id="87bfc-115">與 Azure 的通訊。</span><span class="sxs-lookup"><span data-stu-id="87bfc-115">communication with Azure.</span></span>

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

### <span data-ttu-id="87bfc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87bfc-116">-PassThru</span></span>
<span data-ttu-id="87bfc-117">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="87bfc-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="87bfc-118">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="87bfc-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="87bfc-119">-原則</span><span class="sxs-lookup"><span data-stu-id="87bfc-119">-Policy</span></span>
<span data-ttu-id="87bfc-120">指定此 Cmdlet 移除之已儲存的訪問原則名稱。</span><span class="sxs-lookup"><span data-stu-id="87bfc-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="87bfc-121">-資料表</span><span class="sxs-lookup"><span data-stu-id="87bfc-121">-Table</span></span>
<span data-ttu-id="87bfc-122">指定 Azure 資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="87bfc-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="87bfc-123">-確認</span><span class="sxs-lookup"><span data-stu-id="87bfc-123">-Confirm</span></span>
<span data-ttu-id="87bfc-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87bfc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87bfc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87bfc-125">-WhatIf</span></span>
<span data-ttu-id="87bfc-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87bfc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87bfc-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87bfc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87bfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87bfc-128">CommonParameters</span></span>
<span data-ttu-id="87bfc-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87bfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87bfc-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87bfc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87bfc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="87bfc-131">INPUTS</span></span>

### <span data-ttu-id="87bfc-132">System.object</span><span class="sxs-lookup"><span data-stu-id="87bfc-132">System.String</span></span>

### <span data-ttu-id="87bfc-133">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="87bfc-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="87bfc-134">輸出</span><span class="sxs-lookup"><span data-stu-id="87bfc-134">OUTPUTS</span></span>

### <span data-ttu-id="87bfc-135">System.object</span><span class="sxs-lookup"><span data-stu-id="87bfc-135">System.Boolean</span></span>

## <span data-ttu-id="87bfc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="87bfc-136">NOTES</span></span>

## <span data-ttu-id="87bfc-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="87bfc-137">RELATED LINKS</span></span>

[<span data-ttu-id="87bfc-138">AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87bfc-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="87bfc-139">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="87bfc-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="87bfc-140">新-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87bfc-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="87bfc-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="87bfc-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
