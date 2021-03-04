---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 0f09c391f63d4d8e1eb0949acb54770e242744a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904230"
---
# <span data-ttu-id="2d6ce-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2d6ce-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="2d6ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d6ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6ce-103">移除儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-103">Removes a storage table.</span></span>

## <span data-ttu-id="2d6ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="2d6ce-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d6ce-105">描述</span><span class="sxs-lookup"><span data-stu-id="2d6ce-105">DESCRIPTION</span></span>
<span data-ttu-id="2d6ce-106">**Remove-AzStorageTable** Cmdlet 會從 Azure 中的儲存空間帳戶移除一或多個儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="2d6ce-107">例子</span><span class="sxs-lookup"><span data-stu-id="2d6ce-107">EXAMPLES</span></span>

### <span data-ttu-id="2d6ce-108">範例 1：移除表格</span><span class="sxs-lookup"><span data-stu-id="2d6ce-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="2d6ce-109">此命令會移除表格。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-109">This command removes a table.</span></span>

### <span data-ttu-id="2d6ce-110">範例 2：移除多個資料表</span><span class="sxs-lookup"><span data-stu-id="2d6ce-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="2d6ce-111">此範例使用包含 *Name* 參數的萬用字元，以取得符合模式資料表的所有資料表，然後傳遞管線上的結果以移除資料表。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="2d6ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="2d6ce-112">PARAMETERS</span></span>

### <span data-ttu-id="2d6ce-113">-內容</span><span class="sxs-lookup"><span data-stu-id="2d6ce-113">-Context</span></span>
<span data-ttu-id="2d6ce-114">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2d6ce-115">您可以使用 Cmdlet New-AzStorageContext建立。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2d6ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6ce-116">-DefaultProfile</span></span>
<span data-ttu-id="2d6ce-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d6ce-118">-強制</span><span class="sxs-lookup"><span data-stu-id="2d6ce-118">-Force</span></span>
<span data-ttu-id="2d6ce-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d6ce-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d6ce-120">-Name</span></span>
<span data-ttu-id="2d6ce-121">指定要移除的表格名稱。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d6ce-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d6ce-122">-PassThru</span></span>
<span data-ttu-id="2d6ce-123">表示此 Cmdlet 會返回 **反映** 作業成功的布林值。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2d6ce-124">根據預設，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2d6ce-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2d6ce-125">-Confirm</span></span>
<span data-ttu-id="2d6ce-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d6ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d6ce-127">-WhatIf</span></span>
<span data-ttu-id="2d6ce-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d6ce-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d6ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6ce-130">CommonParameters</span></span>
<span data-ttu-id="2d6ce-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6ce-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2d6ce-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6ce-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2d6ce-133">INPUTS</span></span>

### <span data-ttu-id="2d6ce-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2d6ce-134">System.String</span></span>

### <span data-ttu-id="2d6ce-135">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2d6ce-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d6ce-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2d6ce-136">OUTPUTS</span></span>

### <span data-ttu-id="2d6ce-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d6ce-137">System.Boolean</span></span>

## <span data-ttu-id="2d6ce-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2d6ce-138">NOTES</span></span>

## <span data-ttu-id="2d6ce-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d6ce-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d6ce-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="2d6ce-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
