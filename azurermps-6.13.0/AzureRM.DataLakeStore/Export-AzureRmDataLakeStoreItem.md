---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451219"
---
# <span data-ttu-id="5a097-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5a097-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a097-102">SYNOPSIS</span></span>
<span data-ttu-id="5a097-103">從 Data Lake Store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="5a097-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a097-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a097-104">SYNTAX</span></span>

### <span data-ttu-id="5a097-105">NoDiagnosticLogging (預設) </span><span class="sxs-lookup"><span data-stu-id="5a097-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a097-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="5a097-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a097-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a097-107">DESCRIPTION</span></span>
<span data-ttu-id="5a097-108">**Export AzureRmDataLakeStoreItem** Cmdlet 會從 Data Lake store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="5a097-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="5a097-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a097-109">EXAMPLES</span></span>

### <span data-ttu-id="5a097-110">範例1：從 Data Lake Store 下載專案</span><span class="sxs-lookup"><span data-stu-id="5a097-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="5a097-111">這個命令會從 Data Lake Store 將檔案 TestSource.csv 下載到具有4個併發性的 C:\Test.csv。</span><span class="sxs-lookup"><span data-stu-id="5a097-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="5a097-112">參數</span><span class="sxs-lookup"><span data-stu-id="5a097-112">PARAMETERS</span></span>

### <span data-ttu-id="5a097-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="5a097-113">-Account</span></span>
<span data-ttu-id="5a097-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a097-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5a097-115">-併發性</span><span class="sxs-lookup"><span data-stu-id="5a097-115">-Concurrency</span></span>
<span data-ttu-id="5a097-116">表示要並行下載的檔案數或區塊數。</span><span class="sxs-lookup"><span data-stu-id="5a097-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="5a097-117">根據系統規格，會將預設值計算為最大的精力。</span><span class="sxs-lookup"><span data-stu-id="5a097-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="5a097-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a097-118">-DefaultProfile</span></span>
<span data-ttu-id="5a097-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a097-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a097-120">-目的地</span><span class="sxs-lookup"><span data-stu-id="5a097-120">-Destination</span></span>
<span data-ttu-id="5a097-121">指定要將檔案下載到哪個本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="5a097-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="5a097-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5a097-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5a097-123">或者，也可以指定要用來在檔案或資料夾匯入期間記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="5a097-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5a097-124">預設為錯誤。</span><span class="sxs-lookup"><span data-stu-id="5a097-124">Default is Error.</span></span>

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

### <span data-ttu-id="5a097-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5a097-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="5a097-126">指定要在檔案或資料夾匯入期間記錄事件之診斷記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="5a097-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="5a097-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5a097-127">-Force</span></span>
<span data-ttu-id="5a097-128">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="5a097-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="5a097-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5a097-129">-Path</span></span>
<span data-ttu-id="5a097-130">指定要從 Data Lake Store 下載的專案路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="5a097-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="5a097-131">-遞迴</span><span class="sxs-lookup"><span data-stu-id="5a097-131">-Recurse</span></span>
<span data-ttu-id="5a097-132">表示資料夾下載是遞迴的。</span><span class="sxs-lookup"><span data-stu-id="5a097-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="5a097-133">-簡歷</span><span class="sxs-lookup"><span data-stu-id="5a097-133">-Resume</span></span>
<span data-ttu-id="5a097-134">表示檔案 (s) 被覆制為前一個下載的接續。</span><span class="sxs-lookup"><span data-stu-id="5a097-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="5a097-135">這會導致系統嘗試從沒有完全下載的最後一個檔案繼續。</span><span class="sxs-lookup"><span data-stu-id="5a097-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="5a097-136">-確認</span><span class="sxs-lookup"><span data-stu-id="5a097-136">-Confirm</span></span>
<span data-ttu-id="5a097-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a097-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a097-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a097-138">-WhatIf</span></span>
<span data-ttu-id="5a097-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a097-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a097-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a097-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a097-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a097-141">CommonParameters</span></span>
<span data-ttu-id="5a097-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a097-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a097-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a097-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a097-144">輸入</span><span class="sxs-lookup"><span data-stu-id="5a097-144">INPUTS</span></span>

### <span data-ttu-id="5a097-145">System.object</span><span class="sxs-lookup"><span data-stu-id="5a097-145">System.String</span></span>

### <span data-ttu-id="5a097-146">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="5a097-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5a097-147">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5a097-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5a097-148">System.object</span><span class="sxs-lookup"><span data-stu-id="5a097-148">System.Int32</span></span>

### <span data-ttu-id="5a097-149">LogLevel 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="5a097-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="5a097-150">輸出</span><span class="sxs-lookup"><span data-stu-id="5a097-150">OUTPUTS</span></span>

### <span data-ttu-id="5a097-151">System.object</span><span class="sxs-lookup"><span data-stu-id="5a097-151">System.String</span></span>
<span data-ttu-id="5a097-152">下載檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="5a097-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="5a097-153">筆記</span><span class="sxs-lookup"><span data-stu-id="5a097-153">NOTES</span></span>

## <span data-ttu-id="5a097-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a097-154">RELATED LINKS</span></span>

[<span data-ttu-id="5a097-155">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a097-156">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a097-157">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a097-158">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a097-159">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a097-160">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5a097-161">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5a097-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


