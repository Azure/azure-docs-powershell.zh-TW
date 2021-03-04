---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 8f128396982be5e461e450d320c0264dddb09fa8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904509"
---
# <span data-ttu-id="3b567-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="3b567-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="3b567-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b567-102">SYNOPSIS</span></span>
<span data-ttu-id="3b567-103">在 Data Lake Store 中獲取檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3b567-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="3b567-104">語法</span><span class="sxs-lookup"><span data-stu-id="3b567-104">SYNTAX</span></span>

### <span data-ttu-id="3b567-105">PreviewFileContent (預設) </span><span class="sxs-lookup"><span data-stu-id="3b567-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b567-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="3b567-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b567-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="3b567-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b567-108">描述</span><span class="sxs-lookup"><span data-stu-id="3b567-108">DESCRIPTION</span></span>
<span data-ttu-id="3b567-109">**Get-AzDataLakeStoreItemContent** Cmdlet 會取得 Data Lake Store 中檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3b567-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="3b567-110">例子</span><span class="sxs-lookup"><span data-stu-id="3b567-110">EXAMPLES</span></span>

### <span data-ttu-id="3b567-111">範例 1：取得檔案的內容</span><span class="sxs-lookup"><span data-stu-id="3b567-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="3b567-112">此命令會從 ContosoADL 帳戶中MyFile.txt檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="3b567-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="3b567-113">範例 2：取得檔案的前兩列</span><span class="sxs-lookup"><span data-stu-id="3b567-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="3b567-114">此命令會從 ContosoADL 帳戶的檔案中MyFile.txt兩個新行分隔列。</span><span class="sxs-lookup"><span data-stu-id="3b567-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="3b567-115">參數</span><span class="sxs-lookup"><span data-stu-id="3b567-115">PARAMETERS</span></span>

### <span data-ttu-id="3b567-116">-帳戶</span><span class="sxs-lookup"><span data-stu-id="3b567-116">-Account</span></span>
<span data-ttu-id="3b567-117">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b567-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3b567-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b567-118">-DefaultProfile</span></span>
<span data-ttu-id="3b567-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b567-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b567-120">-編碼</span><span class="sxs-lookup"><span data-stu-id="3b567-120">-Encoding</span></span>
<span data-ttu-id="3b567-121">指定要建立專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="3b567-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="3b567-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3b567-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3b567-123">未知</span><span class="sxs-lookup"><span data-stu-id="3b567-123">Unknown</span></span>
- <span data-ttu-id="3b567-124">字串</span><span class="sxs-lookup"><span data-stu-id="3b567-124">String</span></span>
- <span data-ttu-id="3b567-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="3b567-125">Unicode</span></span>
- <span data-ttu-id="3b567-126">位元組</span><span class="sxs-lookup"><span data-stu-id="3b567-126">Byte</span></span>
- <span data-ttu-id="3b567-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="3b567-127">BigEndianUnicode</span></span>
- <span data-ttu-id="3b567-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="3b567-128">UTF8</span></span>
- <span data-ttu-id="3b567-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="3b567-129">UTF7</span></span>
- <span data-ttu-id="3b567-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="3b567-130">Ascii</span></span>
- <span data-ttu-id="3b567-131">預設</span><span class="sxs-lookup"><span data-stu-id="3b567-131">Default</span></span>
- <span data-ttu-id="3b567-132">Oem</span><span class="sxs-lookup"><span data-stu-id="3b567-132">Oem</span></span>
- <span data-ttu-id="3b567-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="3b567-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b567-134">-強制</span><span class="sxs-lookup"><span data-stu-id="3b567-134">-Force</span></span>
<span data-ttu-id="3b567-135">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3b567-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b567-136">-Head</span><span class="sxs-lookup"><span data-stu-id="3b567-136">-Head</span></span>
<span data-ttu-id="3b567-137">從檔案開頭 (到預覽) 分隔的列數。</span><span class="sxs-lookup"><span data-stu-id="3b567-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="3b567-138">如果前 4mb 的資料沒有遇到新的一行，則只會將該資料退回。</span><span class="sxs-lookup"><span data-stu-id="3b567-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="3b567-139">-長度</span><span class="sxs-lookup"><span data-stu-id="3b567-139">-Length</span></span>
<span data-ttu-id="3b567-140">指定要取得之內容的長度 ，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="3b567-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="3b567-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="3b567-141">-Offset</span></span>
<span data-ttu-id="3b567-142">指定在取得內容之前，要略過檔案的位元組數。</span><span class="sxs-lookup"><span data-stu-id="3b567-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="3b567-143">-路徑</span><span class="sxs-lookup"><span data-stu-id="3b567-143">-Path</span></span>
<span data-ttu-id="3b567-144">指定檔案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="3b567-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3b567-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="3b567-145">-Tail</span></span>
<span data-ttu-id="3b567-146">從檔案結尾 (以) 行分隔的列數。</span><span class="sxs-lookup"><span data-stu-id="3b567-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="3b567-147">如果前 4mb 的資料沒有遇到新的一行，則只會將該資料退回。</span><span class="sxs-lookup"><span data-stu-id="3b567-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="3b567-148">-確認</span><span class="sxs-lookup"><span data-stu-id="3b567-148">-Confirm</span></span>
<span data-ttu-id="3b567-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3b567-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b567-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b567-150">-WhatIf</span></span>
<span data-ttu-id="3b567-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b567-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b567-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b567-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b567-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b567-153">CommonParameters</span></span>
<span data-ttu-id="3b567-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b567-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b567-155">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3b567-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b567-156">輸入</span><span class="sxs-lookup"><span data-stu-id="3b567-156">INPUTS</span></span>

### <span data-ttu-id="3b567-157">System.String</span><span class="sxs-lookup"><span data-stu-id="3b567-157">System.String</span></span>

### <span data-ttu-id="3b567-158">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3b567-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3b567-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3b567-159">System.Int32</span></span>

### <span data-ttu-id="3b567-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="3b567-160">System.Int64</span></span>

### <span data-ttu-id="3b567-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="3b567-161">System.Text.Encoding</span></span>

### <span data-ttu-id="3b567-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3b567-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3b567-163">輸出</span><span class="sxs-lookup"><span data-stu-id="3b567-163">OUTPUTS</span></span>

### <span data-ttu-id="3b567-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="3b567-164">System.Byte</span></span>

### <span data-ttu-id="3b567-165">System.String</span><span class="sxs-lookup"><span data-stu-id="3b567-165">System.String</span></span>

## <span data-ttu-id="3b567-166">筆記</span><span class="sxs-lookup"><span data-stu-id="3b567-166">NOTES</span></span>

## <span data-ttu-id="3b567-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b567-167">RELATED LINKS</span></span>
