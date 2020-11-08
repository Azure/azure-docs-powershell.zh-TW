---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958469"
---
# <span data-ttu-id="67f16-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="67f16-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="67f16-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67f16-102">SYNOPSIS</span></span>
<span data-ttu-id="67f16-103">移除儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="67f16-103">Removes a storage table.</span></span>

## <span data-ttu-id="67f16-104">句法</span><span class="sxs-lookup"><span data-stu-id="67f16-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67f16-105">說明</span><span class="sxs-lookup"><span data-stu-id="67f16-105">DESCRIPTION</span></span>
<span data-ttu-id="67f16-106">**AzStorageTable** Cmdlet 會從 Azure 中的儲存空間中移除一或多個儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="67f16-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="67f16-107">示例</span><span class="sxs-lookup"><span data-stu-id="67f16-107">EXAMPLES</span></span>

### <span data-ttu-id="67f16-108">範例1：移除表格</span><span class="sxs-lookup"><span data-stu-id="67f16-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="67f16-109">這個命令會移除表格。</span><span class="sxs-lookup"><span data-stu-id="67f16-109">This command removes a table.</span></span>

### <span data-ttu-id="67f16-110">範例2：移除多個表格</span><span class="sxs-lookup"><span data-stu-id="67f16-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="67f16-111">這個範例將萬用字元與 *Name* 參數搭配使用，以取得符合模式資料表的所有資料表，然後在管線上傳遞結果來移除資料表。</span><span class="sxs-lookup"><span data-stu-id="67f16-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="67f16-112">參數</span><span class="sxs-lookup"><span data-stu-id="67f16-112">PARAMETERS</span></span>

### <span data-ttu-id="67f16-113">-內容</span><span class="sxs-lookup"><span data-stu-id="67f16-113">-Context</span></span>
<span data-ttu-id="67f16-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="67f16-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="67f16-115">您可以使用 New-AzStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="67f16-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="67f16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f16-116">-DefaultProfile</span></span>
<span data-ttu-id="67f16-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67f16-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f16-118">-Force</span><span class="sxs-lookup"><span data-stu-id="67f16-118">-Force</span></span>
<span data-ttu-id="67f16-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="67f16-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67f16-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="67f16-120">-Name</span></span>
<span data-ttu-id="67f16-121">指定要移除的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="67f16-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="67f16-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67f16-122">-PassThru</span></span>
<span data-ttu-id="67f16-123">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="67f16-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="67f16-124">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="67f16-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="67f16-125">-確認</span><span class="sxs-lookup"><span data-stu-id="67f16-125">-Confirm</span></span>
<span data-ttu-id="67f16-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67f16-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67f16-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67f16-127">-WhatIf</span></span>
<span data-ttu-id="67f16-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67f16-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67f16-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67f16-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67f16-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f16-130">CommonParameters</span></span>
<span data-ttu-id="67f16-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67f16-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f16-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67f16-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f16-133">輸入</span><span class="sxs-lookup"><span data-stu-id="67f16-133">INPUTS</span></span>

### <span data-ttu-id="67f16-134">System.object</span><span class="sxs-lookup"><span data-stu-id="67f16-134">System.String</span></span>

### <span data-ttu-id="67f16-135">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="67f16-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="67f16-136">輸出</span><span class="sxs-lookup"><span data-stu-id="67f16-136">OUTPUTS</span></span>

### <span data-ttu-id="67f16-137">System.object</span><span class="sxs-lookup"><span data-stu-id="67f16-137">System.Boolean</span></span>

## <span data-ttu-id="67f16-138">筆記</span><span class="sxs-lookup"><span data-stu-id="67f16-138">NOTES</span></span>

## <span data-ttu-id="67f16-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="67f16-139">RELATED LINKS</span></span>

[<span data-ttu-id="67f16-140">AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="67f16-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)