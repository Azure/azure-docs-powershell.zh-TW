---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ce4a8051867b535ba2aff4429b5bcfa0b9ab53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916754"
---
# <span data-ttu-id="c1211-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c1211-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1211-102">SYNOPSIS</span></span>
<span data-ttu-id="c1211-103">刪除 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="c1211-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c1211-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1211-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1211-105">描述</span><span class="sxs-lookup"><span data-stu-id="c1211-105">DESCRIPTION</span></span>
<span data-ttu-id="c1211-106">**Remove-AzDataLakeStoreItem** Cmdlet 會刪除 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="c1211-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c1211-107">例子</span><span class="sxs-lookup"><span data-stu-id="c1211-107">EXAMPLES</span></span>

### <span data-ttu-id="c1211-108">範例 1：移除多個專案</span><span class="sxs-lookup"><span data-stu-id="c1211-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="c1211-109">此命令會從 Data Lake Store File01.txtFile.csv和檔案。</span><span class="sxs-lookup"><span data-stu-id="c1211-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="c1211-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1211-110">PARAMETERS</span></span>

### <span data-ttu-id="c1211-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c1211-111">-Account</span></span>
<span data-ttu-id="c1211-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1211-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1211-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1211-113">-DefaultProfile</span></span>
<span data-ttu-id="c1211-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1211-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1211-115">-強制</span><span class="sxs-lookup"><span data-stu-id="c1211-115">-Force</span></span>
<span data-ttu-id="c1211-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c1211-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1211-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1211-117">-PassThru</span></span>
<span data-ttu-id="c1211-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="c1211-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1211-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c1211-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1211-120">-路徑</span><span class="sxs-lookup"><span data-stu-id="c1211-120">-Paths</span></span>
<span data-ttu-id="c1211-121">指定要移除之檔案的 Data Lake Store 路徑陣列，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="c1211-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1211-122">-遞迴</span><span class="sxs-lookup"><span data-stu-id="c1211-122">-Recurse</span></span>
<span data-ttu-id="c1211-123">表示此作業會刪除目的檔案夾中的所有專案，包括子資料夾。</span><span class="sxs-lookup"><span data-stu-id="c1211-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1211-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c1211-124">-Confirm</span></span>
<span data-ttu-id="c1211-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1211-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1211-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1211-126">-WhatIf</span></span>
<span data-ttu-id="c1211-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1211-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1211-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1211-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1211-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1211-129">CommonParameters</span></span>
<span data-ttu-id="c1211-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1211-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1211-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c1211-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1211-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c1211-132">INPUTS</span></span>

### <span data-ttu-id="c1211-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c1211-133">System.String</span></span>

### <span data-ttu-id="c1211-134">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="c1211-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="c1211-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1211-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1211-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c1211-136">OUTPUTS</span></span>

### <span data-ttu-id="c1211-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1211-137">System.Boolean</span></span>

## <span data-ttu-id="c1211-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c1211-138">NOTES</span></span>

## <span data-ttu-id="c1211-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1211-139">RELATED LINKS</span></span>

[<span data-ttu-id="c1211-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="c1211-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c1211-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="c1211-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="c1211-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="c1211-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c1211-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


