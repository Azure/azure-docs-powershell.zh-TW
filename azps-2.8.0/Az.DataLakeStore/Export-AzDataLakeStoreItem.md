---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f7b23188f0ba56a62f2442626f406b134ccd48e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612805"
---
# <span data-ttu-id="93a09-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="93a09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93a09-102">SYNOPSIS</span></span>
<span data-ttu-id="93a09-103">從 Data Lake Store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="93a09-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="93a09-104">句法</span><span class="sxs-lookup"><span data-stu-id="93a09-104">SYNTAX</span></span>

### <span data-ttu-id="93a09-105">NoDiagnosticLogging (預設) </span><span class="sxs-lookup"><span data-stu-id="93a09-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93a09-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="93a09-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93a09-107">說明</span><span class="sxs-lookup"><span data-stu-id="93a09-107">DESCRIPTION</span></span>
<span data-ttu-id="93a09-108">**Export AzDataLakeStoreItem** Cmdlet 會從 Data Lake store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="93a09-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="93a09-109">示例</span><span class="sxs-lookup"><span data-stu-id="93a09-109">EXAMPLES</span></span>

### <span data-ttu-id="93a09-110">範例1：從 Data Lake Store 下載專案</span><span class="sxs-lookup"><span data-stu-id="93a09-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="93a09-111">這個命令會從 Data Lake Store 將檔案 TestSource.csv 下載到具有4個併發性的 C:\Test.csv。</span><span class="sxs-lookup"><span data-stu-id="93a09-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="93a09-112">參數</span><span class="sxs-lookup"><span data-stu-id="93a09-112">PARAMETERS</span></span>

### <span data-ttu-id="93a09-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="93a09-113">-Account</span></span>
<span data-ttu-id="93a09-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="93a09-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="93a09-115">-併發性</span><span class="sxs-lookup"><span data-stu-id="93a09-115">-Concurrency</span></span>
<span data-ttu-id="93a09-116">表示要並行下載的檔案數或區塊數。</span><span class="sxs-lookup"><span data-stu-id="93a09-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="93a09-117">根據系統規格，會將預設值計算為最大的精力。</span><span class="sxs-lookup"><span data-stu-id="93a09-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="93a09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93a09-118">-DefaultProfile</span></span>
<span data-ttu-id="93a09-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93a09-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93a09-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="93a09-120">-Destination</span></span>
<span data-ttu-id="93a09-121">指定要將檔案下載到哪個本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="93a09-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a09-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="93a09-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="93a09-123">或者，也可以指定要用來在檔案或資料夾匯入期間記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="93a09-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="93a09-124">預設為錯誤。</span><span class="sxs-lookup"><span data-stu-id="93a09-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a09-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="93a09-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="93a09-126">指定要在檔案或資料夾匯入期間記錄事件之診斷記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="93a09-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a09-127">-Force</span><span class="sxs-lookup"><span data-stu-id="93a09-127">-Force</span></span>
<span data-ttu-id="93a09-128">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="93a09-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a09-129">-Path</span><span class="sxs-lookup"><span data-stu-id="93a09-129">-Path</span></span>
<span data-ttu-id="93a09-130">指定要從 Data Lake Store 下載的專案路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="93a09-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93a09-131">-遞迴</span><span class="sxs-lookup"><span data-stu-id="93a09-131">-Recurse</span></span>
<span data-ttu-id="93a09-132">表示資料夾下載是遞迴的。</span><span class="sxs-lookup"><span data-stu-id="93a09-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="93a09-133">-簡歷</span><span class="sxs-lookup"><span data-stu-id="93a09-133">-Resume</span></span>
<span data-ttu-id="93a09-134">表示檔案 (s) 被覆制為前一個下載的接續。</span><span class="sxs-lookup"><span data-stu-id="93a09-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="93a09-135">這會導致系統嘗試從沒有完全下載的最後一個檔案繼續。</span><span class="sxs-lookup"><span data-stu-id="93a09-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="93a09-136">-確認</span><span class="sxs-lookup"><span data-stu-id="93a09-136">-Confirm</span></span>
<span data-ttu-id="93a09-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93a09-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93a09-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93a09-138">-WhatIf</span></span>
<span data-ttu-id="93a09-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93a09-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93a09-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93a09-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93a09-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93a09-141">CommonParameters</span></span>
<span data-ttu-id="93a09-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93a09-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93a09-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93a09-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93a09-144">輸入</span><span class="sxs-lookup"><span data-stu-id="93a09-144">INPUTS</span></span>

### <span data-ttu-id="93a09-145">System.object</span><span class="sxs-lookup"><span data-stu-id="93a09-145">System.String</span></span>

### <span data-ttu-id="93a09-146">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="93a09-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="93a09-147">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="93a09-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="93a09-148">System.object</span><span class="sxs-lookup"><span data-stu-id="93a09-148">System.Int32</span></span>

### <span data-ttu-id="93a09-149">LogLevel 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="93a09-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="93a09-150">輸出</span><span class="sxs-lookup"><span data-stu-id="93a09-150">OUTPUTS</span></span>

### <span data-ttu-id="93a09-151">System.object</span><span class="sxs-lookup"><span data-stu-id="93a09-151">System.String</span></span>

## <span data-ttu-id="93a09-152">筆記</span><span class="sxs-lookup"><span data-stu-id="93a09-152">NOTES</span></span>

## <span data-ttu-id="93a09-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="93a09-153">RELATED LINKS</span></span>

[<span data-ttu-id="93a09-154">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="93a09-155">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="93a09-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="93a09-157">移動流覽 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="93a09-158">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="93a09-159">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="93a09-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="93a09-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

