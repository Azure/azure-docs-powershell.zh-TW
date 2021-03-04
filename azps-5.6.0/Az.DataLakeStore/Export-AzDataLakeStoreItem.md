---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 72fcb1ecd78b2682fe678af8b75b36032ff58b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903249"
---
# <span data-ttu-id="dacb8-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="dacb8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dacb8-102">SYNOPSIS</span></span>
<span data-ttu-id="dacb8-103">從 Data Lake Store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="dacb8-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="dacb8-104">語法</span><span class="sxs-lookup"><span data-stu-id="dacb8-104">SYNTAX</span></span>

### <span data-ttu-id="dacb8-105">NoDiagnosticLogging (預設) </span><span class="sxs-lookup"><span data-stu-id="dacb8-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacb8-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="dacb8-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dacb8-107">描述</span><span class="sxs-lookup"><span data-stu-id="dacb8-107">DESCRIPTION</span></span>
<span data-ttu-id="dacb8-108">**Export-AzDataLakeStoreItem** Cmdlet 會從 Data Lake Store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="dacb8-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="dacb8-109">例子</span><span class="sxs-lookup"><span data-stu-id="dacb8-109">EXAMPLES</span></span>

### <span data-ttu-id="dacb8-110">範例 1：從 Data Lake Store 下載專案</span><span class="sxs-lookup"><span data-stu-id="dacb8-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="dacb8-111">此命令會從 Data Lake 市TestSource.csv下載檔案，並C:\Test.csv 4。</span><span class="sxs-lookup"><span data-stu-id="dacb8-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="dacb8-112">參數</span><span class="sxs-lookup"><span data-stu-id="dacb8-112">PARAMETERS</span></span>

### <span data-ttu-id="dacb8-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="dacb8-113">-Account</span></span>
<span data-ttu-id="dacb8-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dacb8-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="dacb8-115">-並行</span><span class="sxs-lookup"><span data-stu-id="dacb8-115">-Concurrency</span></span>
<span data-ttu-id="dacb8-116">表示要平行下載的檔案或區塊數目。</span><span class="sxs-lookup"><span data-stu-id="dacb8-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="dacb8-117">根據系統規格，預設會以最佳效果計算。</span><span class="sxs-lookup"><span data-stu-id="dacb8-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="dacb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacb8-118">-DefaultProfile</span></span>
<span data-ttu-id="dacb8-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dacb8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dacb8-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="dacb8-120">-Destination</span></span>
<span data-ttu-id="dacb8-121">指定要下載檔案的當地檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="dacb8-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="dacb8-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="dacb8-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="dacb8-123">選擇性地指出在檔案或資料夾匯出期間，用於記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="dacb8-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="dacb8-124">預設值為錯誤。</span><span class="sxs-lookup"><span data-stu-id="dacb8-124">Default is Error.</span></span>

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

### <span data-ttu-id="dacb8-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="dacb8-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="dacb8-126">指定診斷記錄在檔案或資料夾匯出期間記錄事件的路徑。</span><span class="sxs-lookup"><span data-stu-id="dacb8-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="dacb8-127">-強制</span><span class="sxs-lookup"><span data-stu-id="dacb8-127">-Force</span></span>
<span data-ttu-id="dacb8-128">表示此作業可以覆寫目標檔案 ，如果已存在。</span><span class="sxs-lookup"><span data-stu-id="dacb8-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="dacb8-129">-路徑</span><span class="sxs-lookup"><span data-stu-id="dacb8-129">-Path</span></span>
<span data-ttu-id="dacb8-130">指定從 Data Lake Store 下載專案的路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="dacb8-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="dacb8-131">-遞迴</span><span class="sxs-lookup"><span data-stu-id="dacb8-131">-Recurse</span></span>
<span data-ttu-id="dacb8-132">表示資料夾下載為遞迴。</span><span class="sxs-lookup"><span data-stu-id="dacb8-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="dacb8-133">-履歷表</span><span class="sxs-lookup"><span data-stu-id="dacb8-133">-Resume</span></span>
<span data-ttu-id="dacb8-134">表示要複製 () 檔案是上一次下載的延續。</span><span class="sxs-lookup"><span data-stu-id="dacb8-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="dacb8-135">這會使系統嘗試從未完全下載的最後一個檔案繼續。</span><span class="sxs-lookup"><span data-stu-id="dacb8-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="dacb8-136">-確認</span><span class="sxs-lookup"><span data-stu-id="dacb8-136">-Confirm</span></span>
<span data-ttu-id="dacb8-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dacb8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacb8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacb8-138">-WhatIf</span></span>
<span data-ttu-id="dacb8-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dacb8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dacb8-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dacb8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacb8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacb8-141">CommonParameters</span></span>
<span data-ttu-id="dacb8-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dacb8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacb8-143">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dacb8-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacb8-144">輸入</span><span class="sxs-lookup"><span data-stu-id="dacb8-144">INPUTS</span></span>

### <span data-ttu-id="dacb8-145">System.String</span><span class="sxs-lookup"><span data-stu-id="dacb8-145">System.String</span></span>

### <span data-ttu-id="dacb8-146">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="dacb8-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="dacb8-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dacb8-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dacb8-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="dacb8-148">System.Int32</span></span>

### <span data-ttu-id="dacb8-149">Microsoft.Azure.Commands.DataLakeStore.models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="dacb8-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="dacb8-150">輸出</span><span class="sxs-lookup"><span data-stu-id="dacb8-150">OUTPUTS</span></span>

### <span data-ttu-id="dacb8-151">System.String</span><span class="sxs-lookup"><span data-stu-id="dacb8-151">System.String</span></span>

## <span data-ttu-id="dacb8-152">筆記</span><span class="sxs-lookup"><span data-stu-id="dacb8-152">NOTES</span></span>

## <span data-ttu-id="dacb8-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="dacb8-153">RELATED LINKS</span></span>

[<span data-ttu-id="dacb8-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="dacb8-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="dacb8-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="dacb8-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="dacb8-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="dacb8-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="dacb8-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dacb8-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


