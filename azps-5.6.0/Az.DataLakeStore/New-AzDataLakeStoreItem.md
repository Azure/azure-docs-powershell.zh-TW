---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 46495d5a057de6c7cff21cdc09fe68d80e0c4da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912030"
---
# <span data-ttu-id="99390-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="99390-102">簡介</span><span class="sxs-lookup"><span data-stu-id="99390-102">SYNOPSIS</span></span>
<span data-ttu-id="99390-103">在 Data Lake Store 中建立新檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="99390-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="99390-104">語法</span><span class="sxs-lookup"><span data-stu-id="99390-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99390-105">描述</span><span class="sxs-lookup"><span data-stu-id="99390-105">DESCRIPTION</span></span>
<span data-ttu-id="99390-106">**New-AzDataLakeStoreItem** Cmdlet 在 Data Lake Store 中建立新檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="99390-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="99390-107">例子</span><span class="sxs-lookup"><span data-stu-id="99390-107">EXAMPLES</span></span>

### <span data-ttu-id="99390-108">範例 1：建立新檔案和新資料夾</span><span class="sxs-lookup"><span data-stu-id="99390-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="99390-109">第一個命令會建立NewFile.txt帳戶的檔案。</span><span class="sxs-lookup"><span data-stu-id="99390-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="99390-110">第二個命令會建立根資料夾的 NewFolder 資料夾。</span><span class="sxs-lookup"><span data-stu-id="99390-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="99390-111">參數</span><span class="sxs-lookup"><span data-stu-id="99390-111">PARAMETERS</span></span>

### <span data-ttu-id="99390-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="99390-112">-Account</span></span>
<span data-ttu-id="99390-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="99390-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="99390-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99390-114">-DefaultProfile</span></span>
<span data-ttu-id="99390-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="99390-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99390-116">-編碼</span><span class="sxs-lookup"><span data-stu-id="99390-116">-Encoding</span></span>
<span data-ttu-id="99390-117">指定要建立專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="99390-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="99390-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="99390-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="99390-119">未知</span><span class="sxs-lookup"><span data-stu-id="99390-119">Unknown</span></span>
- <span data-ttu-id="99390-120">字串</span><span class="sxs-lookup"><span data-stu-id="99390-120">String</span></span>
- <span data-ttu-id="99390-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="99390-121">Unicode</span></span>
- <span data-ttu-id="99390-122">位元組</span><span class="sxs-lookup"><span data-stu-id="99390-122">Byte</span></span>
- <span data-ttu-id="99390-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="99390-123">BigEndianUnicode</span></span>
- <span data-ttu-id="99390-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="99390-124">UTF8</span></span>
- <span data-ttu-id="99390-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="99390-125">UTF7</span></span>
- <span data-ttu-id="99390-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="99390-126">Ascii</span></span>
- <span data-ttu-id="99390-127">預設</span><span class="sxs-lookup"><span data-stu-id="99390-127">Default</span></span>
- <span data-ttu-id="99390-128">Oem</span><span class="sxs-lookup"><span data-stu-id="99390-128">Oem</span></span>
- <span data-ttu-id="99390-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="99390-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="99390-130">-資料夾</span><span class="sxs-lookup"><span data-stu-id="99390-130">-Folder</span></span>
<span data-ttu-id="99390-131">表示此作業會建立資料夾。</span><span class="sxs-lookup"><span data-stu-id="99390-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="99390-132">-強制</span><span class="sxs-lookup"><span data-stu-id="99390-132">-Force</span></span>
<span data-ttu-id="99390-133">表示此作業可以覆寫目的地專案 ，如果該專案已存在。</span><span class="sxs-lookup"><span data-stu-id="99390-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="99390-134">-路徑</span><span class="sxs-lookup"><span data-stu-id="99390-134">-Path</span></span>
<span data-ttu-id="99390-135">指定要建立之專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="99390-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="99390-136">-值</span><span class="sxs-lookup"><span data-stu-id="99390-136">-Value</span></span>
<span data-ttu-id="99390-137">指定要新加到您建立之專案的內容。</span><span class="sxs-lookup"><span data-stu-id="99390-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="99390-138">-確認</span><span class="sxs-lookup"><span data-stu-id="99390-138">-Confirm</span></span>
<span data-ttu-id="99390-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="99390-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99390-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99390-140">-WhatIf</span></span>
<span data-ttu-id="99390-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99390-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99390-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99390-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99390-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99390-143">CommonParameters</span></span>
<span data-ttu-id="99390-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="99390-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99390-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="99390-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99390-146">輸入</span><span class="sxs-lookup"><span data-stu-id="99390-146">INPUTS</span></span>

### <span data-ttu-id="99390-147">System.String</span><span class="sxs-lookup"><span data-stu-id="99390-147">System.String</span></span>

### <span data-ttu-id="99390-148">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="99390-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="99390-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="99390-149">System.Object</span></span>

### <span data-ttu-id="99390-150">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="99390-150">System.Text.Encoding</span></span>

### <span data-ttu-id="99390-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99390-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99390-152">輸出</span><span class="sxs-lookup"><span data-stu-id="99390-152">OUTPUTS</span></span>

### <span data-ttu-id="99390-153">System.String</span><span class="sxs-lookup"><span data-stu-id="99390-153">System.String</span></span>

## <span data-ttu-id="99390-154">筆記</span><span class="sxs-lookup"><span data-stu-id="99390-154">NOTES</span></span>

## <span data-ttu-id="99390-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="99390-155">RELATED LINKS</span></span>

[<span data-ttu-id="99390-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="99390-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="99390-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="99390-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="99390-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="99390-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="99390-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


