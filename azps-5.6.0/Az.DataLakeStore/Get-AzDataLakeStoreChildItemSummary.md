---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: d83e07e207c2b0e3a03c745abc874814378e5ee4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903245"
---
# <span data-ttu-id="45386-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="45386-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="45386-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45386-102">SYNOPSIS</span></span>
<span data-ttu-id="45386-103">獲得指定路徑中包含的總大小、檔案和目錄摘要</span><span class="sxs-lookup"><span data-stu-id="45386-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="45386-104">語法</span><span class="sxs-lookup"><span data-stu-id="45386-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45386-105">描述</span><span class="sxs-lookup"><span data-stu-id="45386-105">DESCRIPTION</span></span>
<span data-ttu-id="45386-106">**Get-AzDataLakeStoreChildItemSummary** 會針對給定路徑來取得內容摘要。</span><span class="sxs-lookup"><span data-stu-id="45386-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="45386-107">它會以遞迴方式計算所指定的路徑下所有檔案的檔案總數、目錄和總大小。</span><span class="sxs-lookup"><span data-stu-id="45386-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="45386-108">例子</span><span class="sxs-lookup"><span data-stu-id="45386-108">EXAMPLES</span></span>

### <span data-ttu-id="45386-109">範例 1：取得資料夾的內容摘要</span><span class="sxs-lookup"><span data-stu-id="45386-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="45386-110">它會列出 /a 下包含的總目錄、檔案數量及其大小。</span><span class="sxs-lookup"><span data-stu-id="45386-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="45386-111">參數</span><span class="sxs-lookup"><span data-stu-id="45386-111">PARAMETERS</span></span>

### <span data-ttu-id="45386-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="45386-112">-Account</span></span>
<span data-ttu-id="45386-113">Data Lake Store 帳戶以在</span><span class="sxs-lookup"><span data-stu-id="45386-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="45386-114">-並行</span><span class="sxs-lookup"><span data-stu-id="45386-114">-Concurrency</span></span>
<span data-ttu-id="45386-115">表示平行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="45386-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="45386-116">根據系統規格，預設會以最佳效果計算。</span><span class="sxs-lookup"><span data-stu-id="45386-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45386-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45386-117">-DefaultProfile</span></span>
<span data-ttu-id="45386-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45386-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45386-119">-路徑</span><span class="sxs-lookup"><span data-stu-id="45386-119">-Path</span></span>
<span data-ttu-id="45386-120">指定 Data Lake 帳戶中應該要取取的路徑。</span><span class="sxs-lookup"><span data-stu-id="45386-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="45386-121">可以是檔案或資料夾，格式為 '/folder/file.txt'，其中 DNS 後的第一個 '/' 代表檔案系統的根目錄。</span><span class="sxs-lookup"><span data-stu-id="45386-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45386-122">-確認</span><span class="sxs-lookup"><span data-stu-id="45386-122">-Confirm</span></span>
<span data-ttu-id="45386-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="45386-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45386-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45386-124">-WhatIf</span></span>
<span data-ttu-id="45386-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45386-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45386-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45386-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45386-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45386-127">CommonParameters</span></span>
<span data-ttu-id="45386-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45386-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45386-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="45386-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45386-130">輸入</span><span class="sxs-lookup"><span data-stu-id="45386-130">INPUTS</span></span>

### <span data-ttu-id="45386-131">System.String</span><span class="sxs-lookup"><span data-stu-id="45386-131">System.String</span></span>

### <span data-ttu-id="45386-132">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="45386-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="45386-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="45386-133">System.Int32</span></span>

## <span data-ttu-id="45386-134">輸出</span><span class="sxs-lookup"><span data-stu-id="45386-134">OUTPUTS</span></span>

### <span data-ttu-id="45386-135">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="45386-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="45386-136">筆記</span><span class="sxs-lookup"><span data-stu-id="45386-136">NOTES</span></span>

## <span data-ttu-id="45386-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="45386-137">RELATED LINKS</span></span>
