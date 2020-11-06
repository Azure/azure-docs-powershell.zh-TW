---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451524"
---
# <span data-ttu-id="343f5-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="343f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="343f5-102">SYNOPSIS</span></span>
<span data-ttu-id="343f5-103">將本機檔案或目錄上傳到 Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="343f5-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="343f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="343f5-104">SYNTAX</span></span>

### <span data-ttu-id="343f5-105">NoDiagnosticLogging (預設) </span><span class="sxs-lookup"><span data-stu-id="343f5-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="343f5-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="343f5-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343f5-107">說明</span><span class="sxs-lookup"><span data-stu-id="343f5-107">DESCRIPTION</span></span>
<span data-ttu-id="343f5-108">匯 **入-AzureRmDataLakeStoreItem** Cmdlet 會將本機檔案或目錄上傳到 Data Lake store。</span><span class="sxs-lookup"><span data-stu-id="343f5-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="343f5-109">示例</span><span class="sxs-lookup"><span data-stu-id="343f5-109">EXAMPLES</span></span>

### <span data-ttu-id="343f5-110">範例1：上傳檔案</span><span class="sxs-lookup"><span data-stu-id="343f5-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="343f5-111">這個命令會將檔案上傳 SrcFile.csv 並將它新增到 Data Lake Store 中的 MyFiles 資料夾，並以4的併發性為 File.csv。</span><span class="sxs-lookup"><span data-stu-id="343f5-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="343f5-112">參數</span><span class="sxs-lookup"><span data-stu-id="343f5-112">PARAMETERS</span></span>

### <span data-ttu-id="343f5-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="343f5-113">-Account</span></span>
<span data-ttu-id="343f5-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="343f5-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-115">-併發性</span><span class="sxs-lookup"><span data-stu-id="343f5-115">-Concurrency</span></span>
<span data-ttu-id="343f5-116">表示以並行方式上傳的檔案數或區塊數。</span><span class="sxs-lookup"><span data-stu-id="343f5-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="343f5-117">根據系統規格，會將預設值計算為最大的精力。</span><span class="sxs-lookup"><span data-stu-id="343f5-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="343f5-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="343f5-119">表示要針對資料夾上傳並行上傳的檔案數目上限。</span><span class="sxs-lookup"><span data-stu-id="343f5-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="343f5-120">根據資料夾和檔案大小，會將預設值計算為最大的努力</span><span class="sxs-lookup"><span data-stu-id="343f5-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343f5-121">-DefaultProfile</span></span>
<span data-ttu-id="343f5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="343f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-123">-目的地</span><span class="sxs-lookup"><span data-stu-id="343f5-123">-Destination</span></span>
<span data-ttu-id="343f5-124">指定要上傳檔案或資料夾的資料 Lake Store 路徑，該路徑是從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="343f5-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="343f5-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="343f5-126">或者，也可以指定要用來在檔案或資料夾匯入期間記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="343f5-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="343f5-127">預設為錯誤。</span><span class="sxs-lookup"><span data-stu-id="343f5-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="343f5-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="343f5-129">指定要在檔案或資料夾匯入期間記錄事件之診斷記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="343f5-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-130">-Force</span><span class="sxs-lookup"><span data-stu-id="343f5-130">-Force</span></span>
<span data-ttu-id="343f5-131">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="343f5-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="343f5-132">-ForceBinary</span></span>
<span data-ttu-id="343f5-133">表示複製的檔案 (s) 應該複製，而不需考慮在附加的新行保留。</span><span class="sxs-lookup"><span data-stu-id="343f5-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-134">-Path</span><span class="sxs-lookup"><span data-stu-id="343f5-134">-Path</span></span>
<span data-ttu-id="343f5-135">指定要上傳的檔案或資料夾的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="343f5-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="343f5-136">-PerFileThreadCount</span></span>
<span data-ttu-id="343f5-137">表示每個檔案使用的最大執行緒數。</span><span class="sxs-lookup"><span data-stu-id="343f5-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="343f5-138">根據資料夾和檔案大小，會將預設值計算為最大的努力</span><span class="sxs-lookup"><span data-stu-id="343f5-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-139">-遞迴</span><span class="sxs-lookup"><span data-stu-id="343f5-139">-Recurse</span></span>
<span data-ttu-id="343f5-140">指示此操作應該上傳所有子資料夾中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="343f5-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-141">-簡歷</span><span class="sxs-lookup"><span data-stu-id="343f5-141">-Resume</span></span>
<span data-ttu-id="343f5-142">表示檔案 (s) 被覆制為前一個上傳的延續。</span><span class="sxs-lookup"><span data-stu-id="343f5-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="343f5-143">這會導致系統嘗試從沒有完全上傳的最後一個檔案繼續。</span><span class="sxs-lookup"><span data-stu-id="343f5-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-144">-確認</span><span class="sxs-lookup"><span data-stu-id="343f5-144">-Confirm</span></span>
<span data-ttu-id="343f5-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="343f5-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343f5-146">-WhatIf</span></span>
<span data-ttu-id="343f5-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="343f5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343f5-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="343f5-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="343f5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343f5-149">CommonParameters</span></span>
<span data-ttu-id="343f5-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="343f5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343f5-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="343f5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343f5-152">輸入</span><span class="sxs-lookup"><span data-stu-id="343f5-152">INPUTS</span></span>

### <span data-ttu-id="343f5-153">所有</span><span class="sxs-lookup"><span data-stu-id="343f5-153">None</span></span>
<span data-ttu-id="343f5-154">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="343f5-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="343f5-155">輸出</span><span class="sxs-lookup"><span data-stu-id="343f5-155">OUTPUTS</span></span>

### <span data-ttu-id="343f5-156">字串</span><span class="sxs-lookup"><span data-stu-id="343f5-156">string</span></span>
<span data-ttu-id="343f5-157">Data Lake Store 帳戶中的完整路徑到上傳的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="343f5-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="343f5-158">筆記</span><span class="sxs-lookup"><span data-stu-id="343f5-158">NOTES</span></span>

## <span data-ttu-id="343f5-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="343f5-159">RELATED LINKS</span></span>

[<span data-ttu-id="343f5-160">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="343f5-161">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="343f5-162">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="343f5-163">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="343f5-164">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="343f5-165">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="343f5-166">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="343f5-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


