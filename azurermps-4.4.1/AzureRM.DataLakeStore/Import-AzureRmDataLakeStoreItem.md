---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625191"
---
# <span data-ttu-id="83b52-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="83b52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83b52-102">SYNOPSIS</span></span>
<span data-ttu-id="83b52-103">將本機檔案或目錄上傳到 Data Lake Store。</span><span class="sxs-lookup"><span data-stu-id="83b52-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b52-104">句法</span><span class="sxs-lookup"><span data-stu-id="83b52-104">SYNTAX</span></span>

### <span data-ttu-id="83b52-105">預設)  (沒有診斷記錄</span><span class="sxs-lookup"><span data-stu-id="83b52-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b52-106">包含診斷記錄</span><span class="sxs-lookup"><span data-stu-id="83b52-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b52-107">說明</span><span class="sxs-lookup"><span data-stu-id="83b52-107">DESCRIPTION</span></span>
<span data-ttu-id="83b52-108">匯 **入-AzureRmDataLakeStoreItem** Cmdlet 會將本機檔案或目錄上傳到 Data Lake store。</span><span class="sxs-lookup"><span data-stu-id="83b52-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="83b52-109">示例</span><span class="sxs-lookup"><span data-stu-id="83b52-109">EXAMPLES</span></span>

### <span data-ttu-id="83b52-110">範例1：上傳檔案</span><span class="sxs-lookup"><span data-stu-id="83b52-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="83b52-111">這個命令會將檔案上傳 SrcFile.csv 並將它新增到 Data Lake Store 中的 MyFiles 資料夾，File.csv。</span><span class="sxs-lookup"><span data-stu-id="83b52-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="83b52-112">參數</span><span class="sxs-lookup"><span data-stu-id="83b52-112">PARAMETERS</span></span>

### <span data-ttu-id="83b52-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="83b52-113">-Account</span></span>
<span data-ttu-id="83b52-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="83b52-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="83b52-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="83b52-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="83b52-116">指定要以並行方式上傳資料夾上傳的檔案數目上限。</span><span class="sxs-lookup"><span data-stu-id="83b52-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="83b52-117">預設值為 5 (5) 。</span><span class="sxs-lookup"><span data-stu-id="83b52-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83b52-118">-目的地</span><span class="sxs-lookup"><span data-stu-id="83b52-118">-Destination</span></span>
<span data-ttu-id="83b52-119">指定要上傳檔案或資料夾的資料 Lake Store 路徑，該路徑是從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="83b52-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="83b52-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="83b52-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="83b52-121">或者，也可以指定要用來在檔案或資料夾匯入期間記錄事件的診斷記錄層級。</span><span class="sxs-lookup"><span data-stu-id="83b52-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="83b52-122">預設為錯誤。</span><span class="sxs-lookup"><span data-stu-id="83b52-122">Default is Error.</span></span>

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

### <span data-ttu-id="83b52-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="83b52-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="83b52-124">指定要在檔案或資料夾匯入期間記錄事件之診斷記錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="83b52-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="83b52-125">-Force</span><span class="sxs-lookup"><span data-stu-id="83b52-125">-Force</span></span>
<span data-ttu-id="83b52-126">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="83b52-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="83b52-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="83b52-127">-ForceBinary</span></span>
<span data-ttu-id="83b52-128">表示此操作會將檔案上傳成二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="83b52-128">Indicates that this operation uploads the file as a binary file.</span></span>

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

### <span data-ttu-id="83b52-129">-Path</span><span class="sxs-lookup"><span data-stu-id="83b52-129">-Path</span></span>
<span data-ttu-id="83b52-130">指定要上傳的檔案或資料夾的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="83b52-130">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="83b52-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="83b52-131">-PerFileThreadCount</span></span>
<span data-ttu-id="83b52-132">指定要在每個檔案中使用的最大執行緒數。</span><span class="sxs-lookup"><span data-stu-id="83b52-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="83b52-133">預設值為 10 (10) 。</span><span class="sxs-lookup"><span data-stu-id="83b52-133">The default value is ten (10).</span></span>

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

### <span data-ttu-id="83b52-134">-遞迴</span><span class="sxs-lookup"><span data-stu-id="83b52-134">-Recurse</span></span>
<span data-ttu-id="83b52-135">指示此操作應該上傳所有子資料夾中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="83b52-135">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="83b52-136">-簡歷</span><span class="sxs-lookup"><span data-stu-id="83b52-136">-Resume</span></span>
<span data-ttu-id="83b52-137">表示此作業應該繼續先前已取消或失敗的上傳。</span><span class="sxs-lookup"><span data-stu-id="83b52-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

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

### <span data-ttu-id="83b52-138">-確認</span><span class="sxs-lookup"><span data-stu-id="83b52-138">-Confirm</span></span>
<span data-ttu-id="83b52-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83b52-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b52-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b52-140">-WhatIf</span></span>
<span data-ttu-id="83b52-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83b52-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b52-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83b52-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b52-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b52-143">-DefaultProfile</span></span>
<span data-ttu-id="83b52-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83b52-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83b52-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b52-145">CommonParameters</span></span>
<span data-ttu-id="83b52-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83b52-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b52-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83b52-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b52-148">輸入</span><span class="sxs-lookup"><span data-stu-id="83b52-148">INPUTS</span></span>

## <span data-ttu-id="83b52-149">輸出</span><span class="sxs-lookup"><span data-stu-id="83b52-149">OUTPUTS</span></span>

### <span data-ttu-id="83b52-150">字串</span><span class="sxs-lookup"><span data-stu-id="83b52-150">string</span></span>
<span data-ttu-id="83b52-151">Data Lake Store 帳戶中的完整路徑到上傳的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="83b52-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="83b52-152">筆記</span><span class="sxs-lookup"><span data-stu-id="83b52-152">NOTES</span></span>

## <span data-ttu-id="83b52-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="83b52-153">RELATED LINKS</span></span>

[<span data-ttu-id="83b52-154">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83b52-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83b52-156">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83b52-157">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83b52-158">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83b52-159">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="83b52-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="83b52-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


