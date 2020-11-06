---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612768"
---
# <span data-ttu-id="e24c5-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e24c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e24c5-102">SYNOPSIS</span></span>
<span data-ttu-id="e24c5-103">在 Data Lake Store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="e24c5-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e24c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="e24c5-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e24c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="e24c5-105">DESCRIPTION</span></span>
<span data-ttu-id="e24c5-106">**新的-AzDataLakeStoreItem** Cmdlet 會在 Data Lake store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="e24c5-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e24c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="e24c5-107">EXAMPLES</span></span>

### <span data-ttu-id="e24c5-108">範例1：建立新的檔案和新資料夾</span><span class="sxs-lookup"><span data-stu-id="e24c5-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="e24c5-109">第一個命令會針對指定的帳號建立檔案 NewFile.txt。</span><span class="sxs-lookup"><span data-stu-id="e24c5-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="e24c5-110">第二個命令會在根資料夾中建立資料夾 NewFolder。</span><span class="sxs-lookup"><span data-stu-id="e24c5-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="e24c5-111">參數</span><span class="sxs-lookup"><span data-stu-id="e24c5-111">PARAMETERS</span></span>

### <span data-ttu-id="e24c5-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e24c5-112">-Account</span></span>
<span data-ttu-id="e24c5-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e24c5-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e24c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24c5-114">-DefaultProfile</span></span>
<span data-ttu-id="e24c5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e24c5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e24c5-116">編碼</span><span class="sxs-lookup"><span data-stu-id="e24c5-116">-Encoding</span></span>
<span data-ttu-id="e24c5-117">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="e24c5-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="e24c5-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e24c5-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e24c5-119">清楚</span><span class="sxs-lookup"><span data-stu-id="e24c5-119">Unknown</span></span>
- <span data-ttu-id="e24c5-120">字串</span><span class="sxs-lookup"><span data-stu-id="e24c5-120">String</span></span>
- <span data-ttu-id="e24c5-121">消除</span><span class="sxs-lookup"><span data-stu-id="e24c5-121">Unicode</span></span>
- <span data-ttu-id="e24c5-122">位元組</span><span class="sxs-lookup"><span data-stu-id="e24c5-122">Byte</span></span>
- <span data-ttu-id="e24c5-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="e24c5-123">BigEndianUnicode</span></span>
- <span data-ttu-id="e24c5-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="e24c5-124">UTF8</span></span>
- <span data-ttu-id="e24c5-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="e24c5-125">UTF7</span></span>
- <span data-ttu-id="e24c5-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="e24c5-126">Ascii</span></span>
- <span data-ttu-id="e24c5-127">設置</span><span class="sxs-lookup"><span data-stu-id="e24c5-127">Default</span></span>
- <span data-ttu-id="e24c5-128">Oem</span><span class="sxs-lookup"><span data-stu-id="e24c5-128">Oem</span></span>
- <span data-ttu-id="e24c5-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="e24c5-129">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24c5-130">-資料夾</span><span class="sxs-lookup"><span data-stu-id="e24c5-130">-Folder</span></span>
<span data-ttu-id="e24c5-131">指示這個作業會建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="e24c5-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="e24c5-132">-Force</span><span class="sxs-lookup"><span data-stu-id="e24c5-132">-Force</span></span>
<span data-ttu-id="e24c5-133">表示此操作可以覆寫目標專案（如果它已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="e24c5-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="e24c5-134">-Path</span><span class="sxs-lookup"><span data-stu-id="e24c5-134">-Path</span></span>
<span data-ttu-id="e24c5-135">指定要建立之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="e24c5-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e24c5-136">-值</span><span class="sxs-lookup"><span data-stu-id="e24c5-136">-Value</span></span>
<span data-ttu-id="e24c5-137">指定要新增到您所建立之專案的內容。</span><span class="sxs-lookup"><span data-stu-id="e24c5-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e24c5-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e24c5-138">-Confirm</span></span>
<span data-ttu-id="e24c5-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e24c5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24c5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24c5-140">-WhatIf</span></span>
<span data-ttu-id="e24c5-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e24c5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e24c5-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e24c5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24c5-143">CommonParameters</span></span>
<span data-ttu-id="e24c5-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e24c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24c5-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e24c5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24c5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e24c5-146">INPUTS</span></span>

### <span data-ttu-id="e24c5-147">System.object</span><span class="sxs-lookup"><span data-stu-id="e24c5-147">System.String</span></span>

### <span data-ttu-id="e24c5-148">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="e24c5-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e24c5-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e24c5-149">System.Object</span></span>

### <span data-ttu-id="e24c5-150">文字編碼</span><span class="sxs-lookup"><span data-stu-id="e24c5-150">System.Text.Encoding</span></span>

### <span data-ttu-id="e24c5-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e24c5-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e24c5-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e24c5-152">OUTPUTS</span></span>

### <span data-ttu-id="e24c5-153">System.object</span><span class="sxs-lookup"><span data-stu-id="e24c5-153">System.String</span></span>

## <span data-ttu-id="e24c5-154">筆記</span><span class="sxs-lookup"><span data-stu-id="e24c5-154">NOTES</span></span>

## <span data-ttu-id="e24c5-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="e24c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="e24c5-156">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="e24c5-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e24c5-158">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e24c5-159">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e24c5-160">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="e24c5-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e24c5-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


