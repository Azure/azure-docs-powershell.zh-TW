---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: e33e32051c15483956d0764f5e9ddca25a083f23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802141"
---
# <span data-ttu-id="6bbb1-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6bbb1-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="6bbb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bbb1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bbb1-103">移除儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bbb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bbb1-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bbb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="6bbb1-105">DESCRIPTION</span></span>
<span data-ttu-id="6bbb1-106">**AzureStorageTable** Cmdlet 會從 Azure 中的儲存空間中移除一或多個儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="6bbb1-107">示例</span><span class="sxs-lookup"><span data-stu-id="6bbb1-107">EXAMPLES</span></span>

### <span data-ttu-id="6bbb1-108">範例1：移除表格</span><span class="sxs-lookup"><span data-stu-id="6bbb1-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="6bbb1-109">這個命令會移除表格。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-109">This command removes a table.</span></span>

### <span data-ttu-id="6bbb1-110">範例2：移除多個表格</span><span class="sxs-lookup"><span data-stu-id="6bbb1-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="6bbb1-111">這個範例將萬用字元與 *Name* 參數搭配使用，以取得符合模式資料表的所有資料表，然後在管線上傳遞結果來移除資料表。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="6bbb1-112">參數</span><span class="sxs-lookup"><span data-stu-id="6bbb1-112">PARAMETERS</span></span>

### <span data-ttu-id="6bbb1-113">-內容</span><span class="sxs-lookup"><span data-stu-id="6bbb1-113">-Context</span></span>
<span data-ttu-id="6bbb1-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6bbb1-115">您可以使用 New-AzureStorageContext Cmdlet 來建立它。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6bbb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bbb1-116">-DefaultProfile</span></span>
<span data-ttu-id="6bbb1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bbb1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6bbb1-118">-Force</span></span>
<span data-ttu-id="6bbb1-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6bbb1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bbb1-120">-Name</span></span>
<span data-ttu-id="6bbb1-121">指定要移除的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="6bbb1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bbb1-122">-PassThru</span></span>
<span data-ttu-id="6bbb1-123">表示此 Cmdlet 會傳回反映操作成功的 **布林值** 。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6bbb1-124">根據預設，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6bbb1-125">-確認</span><span class="sxs-lookup"><span data-stu-id="6bbb1-125">-Confirm</span></span>
<span data-ttu-id="6bbb1-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bbb1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bbb1-127">-WhatIf</span></span>
<span data-ttu-id="6bbb1-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bbb1-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bbb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bbb1-130">CommonParameters</span></span>
<span data-ttu-id="6bbb1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bbb1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6bbb1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bbb1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6bbb1-133">INPUTS</span></span>

### <span data-ttu-id="6bbb1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="6bbb1-134">System.String</span></span>

### <span data-ttu-id="6bbb1-135">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="6bbb1-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6bbb1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6bbb1-136">OUTPUTS</span></span>

### <span data-ttu-id="6bbb1-137">System.object</span><span class="sxs-lookup"><span data-stu-id="6bbb1-137">System.Boolean</span></span>

## <span data-ttu-id="6bbb1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6bbb1-138">NOTES</span></span>

## <span data-ttu-id="6bbb1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bbb1-139">RELATED LINKS</span></span>

[<span data-ttu-id="6bbb1-140">AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6bbb1-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
