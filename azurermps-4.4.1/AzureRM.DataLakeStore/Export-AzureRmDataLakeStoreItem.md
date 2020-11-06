---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453559"
---
# <span data-ttu-id="513c6-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="513c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="513c6-102">SYNOPSIS</span></span>
<span data-ttu-id="513c6-103">從 Data Lake Store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="513c6-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="513c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="513c6-104">SYNTAX</span></span>

### <span data-ttu-id="513c6-105">預設)  (沒有診斷記錄</span><span class="sxs-lookup"><span data-stu-id="513c6-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="513c6-106">包含診斷記錄</span><span class="sxs-lookup"><span data-stu-id="513c6-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="513c6-107">說明</span><span class="sxs-lookup"><span data-stu-id="513c6-107">DESCRIPTION</span></span>
<span data-ttu-id="513c6-108">**Export AzureRmDataLakeStoreItem** Cmdlet 會從 Data Lake store 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="513c6-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="513c6-109">示例</span><span class="sxs-lookup"><span data-stu-id="513c6-109">EXAMPLES</span></span>

### <span data-ttu-id="513c6-110">範例1：從 Data Lake Store 下載專案</span><span class="sxs-lookup"><span data-stu-id="513c6-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="513c6-111">這個命令會將檔案 TestSource.csv 從 Data Lake Store 下載到 C:\Test.csv。</span><span class="sxs-lookup"><span data-stu-id="513c6-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="513c6-112">參數</span><span class="sxs-lookup"><span data-stu-id="513c6-112">PARAMETERS</span></span>

### <span data-ttu-id="513c6-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="513c6-113">-Account</span></span>
<span data-ttu-id="513c6-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="513c6-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="513c6-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="513c6-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="513c6-116">指定要針對資料夾下載並行下載的檔案數目上限。</span><span class="sxs-lookup"><span data-stu-id="513c6-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="513c6-117">預設值為 5 (5) 。</span><span class="sxs-lookup"><span data-stu-id="513c6-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="513c6-118">-目的地</span><span class="sxs-lookup"><span data-stu-id="513c6-118">-Destination</span></span>
<span data-ttu-id="513c6-119">指定要將檔案下載到哪個本機檔路徑。</span><span class="sxs-lookup"><span data-stu-id="513c6-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="513c6-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="513c6-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="513c6-121">或者，也可以指定要用來在檔案或資料夾匯入期間記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="513c6-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="513c6-122">預設為錯誤。</span><span class="sxs-lookup"><span data-stu-id="513c6-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="513c6-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="513c6-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="513c6-124">指定要在檔案或資料夾匯入期間記錄事件之診斷記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="513c6-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="513c6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="513c6-125">-Force</span></span>
<span data-ttu-id="513c6-126">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="513c6-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="513c6-127">-Path</span><span class="sxs-lookup"><span data-stu-id="513c6-127">-Path</span></span>
<span data-ttu-id="513c6-128">指定要從 Data Lake Store 下載的專案路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="513c6-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="513c6-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="513c6-129">-PerFileThreadCount</span></span>
<span data-ttu-id="513c6-130">指定要在每個檔案中使用的最大執行緒數。</span><span class="sxs-lookup"><span data-stu-id="513c6-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="513c6-131">預設值為 10 (10) 。</span><span class="sxs-lookup"><span data-stu-id="513c6-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="513c6-132">-遞迴</span><span class="sxs-lookup"><span data-stu-id="513c6-132">-Recurse</span></span>
<span data-ttu-id="513c6-133">表示資料夾下載是遞迴的。</span><span class="sxs-lookup"><span data-stu-id="513c6-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="513c6-134">-簡歷</span><span class="sxs-lookup"><span data-stu-id="513c6-134">-Resume</span></span>
<span data-ttu-id="513c6-135">表示要複製的檔案是前一個下載的接續檔案。</span><span class="sxs-lookup"><span data-stu-id="513c6-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="513c6-136">下載嘗試從最後一個未完全下載的檔案中繼續。</span><span class="sxs-lookup"><span data-stu-id="513c6-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="513c6-137">-確認</span><span class="sxs-lookup"><span data-stu-id="513c6-137">-Confirm</span></span>
<span data-ttu-id="513c6-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="513c6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513c6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513c6-139">-WhatIf</span></span>
<span data-ttu-id="513c6-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="513c6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513c6-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="513c6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513c6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513c6-142">-DefaultProfile</span></span>
<span data-ttu-id="513c6-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="513c6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="513c6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513c6-144">CommonParameters</span></span>
<span data-ttu-id="513c6-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="513c6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513c6-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="513c6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513c6-147">輸入</span><span class="sxs-lookup"><span data-stu-id="513c6-147">INPUTS</span></span>

## <span data-ttu-id="513c6-148">輸出</span><span class="sxs-lookup"><span data-stu-id="513c6-148">OUTPUTS</span></span>

### <span data-ttu-id="513c6-149">字串</span><span class="sxs-lookup"><span data-stu-id="513c6-149">string</span></span>
<span data-ttu-id="513c6-150">下載檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="513c6-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="513c6-151">筆記</span><span class="sxs-lookup"><span data-stu-id="513c6-151">NOTES</span></span>

## <span data-ttu-id="513c6-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="513c6-152">RELATED LINKS</span></span>

[<span data-ttu-id="513c6-153">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="513c6-154">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="513c6-155">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="513c6-156">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="513c6-157">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="513c6-158">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="513c6-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="513c6-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


