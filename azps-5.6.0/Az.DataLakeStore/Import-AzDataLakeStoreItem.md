---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: afe19fed7cd8de43cb28b7b3f73b01312cdd42fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913246"
---
# <span data-ttu-id="5f76a-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="5f76a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5f76a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f76a-103">將本地檔案或目錄上傳到 Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="5f76a-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="5f76a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5f76a-104">SYNTAX</span></span>

### <span data-ttu-id="5f76a-105">NoDiagnosticLogging (預設) </span><span class="sxs-lookup"><span data-stu-id="5f76a-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f76a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="5f76a-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f76a-107">描述</span><span class="sxs-lookup"><span data-stu-id="5f76a-107">DESCRIPTION</span></span>
<span data-ttu-id="5f76a-108">**Import-AzDataLakeStoreItem** Cmdlet 會上傳本地檔案或目錄至 Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="5f76a-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="5f76a-109">例子</span><span class="sxs-lookup"><span data-stu-id="5f76a-109">EXAMPLES</span></span>

### <span data-ttu-id="5f76a-110">範例 1：上傳檔案</span><span class="sxs-lookup"><span data-stu-id="5f76a-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="5f76a-111">此命令會將檔案上傳SrcFile.csv並將它新增到 Data Lake Store 中的 MyFiles 資料夾，File.csv 4 的並行處理。</span><span class="sxs-lookup"><span data-stu-id="5f76a-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="5f76a-112">參數</span><span class="sxs-lookup"><span data-stu-id="5f76a-112">PARAMETERS</span></span>

### <span data-ttu-id="5f76a-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="5f76a-113">-Account</span></span>
<span data-ttu-id="5f76a-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f76a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5f76a-115">-並行</span><span class="sxs-lookup"><span data-stu-id="5f76a-115">-Concurrency</span></span>
<span data-ttu-id="5f76a-116">表示要平行上傳的檔案或區塊數目。</span><span class="sxs-lookup"><span data-stu-id="5f76a-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="5f76a-117">根據系統規格，預設會以最佳效果計算。</span><span class="sxs-lookup"><span data-stu-id="5f76a-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="5f76a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f76a-118">-DefaultProfile</span></span>
<span data-ttu-id="5f76a-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f76a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f76a-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="5f76a-120">-Destination</span></span>
<span data-ttu-id="5f76a-121">指定要上傳檔案或資料夾的 Data Lake Store 路徑，從 / (根目錄開始) 。</span><span class="sxs-lookup"><span data-stu-id="5f76a-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5f76a-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5f76a-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5f76a-123">選擇性地指出在檔案或資料夾匯出期間，用於記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="5f76a-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5f76a-124">預設值為錯誤。</span><span class="sxs-lookup"><span data-stu-id="5f76a-124">Default is Error.</span></span>

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

### <span data-ttu-id="5f76a-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5f76a-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="5f76a-126">指定診斷記錄在檔案或資料夾匯出期間記錄事件的路徑。</span><span class="sxs-lookup"><span data-stu-id="5f76a-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="5f76a-127">-強制</span><span class="sxs-lookup"><span data-stu-id="5f76a-127">-Force</span></span>
<span data-ttu-id="5f76a-128">表示此作業可以覆寫目標檔案 ，如果已存在。</span><span class="sxs-lookup"><span data-stu-id="5f76a-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="5f76a-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="5f76a-129">-ForceBinary</span></span>
<span data-ttu-id="5f76a-130">表示要複製 () 的檔案，而不需要考慮在附加專案之間保留新的線條。</span><span class="sxs-lookup"><span data-stu-id="5f76a-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="5f76a-131">-路徑</span><span class="sxs-lookup"><span data-stu-id="5f76a-131">-Path</span></span>
<span data-ttu-id="5f76a-132">指定要上傳之檔案或資料夾的當地路徑。</span><span class="sxs-lookup"><span data-stu-id="5f76a-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="5f76a-133">-遞迴</span><span class="sxs-lookup"><span data-stu-id="5f76a-133">-Recurse</span></span>
<span data-ttu-id="5f76a-134">表示此作業應上傳所有子資料夾的所有專案。</span><span class="sxs-lookup"><span data-stu-id="5f76a-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="5f76a-135">-履歷表</span><span class="sxs-lookup"><span data-stu-id="5f76a-135">-Resume</span></span>
<span data-ttu-id="5f76a-136">表示要複製 () 檔案是上一次上傳的延續。</span><span class="sxs-lookup"><span data-stu-id="5f76a-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="5f76a-137">這會使系統嘗試從上次未完全上傳的檔案繼續。</span><span class="sxs-lookup"><span data-stu-id="5f76a-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="5f76a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="5f76a-138">-Confirm</span></span>
<span data-ttu-id="5f76a-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5f76a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f76a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f76a-140">-WhatIf</span></span>
<span data-ttu-id="5f76a-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5f76a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f76a-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5f76a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f76a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f76a-143">CommonParameters</span></span>
<span data-ttu-id="5f76a-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5f76a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f76a-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5f76a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f76a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="5f76a-146">INPUTS</span></span>

### <span data-ttu-id="5f76a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5f76a-147">System.String</span></span>

### <span data-ttu-id="5f76a-148">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5f76a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5f76a-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f76a-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5f76a-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5f76a-150">System.Int32</span></span>

### <span data-ttu-id="5f76a-151">Microsoft.Azure.Commands.DataLakeStore.models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="5f76a-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="5f76a-152">輸出</span><span class="sxs-lookup"><span data-stu-id="5f76a-152">OUTPUTS</span></span>

### <span data-ttu-id="5f76a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5f76a-153">System.String</span></span>

## <span data-ttu-id="5f76a-154">筆記</span><span class="sxs-lookup"><span data-stu-id="5f76a-154">NOTES</span></span>

## <span data-ttu-id="5f76a-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f76a-155">RELATED LINKS</span></span>

[<span data-ttu-id="5f76a-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="5f76a-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="5f76a-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="5f76a-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="5f76a-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="5f76a-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="5f76a-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5f76a-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


