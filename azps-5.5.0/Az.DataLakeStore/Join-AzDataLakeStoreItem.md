---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133310"
---
# <span data-ttu-id="332f8-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="332f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="332f8-102">SYNOPSIS</span></span>
<span data-ttu-id="332f8-103">加入一或多個檔案，在 Data Lake Store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="332f8-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="332f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="332f8-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="332f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="332f8-105">DESCRIPTION</span></span>
<span data-ttu-id="332f8-106">**AzDataLakeStoreItem** Cmdlet 加入一或多個檔案，以便在 Data Lake store 中建立一個檔案。</span><span class="sxs-lookup"><span data-stu-id="332f8-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="332f8-107">示例</span><span class="sxs-lookup"><span data-stu-id="332f8-107">EXAMPLES</span></span>

### <span data-ttu-id="332f8-108">範例1：加入兩個專案</span><span class="sxs-lookup"><span data-stu-id="332f8-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="332f8-109">這個命令會加入 File01.txt 並 File02.txt，以建立 CombinedFile.txt 的檔案。</span><span class="sxs-lookup"><span data-stu-id="332f8-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="332f8-110">參數</span><span class="sxs-lookup"><span data-stu-id="332f8-110">PARAMETERS</span></span>

### <span data-ttu-id="332f8-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="332f8-111">-Account</span></span>
<span data-ttu-id="332f8-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="332f8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="332f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332f8-113">-DefaultProfile</span></span>
<span data-ttu-id="332f8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="332f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="332f8-115">-目的地</span><span class="sxs-lookup"><span data-stu-id="332f8-115">-Destination</span></span>
<span data-ttu-id="332f8-116">指定已加入專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="332f8-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="332f8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="332f8-117">-Force</span></span>
<span data-ttu-id="332f8-118">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="332f8-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="332f8-119">-路徑</span><span class="sxs-lookup"><span data-stu-id="332f8-119">-Paths</span></span>
<span data-ttu-id="332f8-120">指定要合併之檔案的資料 Lake Store 路徑陣列，並從根目錄 (/) 。</span><span class="sxs-lookup"><span data-stu-id="332f8-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="332f8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="332f8-121">-Confirm</span></span>
<span data-ttu-id="332f8-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="332f8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="332f8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="332f8-123">-WhatIf</span></span>
<span data-ttu-id="332f8-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="332f8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="332f8-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="332f8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="332f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332f8-126">CommonParameters</span></span>
<span data-ttu-id="332f8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="332f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332f8-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="332f8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332f8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="332f8-129">INPUTS</span></span>

### <span data-ttu-id="332f8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="332f8-130">System.String</span></span>

### <span data-ttu-id="332f8-131">DataLakeStorePathInstance [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="332f8-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="332f8-132">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="332f8-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="332f8-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="332f8-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="332f8-134">輸出</span><span class="sxs-lookup"><span data-stu-id="332f8-134">OUTPUTS</span></span>

### <span data-ttu-id="332f8-135">System.object</span><span class="sxs-lookup"><span data-stu-id="332f8-135">System.String</span></span>

## <span data-ttu-id="332f8-136">筆記</span><span class="sxs-lookup"><span data-stu-id="332f8-136">NOTES</span></span>

## <span data-ttu-id="332f8-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="332f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="332f8-138">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="332f8-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="332f8-140">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="332f8-141">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="332f8-142">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="332f8-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="332f8-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


