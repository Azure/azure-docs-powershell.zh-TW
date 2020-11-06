---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454608"
---
# <span data-ttu-id="f2fc5-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f2fc5-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="f2fc5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fc5-103">取得 Data Lake Store 中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2fc5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2fc5-104">SYNTAX</span></span>

### <span data-ttu-id="f2fc5-105">PreviewFileContent (預設) </span><span class="sxs-lookup"><span data-stu-id="f2fc5-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fc5-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="f2fc5-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fc5-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="f2fc5-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2fc5-108">說明</span><span class="sxs-lookup"><span data-stu-id="f2fc5-108">DESCRIPTION</span></span>
<span data-ttu-id="f2fc5-109">**AzureRmDataLakeStoreItemContent** Cmdlet 會取得 Data Lake store 中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="f2fc5-110">示例</span><span class="sxs-lookup"><span data-stu-id="f2fc5-110">EXAMPLES</span></span>

### <span data-ttu-id="f2fc5-111">範例1：取得檔案內容</span><span class="sxs-lookup"><span data-stu-id="f2fc5-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="f2fc5-112">這個命令會在 ContosoADL 帳戶中取得檔案 MyFile.txt 的內容。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="f2fc5-113">範例2：取得檔案的前兩列</span><span class="sxs-lookup"><span data-stu-id="f2fc5-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="f2fc5-114">這個命令會在 ContosoADL 帳戶的檔案 MyFile.txt 中取得前兩行分隔的列。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="f2fc5-115">參數</span><span class="sxs-lookup"><span data-stu-id="f2fc5-115">PARAMETERS</span></span>

### <span data-ttu-id="f2fc5-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f2fc5-116">-Account</span></span>
<span data-ttu-id="f2fc5-117">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f2fc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fc5-118">-DefaultProfile</span></span>
<span data-ttu-id="f2fc5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2fc5-120">編碼</span><span class="sxs-lookup"><span data-stu-id="f2fc5-120">-Encoding</span></span>
<span data-ttu-id="f2fc5-121">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f2fc5-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f2fc5-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f2fc5-123">清楚</span><span class="sxs-lookup"><span data-stu-id="f2fc5-123">Unknown</span></span>
- <span data-ttu-id="f2fc5-124">字串</span><span class="sxs-lookup"><span data-stu-id="f2fc5-124">String</span></span>
- <span data-ttu-id="f2fc5-125">消除</span><span class="sxs-lookup"><span data-stu-id="f2fc5-125">Unicode</span></span>
- <span data-ttu-id="f2fc5-126">位元組</span><span class="sxs-lookup"><span data-stu-id="f2fc5-126">Byte</span></span>
- <span data-ttu-id="f2fc5-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f2fc5-127">BigEndianUnicode</span></span>
- <span data-ttu-id="f2fc5-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="f2fc5-128">UTF8</span></span>
- <span data-ttu-id="f2fc5-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="f2fc5-129">UTF7</span></span>
- <span data-ttu-id="f2fc5-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="f2fc5-130">Ascii</span></span>
- <span data-ttu-id="f2fc5-131">設置</span><span class="sxs-lookup"><span data-stu-id="f2fc5-131">Default</span></span>
- <span data-ttu-id="f2fc5-132">Oem</span><span class="sxs-lookup"><span data-stu-id="f2fc5-132">Oem</span></span>
- <span data-ttu-id="f2fc5-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f2fc5-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fc5-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f2fc5-134">-Force</span></span>
<span data-ttu-id="f2fc5-135">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fc5-136">-Head</span><span class="sxs-lookup"><span data-stu-id="f2fc5-136">-Head</span></span>
<span data-ttu-id="f2fc5-137">從檔案開頭到 [預覽])  (新行分隔的列數。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="f2fc5-138">如果在第一個4mb 的資料中沒遇到新的行，就只會傳回該資料。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fc5-139">長度</span><span class="sxs-lookup"><span data-stu-id="f2fc5-139">-Length</span></span>
<span data-ttu-id="f2fc5-140">指定要取得之內容的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fc5-141">-位移</span><span class="sxs-lookup"><span data-stu-id="f2fc5-141">-Offset</span></span>
<span data-ttu-id="f2fc5-142">指定在取得內容之前要在檔案中略過的位元組數。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fc5-143">-Path</span><span class="sxs-lookup"><span data-stu-id="f2fc5-143">-Path</span></span>
<span data-ttu-id="f2fc5-144">指定檔案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f2fc5-145">-尾</span><span class="sxs-lookup"><span data-stu-id="f2fc5-145">-Tail</span></span>
<span data-ttu-id="f2fc5-146">從檔案的結尾到預覽，) 的列數 (的新行分隔。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="f2fc5-147">如果在第一個4mb 的資料中沒遇到新的行，就只會傳回該資料。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fc5-148">-確認</span><span class="sxs-lookup"><span data-stu-id="f2fc5-148">-Confirm</span></span>
<span data-ttu-id="f2fc5-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2fc5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2fc5-150">-WhatIf</span></span>
<span data-ttu-id="f2fc5-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2fc5-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2fc5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fc5-153">CommonParameters</span></span>
<span data-ttu-id="f2fc5-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fc5-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fc5-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f2fc5-156">INPUTS</span></span>

### <span data-ttu-id="f2fc5-157">System.object</span><span class="sxs-lookup"><span data-stu-id="f2fc5-157">System.String</span></span>

### <span data-ttu-id="f2fc5-158">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f2fc5-159">System.object</span><span class="sxs-lookup"><span data-stu-id="f2fc5-159">System.Int32</span></span>

### <span data-ttu-id="f2fc5-160">System.object</span><span class="sxs-lookup"><span data-stu-id="f2fc5-160">System.Int64</span></span>

### <span data-ttu-id="f2fc5-161">FileSystemCmdletProviderEncoding 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="f2fc5-162">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f2fc5-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2fc5-163">輸出</span><span class="sxs-lookup"><span data-stu-id="f2fc5-163">OUTPUTS</span></span>

### <span data-ttu-id="f2fc5-164">System.object</span><span class="sxs-lookup"><span data-stu-id="f2fc5-164">System.Byte</span></span>
<span data-ttu-id="f2fc5-165">所檢索之檔案內容的位元組資料流程表示。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="f2fc5-166">System.object</span><span class="sxs-lookup"><span data-stu-id="f2fc5-166">System.String</span></span>
<span data-ttu-id="f2fc5-167">字串表示形式 (為所檢索之檔案內容的指定編碼) 。</span><span class="sxs-lookup"><span data-stu-id="f2fc5-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="f2fc5-168">筆記</span><span class="sxs-lookup"><span data-stu-id="f2fc5-168">NOTES</span></span>

## <span data-ttu-id="f2fc5-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2fc5-169">RELATED LINKS</span></span>