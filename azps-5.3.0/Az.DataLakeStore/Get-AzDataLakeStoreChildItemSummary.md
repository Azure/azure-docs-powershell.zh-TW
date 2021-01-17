---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: b86b3f070a28de45039ebeb5ed0090f69756639f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434836"
---
# <span data-ttu-id="38867-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="38867-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="38867-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38867-102">SYNOPSIS</span></span>
<span data-ttu-id="38867-103">取得指定路徑中所含之總大小、檔案和目錄的摘要</span><span class="sxs-lookup"><span data-stu-id="38867-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="38867-104">句法</span><span class="sxs-lookup"><span data-stu-id="38867-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38867-105">說明</span><span class="sxs-lookup"><span data-stu-id="38867-105">DESCRIPTION</span></span>
<span data-ttu-id="38867-106">[ **取得 AzDataLakeStoreChildItemSummary** ] 會檢索指定路徑的內容摘要。</span><span class="sxs-lookup"><span data-stu-id="38867-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="38867-107">它會以遞迴方式計算指定路徑下所有檔案的總檔案數、目錄及總大小。</span><span class="sxs-lookup"><span data-stu-id="38867-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="38867-108">示例</span><span class="sxs-lookup"><span data-stu-id="38867-108">EXAMPLES</span></span>

### <span data-ttu-id="38867-109">範例1：取得資料夾的內容摘要</span><span class="sxs-lookup"><span data-stu-id="38867-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="38867-110">它會列出 [/a.] 下包含的目錄總數、檔案及其大小。</span><span class="sxs-lookup"><span data-stu-id="38867-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="38867-111">參數</span><span class="sxs-lookup"><span data-stu-id="38867-111">PARAMETERS</span></span>

### <span data-ttu-id="38867-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="38867-112">-Account</span></span>
<span data-ttu-id="38867-113">在其中執行 filesystem 操作的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="38867-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="38867-114">-併發性</span><span class="sxs-lookup"><span data-stu-id="38867-114">-Concurrency</span></span>
<span data-ttu-id="38867-115">指出並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="38867-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="38867-116">根據系統規格，會將預設值計算為最大的精力。</span><span class="sxs-lookup"><span data-stu-id="38867-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="38867-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38867-117">-DefaultProfile</span></span>
<span data-ttu-id="38867-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38867-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38867-119">-Path</span><span class="sxs-lookup"><span data-stu-id="38867-119">-Path</span></span>
<span data-ttu-id="38867-120">指定的資料 Lake 帳戶中應該要檢索的路徑。</span><span class="sxs-lookup"><span data-stu-id="38867-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="38867-121">可以是 [/folder/file.txt "格式的檔案或資料夾，其中第一個"/"代表了檔案系統的根。</span><span class="sxs-lookup"><span data-stu-id="38867-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="38867-122">-確認</span><span class="sxs-lookup"><span data-stu-id="38867-122">-Confirm</span></span>
<span data-ttu-id="38867-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38867-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38867-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38867-124">-WhatIf</span></span>
<span data-ttu-id="38867-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38867-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38867-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38867-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38867-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38867-127">CommonParameters</span></span>
<span data-ttu-id="38867-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38867-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38867-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38867-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38867-130">輸入</span><span class="sxs-lookup"><span data-stu-id="38867-130">INPUTS</span></span>

### <span data-ttu-id="38867-131">System.object</span><span class="sxs-lookup"><span data-stu-id="38867-131">System.String</span></span>

### <span data-ttu-id="38867-132">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="38867-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="38867-133">System.object</span><span class="sxs-lookup"><span data-stu-id="38867-133">System.Int32</span></span>

## <span data-ttu-id="38867-134">輸出</span><span class="sxs-lookup"><span data-stu-id="38867-134">OUTPUTS</span></span>

### <span data-ttu-id="38867-135">DataLakeStoreChildItemSummary 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="38867-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="38867-136">筆記</span><span class="sxs-lookup"><span data-stu-id="38867-136">NOTES</span></span>

## <span data-ttu-id="38867-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="38867-137">RELATED LINKS</span></span>
