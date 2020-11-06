---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454396"
---
# <span data-ttu-id="25b46-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="25b46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25b46-102">SYNOPSIS</span></span>
<span data-ttu-id="25b46-103">刪除 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="25b46-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25b46-104">句法</span><span class="sxs-lookup"><span data-stu-id="25b46-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b46-105">說明</span><span class="sxs-lookup"><span data-stu-id="25b46-105">DESCRIPTION</span></span>
<span data-ttu-id="25b46-106">**AzureRmDataLakeStoreItem** Cmdlet 會刪除 Data Lake store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="25b46-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="25b46-107">示例</span><span class="sxs-lookup"><span data-stu-id="25b46-107">EXAMPLES</span></span>

### <span data-ttu-id="25b46-108">範例1：移除多個專案</span><span class="sxs-lookup"><span data-stu-id="25b46-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="25b46-109">這個命令會從 Data Lake Store 移除 File01.txt 和 File.csv 的檔案。</span><span class="sxs-lookup"><span data-stu-id="25b46-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="25b46-110">參數</span><span class="sxs-lookup"><span data-stu-id="25b46-110">PARAMETERS</span></span>

### <span data-ttu-id="25b46-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="25b46-111">-Account</span></span>
<span data-ttu-id="25b46-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="25b46-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="25b46-113">-Clean</span><span class="sxs-lookup"><span data-stu-id="25b46-113">-Clean</span></span>
<span data-ttu-id="25b46-114">表示此操作會移除目的檔案夾的所有內容，並保留資料夾。</span><span class="sxs-lookup"><span data-stu-id="25b46-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="25b46-115">將此參數與 *遞迴* 參數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="25b46-115">Use this parameter with the *Recurse* parameter.</span></span>

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

### <span data-ttu-id="25b46-116">-Force</span><span class="sxs-lookup"><span data-stu-id="25b46-116">-Force</span></span>
<span data-ttu-id="25b46-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="25b46-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25b46-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25b46-118">-PassThru</span></span>
<span data-ttu-id="25b46-119">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="25b46-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25b46-120">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="25b46-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25b46-121">-路徑</span><span class="sxs-lookup"><span data-stu-id="25b46-121">-Paths</span></span>
<span data-ttu-id="25b46-122">指定要移除之檔案的 Data Lake Store 路徑陣列，並從根目錄 (/) 。</span><span class="sxs-lookup"><span data-stu-id="25b46-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-123">-遞迴</span><span class="sxs-lookup"><span data-stu-id="25b46-123">-Recurse</span></span>
<span data-ttu-id="25b46-124">表示此操作會刪除目的檔案夾中的所有專案，包括子資料夾。</span><span class="sxs-lookup"><span data-stu-id="25b46-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="25b46-125">除非您指定 *Clean* 參數，否則目的檔案夾也會被刪除。</span><span class="sxs-lookup"><span data-stu-id="25b46-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b46-126">-確認</span><span class="sxs-lookup"><span data-stu-id="25b46-126">-Confirm</span></span>
<span data-ttu-id="25b46-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25b46-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b46-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b46-128">-WhatIf</span></span>
<span data-ttu-id="25b46-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25b46-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b46-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25b46-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b46-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b46-131">-DefaultProfile</span></span>
<span data-ttu-id="25b46-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25b46-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b46-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b46-133">CommonParameters</span></span>
<span data-ttu-id="25b46-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25b46-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b46-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25b46-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b46-136">輸入</span><span class="sxs-lookup"><span data-stu-id="25b46-136">INPUTS</span></span>

## <span data-ttu-id="25b46-137">輸出</span><span class="sxs-lookup"><span data-stu-id="25b46-137">OUTPUTS</span></span>

### <span data-ttu-id="25b46-138">bool</span><span class="sxs-lookup"><span data-stu-id="25b46-138">bool</span></span>
<span data-ttu-id="25b46-139">如果已指定 PassThru，則會傳回運算的結果。</span><span class="sxs-lookup"><span data-stu-id="25b46-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="25b46-140">筆記</span><span class="sxs-lookup"><span data-stu-id="25b46-140">NOTES</span></span>

## <span data-ttu-id="25b46-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="25b46-141">RELATED LINKS</span></span>

[<span data-ttu-id="25b46-142">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="25b46-143">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="25b46-144">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="25b46-145">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="25b46-146">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="25b46-147">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="25b46-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


