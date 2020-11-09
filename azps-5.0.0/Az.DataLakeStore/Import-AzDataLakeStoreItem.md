---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285011"
---
# <span data-ttu-id="f90c7-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f90c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f90c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f90c7-103">將本機檔案或目錄上傳到 Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="f90c7-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="f90c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="f90c7-104">SYNTAX</span></span>

### <span data-ttu-id="f90c7-105">NoDiagnosticLogging (預設) </span><span class="sxs-lookup"><span data-stu-id="f90c7-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f90c7-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="f90c7-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f90c7-107">說明</span><span class="sxs-lookup"><span data-stu-id="f90c7-107">DESCRIPTION</span></span>
<span data-ttu-id="f90c7-108">匯 **入-AzDataLakeStoreItem** Cmdlet 會將本機檔案或目錄上傳到 Data Lake store。</span><span class="sxs-lookup"><span data-stu-id="f90c7-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="f90c7-109">示例</span><span class="sxs-lookup"><span data-stu-id="f90c7-109">EXAMPLES</span></span>

### <span data-ttu-id="f90c7-110">範例1：上傳檔案</span><span class="sxs-lookup"><span data-stu-id="f90c7-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="f90c7-111">這個命令會將檔案上傳 SrcFile.csv 並將它新增到 Data Lake Store 中的 MyFiles 資料夾，並以4的併發性為 File.csv。</span><span class="sxs-lookup"><span data-stu-id="f90c7-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="f90c7-112">參數</span><span class="sxs-lookup"><span data-stu-id="f90c7-112">PARAMETERS</span></span>

### <span data-ttu-id="f90c7-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f90c7-113">-Account</span></span>
<span data-ttu-id="f90c7-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f90c7-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f90c7-115">-併發性</span><span class="sxs-lookup"><span data-stu-id="f90c7-115">-Concurrency</span></span>
<span data-ttu-id="f90c7-116">表示以並行方式上傳的檔案數或區塊數。</span><span class="sxs-lookup"><span data-stu-id="f90c7-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="f90c7-117">根據系統規格，會將預設值計算為最大的精力。</span><span class="sxs-lookup"><span data-stu-id="f90c7-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="f90c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90c7-118">-DefaultProfile</span></span>
<span data-ttu-id="f90c7-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f90c7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f90c7-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="f90c7-120">-Destination</span></span>
<span data-ttu-id="f90c7-121">指定要上傳檔案或資料夾的資料 Lake Store 路徑，該路徑是從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="f90c7-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f90c7-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="f90c7-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="f90c7-123">或者，也可以指定要用來在檔案或資料夾匯入期間記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="f90c7-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="f90c7-124">預設為錯誤。</span><span class="sxs-lookup"><span data-stu-id="f90c7-124">Default is Error.</span></span>

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

### <span data-ttu-id="f90c7-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="f90c7-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="f90c7-126">指定要在檔案或資料夾匯入期間記錄事件之診斷記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="f90c7-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="f90c7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f90c7-127">-Force</span></span>
<span data-ttu-id="f90c7-128">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="f90c7-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f90c7-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="f90c7-129">-ForceBinary</span></span>
<span data-ttu-id="f90c7-130">表示複製的檔案 (s) 應該複製，而不需考慮在附加的新行保留。</span><span class="sxs-lookup"><span data-stu-id="f90c7-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="f90c7-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f90c7-131">-Path</span></span>
<span data-ttu-id="f90c7-132">指定要上傳的檔案或資料夾的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="f90c7-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="f90c7-133">-遞迴</span><span class="sxs-lookup"><span data-stu-id="f90c7-133">-Recurse</span></span>
<span data-ttu-id="f90c7-134">指示此操作應該上傳所有子資料夾中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="f90c7-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="f90c7-135">-簡歷</span><span class="sxs-lookup"><span data-stu-id="f90c7-135">-Resume</span></span>
<span data-ttu-id="f90c7-136">表示檔案 (s) 被覆制為前一個上傳的延續。</span><span class="sxs-lookup"><span data-stu-id="f90c7-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="f90c7-137">這會導致系統嘗試從沒有完全上傳的最後一個檔案繼續。</span><span class="sxs-lookup"><span data-stu-id="f90c7-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="f90c7-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f90c7-138">-Confirm</span></span>
<span data-ttu-id="f90c7-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f90c7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f90c7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f90c7-140">-WhatIf</span></span>
<span data-ttu-id="f90c7-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f90c7-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f90c7-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f90c7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f90c7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90c7-143">CommonParameters</span></span>
<span data-ttu-id="f90c7-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f90c7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90c7-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f90c7-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90c7-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f90c7-146">INPUTS</span></span>

### <span data-ttu-id="f90c7-147">System.object</span><span class="sxs-lookup"><span data-stu-id="f90c7-147">System.String</span></span>

### <span data-ttu-id="f90c7-148">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f90c7-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f90c7-149">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f90c7-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f90c7-150">System.object</span><span class="sxs-lookup"><span data-stu-id="f90c7-150">System.Int32</span></span>

### <span data-ttu-id="f90c7-151">LogLevel 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f90c7-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="f90c7-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f90c7-152">OUTPUTS</span></span>

### <span data-ttu-id="f90c7-153">System.object</span><span class="sxs-lookup"><span data-stu-id="f90c7-153">System.String</span></span>

## <span data-ttu-id="f90c7-154">筆記</span><span class="sxs-lookup"><span data-stu-id="f90c7-154">NOTES</span></span>

## <span data-ttu-id="f90c7-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f90c7-155">RELATED LINKS</span></span>

[<span data-ttu-id="f90c7-156">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f90c7-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f90c7-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="f90c7-159">移動流覽 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="f90c7-160">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f90c7-161">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f90c7-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f90c7-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


